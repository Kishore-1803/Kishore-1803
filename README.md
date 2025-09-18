<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>GitHub README Preview</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', sans-serif;
            line-height: 1.6;
            color: #e6edf3;
            background: #0d1117;
            margin: 0;
            padding: 20px;
        }
        
        .progress-bar {
            width: 100%;
            height: 8px;
            background: #21262d;
            border-radius: 4px;
            overflow: hidden;
            margin: 5px 0;
        }
        
        .progress-fill {
            height: 100%;
            background: linear-gradient(90deg, #39d353, #26a641);
            border-radius: 4px;
            animation: progressLoad 2s ease-in-out;
            transition: width 0.3s ease;
        }
        
        @keyframes progressLoad {
            from { width: 0%; }
        }
        
        .skill-item {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 8px 0;
            border-bottom: 1px solid #21262d;
        }
        
        .skill-name {
            font-weight: 600;
            min-width: 150px;
        }
        
        .skill-level {
            font-size: 0.9em;
            color: #7d8590;
            margin-left: 10px;
        }
        
        .ascii-box {
            font-family: 'Courier New', monospace;
            background: #161b22;
            border: 1px solid #30363d;
            border-radius: 6px;
            padding: 15px;
            margin: 10px 0;
            font-size: 14px;
        }
        
        .center { text-align: center; }
        .mb-20 { margin-bottom: 20px; }
        .mt-20 { margin-top: 20px; }
        
        h1, h2, h3 { color: #f0f6fc; }
        
        table {
            width: 100%;
            border-collapse: collapse;
            margin: 20px 0;
        }
        
        td {
            padding: 15px;
            vertical-align: top;
            border: 1px solid #21262d;
            background: #161b22;
        }
        
        .icons {
            margin: 15px 0;
        }
        
        .icons img {
            margin: 0 2px;
        }
        
        .quote-box {
            background: #0d419d;
            border-left: 4px solid #1f6feb;
            padding: 15px;
            margin: 20px 0;
            border-radius: 6px;
        }
        
        .connect-table td {
            text-align: center;
            background: #21262d;
            border-radius: 6px;
        }
        
        .connect-table a {
            color: #58a6ff;
            text-decoration: none;
        }
        
        .connect-table a:hover {
            text-decoration: underline;
        }
    </style>
</head>
<body>

<div class="center">
    <h1>Welcome to My Digital Universe</h1>
    
    <div class="ascii-box">
        ╔══════════════════════════════════════╗<br>
        ║           KISHORE BALAJI             ║<br>
        ║     Full Stack Developer & AI        ║<br>
        ║         Enthusiast                   ║<br>
        ╚══════════════════════════════════════╝
    </div>
</div>

<hr>

<div class="center">
    <table style="margin: 0 auto; background: none; border: none;">
        <tr>
            <td style="background: none; border: none;"><strong>Home Base</strong></td>
            <td style="background: none; border: none;"><strong>Tech Arsenal</strong></td>
            <td style="background: none; border: none;"><strong>Mission Control</strong></td>
            <td style="background: none; border: none;"><strong>Connect</strong></td>
        </tr>
    </table>
</div>

<hr>

<h2>Home Base</h2>

<table>
<tr>
<td width="40%">

<h3>System Info</h3>
<div class="ascii-box">
Name: Kishore Balaji<br>
Role: CSE(AI) Student & Full Stack Developer<br>
Institution: Amrita Vishwa Vidyapeetam, Coimbatore<br>
CGPA: 8.05/10.0<br>
Status: Available for internships & collaborations<br>
Current_Focus: AI-powered web applications<br>
Specialization: Full Stack + AI/ML Integration<br>
Coffee_Level: ████████░░ 80%
</div>

</td>
<td width="60%">

<h3>Character Stats</h3>

<div class="skill-item">
    <span class="skill-name">CREATIVITY</span>
    <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
        <div class="progress-fill" style="width: 100%;"></div>
    </div>
    <span class="skill-level">100%</span>
</div>

<div class="skill-item">
    <span class="skill-name">PROBLEM SOLVING</span>
    <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
        <div class="progress-fill" style="width: 90%;"></div>
    </div>
    <span class="skill-level">90%</span>
</div>

<div class="skill-item">
    <span class="skill-name">TEAMWORK</span>
    <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
        <div class="progress-fill" style="width: 85%;"></div>
    </div>
    <span class="skill-level">85%</span>
</div>

<div class="skill-item">
    <span class="skill-name">LEARNING SPEED</span>
    <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
        <div class="progress-fill" style="width: 95%;"></div>
    </div>
    <span class="skill-level">95%</span>
</div>

<div class="skill-item">
    <span class="skill-name">CODE QUALITY</span>
    <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
        <div class="progress-fill" style="width: 80%;"></div>
    </div>
    <span class="skill-level">80%</span>
</div>

<p><em>Special Abilities: Bug Detection, Coffee-to-Code Conversion, Late Night Debugging</em></p>

</td>
</tr>
</table>

<hr>

<h2>Tech Arsenal</h2>

<h3>Programming Languages</h3>
<div class="center">
    <div class="icons">
        <img src="https://skillicons.dev/icons?i=java,python,cpp,js&theme=dark" alt="Programming Languages" />
    </div>
    
    <div class="skill-item">
        <span class="skill-name">Java</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 90%;"></div>
        </div>
        <span class="skill-level">90%</span>
    </div>
    
    <div class="skill-item">
        <span class="skill-name">Python</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 95%;"></div>
        </div>
        <span class="skill-level">95%</span>
    </div>
    
    <div class="skill-item">
        <span class="skill-name">C++</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 75%;"></div>
        </div>
        <span class="skill-level">75%</span>
    </div>
    
    <div class="skill-item">
        <span class="skill-name">JavaScript</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 90%;"></div>
        </div>
        <span class="skill-level">90%</span>
    </div>
</div>

<h3>AI/ML Technologies</h3>
<div class="center">
    <div class="icons">
        <img src="https://skillicons.dev/icons?i=tensorflow,pytorch&theme=dark" alt="AI/ML" />
        <img src="https://img.shields.io/badge/Gemini_API-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Gemini API" />
    </div>
    
    <div class="skill-item">
        <span class="skill-name">Machine Learning</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 80%;"></div>
        </div>
        <span class="skill-level">80%</span>
    </div>
    
    <div class="skill-item">
        <span class="skill-name">Deep Learning</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 70%;"></div>
        </div>
        <span class="skill-level">70%</span>
    </div>
    
    <div class="skill-item">
        <span class="skill-name">LLM Integration</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 95%;"></div>
        </div>
        <span class="skill-level">95%</span>
    </div>
    
    <div class="skill-item">
        <span class="skill-name">Prompt Engineering</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 90%;"></div>
        </div>
        <span class="skill-level">90%</span>
    </div>
</div>

<h3>Web Development</h3>
<div class="center">
    <div class="icons">
        <img src="https://skillicons.dev/icons?i=html,css,nextjs,express,flask,fastapi&theme=dark" alt="Web Development" />
    </div>
    
    <div class="skill-item">
        <span class="skill-name">HTML/CSS</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 100%;"></div>
        </div>
        <span class="skill-level">100%</span>
    </div>
    
    <div class="skill-item">
        <span class="skill-name">Next.js</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 90%;"></div>
        </div>
        <span class="skill-level">90%</span>
    </div>
    
    <div class="skill-item">
        <span class="skill-name">Express.js</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 75%;"></div>
        </div>
        <span class="skill-level">75%</span>
    </div>
    
    <div class="skill-item">
        <span class="skill-name">Flask</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 80%;"></div>
        </div>
        <span class="skill-level">80%</span>
    </div>
    
    <div class="skill-item">
        <span class="skill-name">FastAPI</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 95%;"></div>
        </div>
        <span class="skill-level">95%</span>
    </div>
</div>

<h3>Database Systems</h3>
<div class="center">
    <div class="icons">
        <img src="https://skillicons.dev/icons?i=postgresql,mongodb&theme=dark" alt="Databases" />
        <img src="https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white" alt="Supabase" />
        <img src="https://img.shields.io/badge/SQL-336791?style=for-the-badge&logo=postgresql&logoColor=white" alt="SQL" />
    </div>
    
    <div class="skill-item">
        <span class="skill-name">PostgreSQL</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 95%;"></div>
        </div>
        <span class="skill-level">95%</span>
    </div>
    
    <div class="skill-item">
        <span class="skill-name">MongoDB</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 90%;"></div>
        </div>
        <span class="skill-level">90%</span>
    </div>
    
    <div class="skill-item">
        <span class="skill-name">Supabase</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 80%;"></div>
        </div>
        <span class="skill-level">80%</span>
    </div>
    
    <div class="skill-item">
        <span class="skill-name">SQL</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 90%;"></div>
        </div>
        <span class="skill-level">90%</span>
    </div>
</div>

<h3>Tools & Platforms</h3>
<div class="center">
    <div class="icons">
        <img src="https://skillicons.dev/icons?i=git,github,vscode&theme=dark" alt="Tools" />
        <img src="https://img.shields.io/badge/CI/CD-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="CI/CD" />
    </div>
    
    <div class="skill-item">
        <span class="skill-name">Git/GitHub</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 100%;"></div>
        </div>
        <span class="skill-level">100%</span>
    </div>
    
    <div class="skill-item">
        <span class="skill-name">Visual Studio Code</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 100%;"></div>
        </div>
        <span class="skill-level">100%</span>
    </div>
    
    <div class="skill-item">
        <span class="skill-name">CI/CD</span>
        <div class="progress-bar" style="flex-grow: 1; margin: 0 10px;">
            <div class="progress-fill" style="width: 70%;"></div>
        </div>
        <span class="skill-level">70%</span>
    </div>
</div>

<hr>

<h2>Achievement Unlocked</h2>

<div class="center">

<table style="margin: 20px auto;">
<tr>
<th>Badge</th>
<th>Level</th>
<th>Description</th>
</tr>
<tr>
<td><strong>Problem Solver</strong></td>
<td>Expert</td>
<td>Solved 100+ coding challenges</td>
</tr>
<tr>
<td><strong>Full Stack</strong></td>
<td>Advanced</td>
<td>Built 10+ complete applications</td>
</tr>
<tr>
<td><strong>AI Explorer</strong></td>
<td>Intermediate</td>
<td>Implemented ML models</td>
</tr>
<tr>
<td><strong>Tool Creator</strong></td>
<td>Beginner+</td>
<td>Developed utility tools</td>
</tr>
<tr>
<td><strong>Mobile Ready</strong></td>
<td>Learning</td>
<td>Exploring React Native</td>
</tr>
</table>

</div>

<hr>

<h2>Code Philosophy</h2>

<div class="center">
    <div class="ascii-box">
const myApproach = {<br>
  design: "User-first, always",<br>
  code: "Clean, readable, maintainable",<br>
  testing: "Write tests, sleep peacefully",<br>
  learning: "Never stop, never settle",<br>
  collaboration: "Teamwork makes the dream work",<br>
  <br>
  motto: function() {<br>
    return "Code is poetry, bugs are just typos!";<br>
  }<br>
};
    </div>
</div>

<hr>

<h2>Fun Zone</h2>

<div class="center">
    <h3>Random Developer Facts</h3>
</div>

<table>
<tr>
<td width="33%" class="center">
<strong>Best Coding Time</strong><br>
11 PM - 3 AM<br>
<em>When the world sleeps,<br>I code</em>
</td>
<td width="33%" class="center">
<strong>Fuel of Choice</strong><br>
Strong Black Coffee<br>
<em>Debugging juice<br>Error eliminator</em>
</td>
<td width="33%" class="center">
<strong>Coding Soundtrack</strong><br>
Lo-fi Hip Hop<br>
<em>Brain.exe optimization<br>Focus mode activated</em>
</td>
</tr>
</table>

<div class="center">
    <h3>Developer Mood Tracker</h3>
    <p><strong>Today I'm feeling:</strong> <code>motivated && caffeinated && ready_to_code</code></p>
    
    <div class="skill-item" style="justify-content: center;">
        <span style="margin-right: 10px;">Mood:</span>
        <div class="progress-bar" style="width: 300px;">
            <div class="progress-fill" style="width: 100%;"></div>
        </div>
        <span style="margin-left: 10px;">100% Ready to Ship!</span>
    </div>
</div>

<hr>

<h2>Connect With Me</h2>

<div class="center">
    <h3>Find Me In The Digital World</h3>

    <table class="connect-table">
    <tr>
    <td width="25%">
    <strong>Portfolio</strong><br>
    <a href="https://kishore-balaji.vercel.app/" target="_blank">kishore-balaji.vercel.app</a><br>
    <em>My digital showcase</em>
    </td>
    <td width="25%">
    <strong>LinkedIn</strong><br>
    <a href="https://www.linkedin.com/in/kishore-balaji-081168292" target="_blank">kishore-balaji</a><br>
    <em>Professional network</em>
    </td>
    <td width="25%">
    <strong>Instagram</strong><br>
    <a href="https://www.instagram.com/kishore_balaji_03" target="_blank">@kishore_balaji_03</a><br>
    <em>Life in pixels</em>
    </td>
    <td width="25%">
    <strong>Email</strong><br>
    kishorebalaji03@gmail.com<br>
    <em>Direct communication</em>
    </td>
    </tr>
    </table>

    <h3>LeetCode Journey</h3>
    <img src="https://leetcard.jacoblin.cool/kishore_balaji_03?theme=unicorn&font=source_code_pro" alt="LeetCode Progress" />
</div>

<hr>

<div class="center">
    <h3>The End... Or Is It?</h3>
    
    <div class="ascii-box">
     ╔══════════════════════════════════════╗<br>
     ║  "The best time to plant a tree was  ║<br>
     ║   20 years ago. The second best      ║<br>
     ║   time is now. The third best time   ║<br>
     ║   is right after you fix this bug."  ║<br>
     ║                                      ║<br>
     ║           - Ancient Developer        ║<br>
     ╚══════════════════════════════════════╝
    </div>

    <p><strong>Thanks for visiting my corner of the internet!</strong><br>
    <em>Now go build something awesome!</em></p>

    <hr>

    <sub>This README updates itself with my mood swings and coffee levels</sub>
</div>

<script>
// Add some interactive animations
document.addEventListener('DOMContentLoaded', function() {
    const progressBars = document.querySelectorAll('.progress-fill');
    
    // Animate progress bars on page load
    setTimeout(() => {
        progressBars.forEach(bar => {
            const width = bar.style.width;
            bar.style.width = '0%';
            setTimeout(() => {
                bar.style.width = width;
            }, Math.random() * 500);
        });
    }, 500);
    
    // Add hover effects
    const skillItems = document.querySelectorAll('.skill-item');
    skillItems.forEach(item => {
        item.addEventListener('mouseenter', function() {
            this.style.backgroundColor = '#21262d';
            this.style.transform = 'translateX(5px)';
            this.style.transition = 'all 0.3s ease';
        });
        
        item.addEventListener('mouseleave', function() {
            this.style.backgroundColor = 'transparent';
            this.style.transform = 'translateX(0)';
        });
    });
});
</script>

</body>
</html>
