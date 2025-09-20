<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kishore Balaji - Digital Matrix</title>
    <style>
        body {
            font-family: 'Courier New', monospace;
            line-height: 1.6;
            color: #00ff00;
            background: #0a0a0a;
            margin: 0;
            padding: 20px;
            overflow-x: hidden;
        }
        
        .matrix-bg {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.1;
        }
        
        .glitch-text {
            animation: glitch 2s infinite;
            color: #00ff00;
            text-shadow: 0 0 10px #00ff00;
        }
        
        @keyframes glitch {
            0%, 90%, 100% { transform: translateX(0); }
            20% { transform: translateX(-2px); }
            40% { transform: translateX(2px); }
            60% { transform: translateX(-1px); }
            80% { transform: translateX(1px); }
        }
        
        .terminal-window {
            border: 2px solid #00ff00;
            border-radius: 10px;
            background: rgba(0, 0, 0, 0.8);
            padding: 20px;
            margin: 20px 0;
            box-shadow: 0 0 20px rgba(0, 255, 0, 0.3);
        }
        
        .terminal-header {
            display: flex;
            align-items: center;
            margin-bottom: 15px;
            padding-bottom: 10px;
            border-bottom: 1px solid #00ff00;
        }
        
        .terminal-buttons {
            display: flex;
            gap: 5px;
        }
        
        .btn {
            width: 12px;
            height: 12px;
            border-radius: 50%;
        }
        
        .btn-red { background: #ff5f56; }
        .btn-yellow { background: #ffbd2e; }
        .btn-green { background: #27ca3f; }
        
        .typing-animation {
            overflow: hidden;
            border-right: 3px solid #00ff00;
            white-space: nowrap;
            animation: typing 3s steps(40, end), blink-caret 0.75s step-end infinite;
        }
        
        @keyframes typing {
            from { width: 0; }
            to { width: 100%; }
        }
        
        @keyframes blink-caret {
            from, to { border-color: transparent; }
            50% { border-color: #00ff00; }
        }
        
        .skill-bar-container {
            margin: 10px 0;
            padding: 5px;
        }
        
        .skill-name {
            display: flex;
            justify-content: space-between;
            margin-bottom: 5px;
            color: #00ff00;
            font-weight: bold;
        }
        
        .skill-bar {
            width: 100%;
            height: 20px;
            background: #1a1a1a;
            border: 1px solid #00ff00;
            border-radius: 10px;
            overflow: hidden;
            position: relative;
        }
        
        .skill-fill {
            height: 100%;
            background: linear-gradient(90deg, #00ff00, #00cc00, #008800);
            border-radius: 8px;
            animation: skillLoad 3s ease-in-out;
            position: relative;
            transition: all 0.5s ease;
        }
        
        .skill-fill::after {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255,255,255,0.3), transparent);
            animation: shimmer 2s infinite;
        }
        
        @keyframes skillLoad {
            from { width: 0%; }
        }
        
        @keyframes shimmer {
            0% { left: -100%; }
            100% { left: 100%; }
        }
        
        .matrix-table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        
        .matrix-table td {
            padding: 15px;
            border: 1px solid #00ff00;
            background: rgba(0, 255, 0, 0.05);
            vertical-align: top;
        }
        
        .center { text-align: center; }
        
        .neon-glow {
            text-shadow: 0 0 5px #00ff00, 0 0 10px #00ff00, 0 0 15px #00ff00;
        }
        
        .status-indicator {
            display: inline-block;
            width: 10px;
            height: 10px;
            border-radius: 50%;
            background: #00ff00;
            animation: pulse 2s infinite;
            margin-right: 10px;
        }
        
        @keyframes pulse {
            0%, 100% { opacity: 1; }
            50% { opacity: 0.3; }
        }
        
        .code-block {
            background: #0d0d0d;
            border: 1px solid #00ff00;
            border-radius: 5px;
            padding: 15px;
            margin: 15px 0;
            font-family: 'Courier New', monospace;
            overflow-x: auto;
        }
        
        .icons-container {
            text-align: center;
            margin: 20px 0;
        }
        
        .icons-container img {
            margin: 5px;
            filter: drop-shadow(0 0 5px #00ff00);
            transition: all 0.3s ease;
        }
        
        .icons-container img:hover {
            filter: drop-shadow(0 0 15px #00ff00);
            transform: scale(1.1);
        }
        
        h1, h2, h3 {
            color: #00ff00;
            text-shadow: 0 0 10px #00ff00;
        }
        
        .connect-links {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 15px;
            margin: 20px 0;
        }
        
        .connect-card {
            border: 1px solid #00ff00;
            border-radius: 8px;
            padding: 15px;
            text-align: center;
            background: rgba(0, 255, 0, 0.05);
            transition: all 0.3s ease;
        }
        
        .connect-card:hover {
            background: rgba(0, 255, 0, 0.1);
            box-shadow: 0 0 15px rgba(0, 255, 0, 0.3);
            transform: translateY(-2px);
        }
        
        .connect-card a {
            color: #00ff00;
            text-decoration: none;
        }
        
        .connect-card a:hover {
            text-shadow: 0 0 5px #00ff00;
        }
    </style>
</head>
<body>

<div class="matrix-bg">
    <canvas id="matrix-canvas"></canvas>
</div>

<div class="center">
    <h1 class="glitch-text neon-glow">SYSTEM.LOAD("KISHORE_BALAJI")</h1>
    
    <div class="terminal-window">
        <div class="terminal-header">
            <div class="terminal-buttons">
                <div class="btn btn-red"></div>
                <div class="btn btn-yellow"></div>
                <div class="btn btn-green"></div>
            </div>
            <span style="margin-left: 15px;">kishore@digital-matrix:~$</span>
        </div>
        <div class="typing-animation">
            Full Stack Developer + AI Engineer | Student.exe | Level: 21 | XP: 8050
        </div>
    </div>
</div>

<hr style="border-color: #00ff00;">

<h2 class="center neon-glow">SYSTEM STATUS</h2>

<div class="terminal-window">
    <div class="matrix-table">
        <table style="width: 100%; color: #00ff00;">
            <tr>
                <td width="50%">
                    <h3>USER.INFO</h3>
                    <div class="code-block">
                        <span class="status-indicator"></span>Name: Kishore Balaji<br>
                        <span class="status-indicator"></span>Class: CSE(AI) Student<br>
                        <span class="status-indicator"></span>Institution: Amrita Vishwa Vidyapeetam<br>
                        <span class="status-indicator"></span>Performance: 8.05/10.0 CGPA<br>
                        <span class="status-indicator"></span>Status: ACTIVE - Ready for missions<br>
                        <span class="status-indicator"></span>Specialization: Full Stack + AI Integration<br>
                        <span class="status-indicator"></span>Energy Level: 80% ████████░░
                    </div>
                </td>
                <td width="50%">
                    <h3>CORE.ATTRIBUTES</h3>
                    
                    <div class="skill-bar-container">
                        <div class="skill-name">
                            <span>PROBLEM_SOLVING</span>
                            <span>95%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-fill" style="width: 95%;"></div>
                        </div>
                    </div>
                    
                    <div class="skill-bar-container">
                        <div class="skill-name">
                            <span>CODE_QUALITY</span>
                            <span>90%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-fill" style="width: 90%;"></div>
                        </div>
                    </div>
                    
                    <div class="skill-bar-container">
                        <div class="skill-name">
                            <span>LEARNING_SPEED</span>
                            <span>98%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-fill" style="width: 98%;"></div>
                        </div>
                    </div>
                    
                    <div class="skill-bar-container">
                        <div class="skill-name">
                            <span>COLLABORATION</span>
                            <span>85%</span>
                        </div>
                        <div class="skill-bar">
                            <div class="skill-fill" style="width: 85%;"></div>
                        </div>
                    </div>
                </td>
            </tr>
        </table>
    </div>
</div>

<hr style="border-color: #00ff00;">

<h2 class="center neon-glow">SYSTEM.SKILLS</h2>

<div class="terminal-window">
    <h3>PROGRAMMING.LANGUAGES</h3>
    <div class="icons-container">
        <img src="https://go-skill-icons.vercel.app/api/icons?i=java,python,cpp,javascript&theme=dark" alt="Programming Languages" />
    </div>
    
    <div class="skill-bar-container">
        <div class="skill-name"><span>Java</span><span>90%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 90%;"></div></div>
    </div>
    
    <div class="skill-bar-container">
        <div class="skill-name"><span>Python</span><span>95%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 95%;"></div></div>
    </div>
    
    <div class="skill-bar-container">
        <div class="skill-name"><span>C++</span><span>75%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 75%;"></div></div>
    </div>
    
    <div class="skill-bar-container">
        <div class="skill-name"><span>JavaScript</span><span>90%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 90%;"></div></div>
    </div>
</div>

<div class="terminal-window">
    <h3>AI.MACHINE_LEARNING</h3>
    <div class="icons-container">
        <img src="https://go-skill-icons.vercel.app/api/icons?i=tensorflow,pytorch,numpy,pandas&theme=dark" alt="AI/ML" />
    </div>
    
    <div class="skill-bar-container">
        <div class="skill-name"><span>Machine Learning</span><span>80%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 80%;"></div></div>
    </div>
    
    <div class="skill-bar-container">
        <div class="skill-name"><span>Deep Learning</span><span>70%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 70%;"></div></div>
    </div>
    
    <div class="skill-bar-container">
        <div class="skill-name"><span>LLM Integration</span><span>95%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 95%;"></div></div>
    </div>
    
    <div class="skill-bar-container">
        <div class="skill-name"><span>Prompt Engineering</span><span>90%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 90%;"></div></div>
    </div>
</div>

<div class="terminal-window">
    <h3>WEB.DEVELOPMENT</h3>
    <div class="icons-container">
        <img src="https://go-skill-icons.vercel.app/api/icons?i=html,css,react,next,express,flask,fastapi&theme=dark" alt="Web Development" />
    </div>
    
    <div class="skill-bar-container">
        <div class="skill-name"><span>HTML/CSS</span><span>100%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 100%;"></div></div>
    </div>
    
    <div class="skill-bar-container">
        <div class="skill-name"><span>React.js</span><span>90%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 90%;"></div></div>
    </div>
    
    <div class="skill-bar-container">
        <div class="skill-name"><span>Next.js</span><span>90%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 90%;"></div></div>
    </div>
    
    <div class="skill-bar-container">
        <div class="skill-name"><span>FastAPI</span><span>95%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 95%;"></div></div>
    </div>
</div>

<div class="terminal-window">
    <h3>DATABASE.SYSTEMS</h3>
    <div class="icons-container">
        <img src="https://go-skill-icons.vercel.app/api/icons?i=postgresql,mongodb,supabase&theme=dark" alt="Databases" />
    </div>
    
    <div class="skill-bar-container">
        <div class="skill-name"><span>PostgreSQL</span><span>95%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 95%;"></div></div>
    </div>
    
    <div class="skill-bar-container">
        <div class="skill-name"><span>MongoDB</span><span>90%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 90%;"></div></div>
    </div>
    
    <div class="skill-bar-container">
        <div class="skill-name"><span>Supabase</span><span>80%</span></div>
        <div class="skill-bar"><div class="skill-fill" style="width: 80%;"></div></div>
    </div>
</div>

<hr style="border-color: #00ff00;">

<h2 class="center neon-glow">CURRENT.PROCESSES</h2>

<div class="terminal-window">
    <div class="code-block">
        <div style="color: #00ff00;">
            <span style="color: #ffff00;">$</span> ps aux | grep current_projects<br>
            ▶ ai_powered_web_apps     RUNNING    High Priority<br>
            ▶ open_source_contrib     RUNNING    Medium Priority<br>
            ▶ system_design_learning  RUNNING    High Priority<br>
            ▶ react_advanced_patterns RUNNING    Medium Priority<br>
            ▶ cloud_architecture      RUNNING    Learning Mode<br>
        </div>
    </div>
</div>

<hr style="border-color: #00ff00;">

<h2 class="center neon-glow">SYSTEM.PHILOSOPHY</h2>

<div class="terminal-window">
    <div class="code-block">
        <span style="color: #ffff00;">const</span> <span style="color: #00ffff;">codePhilosophy</span> = {<br>
        &nbsp;&nbsp;<span style="color: #ffff00;">design</span>: <span style="color: #ffffff;">"User-first, always"</span>,<br>
        &nbsp;&nbsp;<span style="color: #ffff00;">code</span>: <span style="color: #ffffff;">"Clean, readable, maintainable"</span>,<br>
        &nbsp;&nbsp;<span style="color: #ffff00;">testing</span>: <span style="color: #ffffff;">"Write tests, sleep peacefully"</span>,<br>
        &nbsp;&nbsp;<span style="color: #ffff00;">learning</span>: <span style="color: #ffffff;">"Never stop, never settle"</span>,<br>
        &nbsp;&nbsp;<span style="color: #ffff00;">collaboration</span>: <span style="color: #ffffff;">"Teamwork makes the dream work"</span>,<br><br>
        &nbsp;&nbsp;<span style="color: #ffff00;">motto</span>: <span style="color: #00ffff;">function</span>() {<br>
        &nbsp;&nbsp;&nbsp;&nbsp;<span style="color: #ffff00;">return</span> <span style="color: #ffffff;">"Code is poetry, bugs are just syntax errors in reality"</span>;<br>
        &nbsp;&nbsp;}<br>
        };
    </div>
</div>

<hr style="border-color: #00ff00;">

<h2 class="center neon-glow">NETWORK.CONNECTIONS</h2>

<div class="connect-links">
    <div class="connect-card">
        <h4>MAIN.SERVER</h4>
        <a href="https://kishore-balaji.vercel.app/" target="_blank">kishore-balaji.vercel.app</a>
        <p>Digital portfolio & projects</p>
    </div>
    
    <div class="connect-card">
        <h4>PROFESSIONAL.NET</h4>
        <a href="https://www.linkedin.com/in/kishore-balaji-081168292" target="_blank">LinkedIn Profile</a>
        <p>Career & networking hub</p>
    </div>
    
    <div class="connect-card">
        <h4>SOCIAL.STREAM</h4>
        <a href="https://www.instagram.com/kishore_balaji_03" target="_blank">@kishore_balaji_03</a>
        <p>Life beyond the code</p>
    </div>
    
    <div class="connect-card">
        <h4>DIRECT.COMM</h4>
        <a href="mailto:kishorebalajisivani@gmail.com">Send Message</a>
        <p>kishorebalajisivani@gmail.com</p>
    </div>
</div>

<div class="center">
    <h3>CODING.CHALLENGE.STATS</h3>
    <img src="https://leetcard.jacoblin.cool/kishore_balaji_03?theme=dark&font=source_code_pro" alt="LeetCode Stats" style="border: 1px solid #00ff00; border-radius: 10px;" />
</div>

<hr style="border-color: #00ff00;">

<div class="center">
    <div class="terminal-window">
        <div class="code-block">
            <span style="color: #00ff00;">╔════════════════════════════════════════════╗</span><br>
            <span style="color: #00ff00;">║  "First, solve the problem. Then, write   ║</span><br>
            <span style="color: #00ff00;">║   the code. Finally, make it beautiful."  ║</span><br>
            <span style="color: #00ff00;">║                                            ║</span><br>
            <span style="color: #00ff00;">║           - Code.Philosophy.exe           ║</span><br>
            <span style="color: #00ff00;">╚════════════════════════════════════════════╝</span>
        </div>
        
        <p class="neon-glow">Thanks for accessing my digital matrix!</p>
        <p style="color: #888;">Now go build something that matters.</p>
        
        <div style="margin-top: 20px;">
            <span class="status-indicator"></span>
            <em>This profile auto-updates with my coding adventures and coffee consumption levels</em>
        </div>
    </div>
</div>

<script>
// Matrix background animation
const canvas = document.getElementById('matrix-canvas');
const ctx = canvas.getContext('2d');

canvas.width = window.innerWidth;
canvas.height = window.innerHeight;

const matrix = "ABCDEFGHIJKLMNOPQRSTUVWXYZ123456789@#$%^&*()*&^%+-/~{[|`]}";
const matrixArray = matrix.split("");

const font_size = 10;
const columns = canvas.width / font_size;

const drops = [];
for(let x = 0; x < columns; x++) {
    drops[x] = 1;
}

function drawMatrix() {
    ctx.fillStyle = 'rgba(0, 0, 0, 0.04)';
    ctx.fillRect(0, 0, canvas.width, canvas.height);
    
    ctx.fillStyle = '#00ff00';
    ctx.font = font_size + 'px arial';
    
    for(let i = 0; i < drops.length; i++) {
        const text = matrixArray[Math.floor(Math.random() * matrixArray.length)];
        ctx.fillText(text, i * font_size, drops[i] * font_size);
        
        if(drops[i] * font_size > canvas.height && Math.random() > 0.975) {
            drops[i] = 0;
        }
        drops[i]++;
    }
}

setInterval(drawMatrix, 35);

// Skill bar animations
document.addEventListener('DOMContentLoaded', function() {
    const skillBars = document.querySelectorAll('.skill-fill');
    
    // Animate skill bars on page load
    setTimeout(() => {
        skillBars.forEach((bar, index) => {
            const width = bar.style.width;
            bar.style.width = '0%';
            setTimeout(() => {
                bar.style.width = width;
            }, index * 100);
        });
    }, 1000);
    
    // Add hover effects to skill containers
    const skillContainers = document.querySelectorAll('.skill-bar-container');
    skillContainers.forEach(container => {
        container.addEventListener('mouseenter', function() {
            this.style.transform = 'scale(1.02)';
            this.style.transition = 'all 0.3s ease';
        });
        
        container.addEventListener('mouseleave', function() {
            this.style.transform = 'scale(1)';
        });
    });
});

// Resize canvas when window resizes
window.addEventListener('resize', function() {
    canvas.width = window.innerWidth;
    canvas.height = window.innerHeight;
});
</script>

</body>
</html>
