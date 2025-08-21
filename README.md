<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Jawad Shah - Full Stack Developer</title>
    <style>
        :root {
            --primary: #0ea5e9;
            --secondary: #7e22ce;
            --dark: #1e293b;
            --light: #f8fafc;
            --gray: #64748b;
            --accent: #ec4899;
            --card-bg: #1a1b26;
            --header-bg: #16161e;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #0f172a, #1e293b);
            color: var(--light);
            line-height: 1.6;
            padding: 20px;
            max-width: 1200px;
            margin: 0 auto;
        }
        
        .container {
            display: flex;
            flex-direction: column;
            gap: 30px;
        }
        
        .header {
            text-align: center;
            padding: 30px 20px;
            background: var(--header-bg);
            border-radius: 16px;
            box-shadow: 0 10px 25px rgba(0, 0, 0, 0.3);
        }
        
        .avatar {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            border: 4px solid var(--primary);
            margin-bottom: 20px;
            object-fit: cover;
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
            background: linear-gradient(90deg, var(--primary), var(--accent));
            -webkit-background-clip: text;
            background-clip: text;
            color: transparent;
        }
        
        h2 {
            font-size: 1.8rem;
            margin: 25px 0 15px;
            color: var(--primary);
        }
        
        h3 {
            font-size: 1.4rem;
            margin: 20px 0 10px;
            color: var(--secondary);
        }
        
        p {
            margin-bottom: 15px;
            color: #cbd5e1;
        }
        
        .badges {
            display: flex;
            justify-content: center;
            gap: 10px;
            flex-wrap: wrap;
            margin: 20px 0;
        }
        
        .badge {
            display: inline-block;
            padding: 8px 16px;
            background: rgba(30, 41, 59, 0.6);
            border-radius: 50px;
            color: var(--light);
            text-decoration: none;
            font-size: 0.9rem;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .badge:hover {
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
            background: var(--primary);
        }
        
        .section {
            background: var(--card-bg);
            border-radius: 16px;
            padding: 25px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
        }
        
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }
        
        .tech-item {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            padding: 15px 10px;
            background: rgba(30, 41, 59, 0.6);
            border-radius: 12px;
            transition: all 0.3s ease;
        }
        
        .tech-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
            background: var(--primary);
        }
        
        .tech-icon {
            width: 40px;
            height: 40px;
            margin-bottom: 8px;
        }
        
        .stats-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .stat-card {
            background: rgba(30, 41, 59, 0.6);
            border-radius: 12px;
            padding: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
        }
        
        .stat-value {
            font-size: 2.5rem;
            font-weight: bold;
            margin: 10px 0;
            color: var(--primary);
        }
        
        .stat-label {
            color: #94a3b8;
            font-size: 0.9rem;
        }
        
        .metrics-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .metric-card {
            background: rgba(30, 41, 59, 0.6);
            border-radius: 12px;
            padding: 20px;
            display: flex;
            align-items: center;
            gap: 15px;
        }
        
        .metric-icon {
            width: 40px;
            height: 40px;
            color: var(--primary);
            flex-shrink: 0;
        }
        
        .metric-content {
            flex: 1;
        }
        
        .metric-value {
            font-size: 1.5rem;
            font-weight: bold;
            margin-bottom: 5px;
        }
        
        .metric-label {
            color: #94a3b8;
            font-size: 0.9rem;
        }
        
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 20px;
            margin-top: 20px;
        }
        
        .project-card {
            background: rgba(30, 41, 59, 0.6);
            border-radius: 12px;
            padding: 20px;
            transition: all 0.3s ease;
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
        }
        
        .project-title {
            font-size: 1.3rem;
            margin-bottom: 10px;
            color: var(--primary);
        }
        
        .project-link {
            display: inline-block;
            margin-top: 15px;
            color: var(--accent);
            text-decoration: none;
            font-weight: 500;
        }
        
        .project-link:hover {
            text-decoration: underline;
        }
        
        .habits-list {
            list-style: none;
            margin-top: 15px;
        }
        
        .habits-list li {
            padding: 10px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
            display: flex;
            align-items: center;
        }
        
        .habits-list li:before {
            content: "•";
            color: var(--primary);
            font-weight: bold;
            display: inline-block;
            width: 20px;
            font-size: 1.5rem;
        }
        
        footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            color: #94a3b8;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .stats-container, .metrics-grid, .projects-grid {
                grid-template-columns: 1fr;
            }
            
            h1 {
                font-size: 2rem;
            }
            
            h2 {
                font-size: 1.5rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <header class="header">
            <img src="https://media2.giphy.com/media/79uMvMuByazSk1cZUX/giphy.gif?cid=ecf05e473ocvmlvn2df8dfx3uh3hrkom2vtc1e4udmv8z640&rid=giphy.gif&ct=s" alt="wave" class="avatar" />
            <h1>Hi, I'm Jawad Shah 👋</h1>
            <p><b>Full-Stack Developer</b> — building robust web apps with delightful UX.</p>
            <div class="badges">
                <a href="mailto:col.jawadshahak47@gmail.com" class="badge">Email</a>
                <a href="https://www.linkedin.com/in/jawad-shah/" class="badge">LinkedIn</a>
                <a href="https://twitter.com/private_boii" class="badge">Twitter</a>
                <a href="https://jawad114.github.io/" class="badge">Portfolio</a>
            </div>
        </header>

        <!-- About Me Section -->
        <section class="section">
            <h2>About Me</h2>
            <p>🚀 I love shipping clean, well-tested features.</p>
            <p>🌱 Currently diving into <b>ML</b> & scalable architectures.</p>
            <p>🤝 Open to collaboration on impactful OSS or product work.</p>
            <p>💬 Ask me about React, Node.js, TypeScript, and cloud dev.</p>
        </section>

        <!-- Tech Stack Section -->
        <section class="section">
            <h2>Tech I Use</h2>
            <div class="tech-grid">
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/github/explore/master/topics/html/html.png" alt="HTML" class="tech-icon">
                    <span>HTML</span>
                </div>
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/github/explore/master/topics/css/css.png" alt="CSS" class="tech-icon">
                    <span>CSS</span>
                </div>
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/github/explore/master/topics/javascript/javascript.png" alt="JavaScript" class="tech-icon">
                    <span>JavaScript</span>
                </div>
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/github/explore/master/topics/typescript/typescript.png" alt="TypeScript" class="tech-icon">
                    <span>TypeScript</span>
                </div>
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/github/explore/master/topics/react/react.png" alt="React" class="tech-icon">
                    <span>React</span>
                </div>
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/github/explore/master/topics/nextjs/nextjs.png" alt="Next.js" class="tech-icon">
                    <span>Next.js</span>
                </div>
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/github/explore/master/topics/nodejs/nodejs.png" alt="Node.js" class="tech-icon">
                    <span>Node.js</span>
                </div>
                <div class="tech-item">
                    <img src="https://raw.githubusercontent.com/github/explore/master/topics/express/express.png" alt="Express" class="tech-icon">
                    <span>Express</span>
                </div>
            </div>
        </section>

        <!-- GitHub Metrics Section -->
        <section class="section">
            <h2>GitHub Metrics</h2>
            <div class="metrics-grid">
                <div class="metric-card">
                    <svg class="metric-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" width="16" height="16">
                        <path fill="currentColor" fill-rule="evenodd" d="M1.5 8a6.5 6.5 0 1113 0 6.5 6.5 0 01-13 0zM8 0a8 8 0 100 16A8 8 0 008 0zm.5 4.75a.75.75 0 00-1.5 0v3.5a.75.75 0 00.471.696l2.5 1a.75.75 0 00.557-1.392L8.5 7.742V4.75z"/>
                    </svg>
                    <div class="metric-content">
                        <div class="metric-value">6 years</div>
                        <div class="metric-label">On GitHub</div>
                    </div>
                </div>
                
                <div class="metric-card">
                    <svg class="metric-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" width="16" height="16">
                        <path fill="currentColor" fill-rule="evenodd" d="M5.5 3.5a2 2 0 100 4 2 2 0 000-4zM2 5.5a3.5 3.5 0 115.898 2.549 5.507 5.507 0 013.034 4.084.75.75 0 11-1.482.235 4.001 4.001 0 00-7.9 0 .75.75 0 01-1.482-.236A5.507 5.507 0 013.102 8.05 3.49 3.49 0 012 5.5zM11 4a.75.75 0 100 1.5 1.5 1.5 0 01.666 2.844.75.75 0 00-.416.672v.352a.75.75 0 00.574.73c1.2.289 2.162 1.2 2.522 2.372a.75.75 0 101.434-.44 5.01 5.01 0 00-2.56-3.012A3 3 0 0011 4z"/>
                    </svg>
                    <div class="metric-content">
                        <div class="metric-value">103</div>
                        <div class="metric-label">Followers</div>
                    </div>
                </div>
                
                <div class="metric-card">
                    <svg class="metric-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" width="16" height="16">
                        <path fill="currentColor" fill-rule="evenodd" d="M1 2.5A2.5 2.5 0 013.5 0h8.75a.75.75 0 01.75.75v3.5a.75.75 0 01-1.5 0V1.5h-8a1 1 0 00-1 1v6.708A2.492 2.492 0 013.5 9h3.25a.75.75 0 010 1.5H3.5a1 1 0 100 2h5.75a.75.75 0 010 1.5H3.5A2.5 2.5 0 011 11.5v-9zm13.23 7.79a.75.75 0 001.06-1.06l-2.505-2.505a.75.75 0 00-1.06 0L9.22 9.229a.75.75 0 001.06 1.061l1.225-1.224v6.184a.75.75 0 001.5 0V9.066l1.224 1.224z"/>
                    </svg>
                    <div class="metric-content">
                        <div class="metric-value">51</div>
                        <div class="metric-label">Repositories Contributed To</div>
                    </div>
                </div>
                
                <div class="metric-card">
                    <svg class="metric-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" width="16" height="16">
                        <path fill="currentColor" fill-rule="evenodd" d="M10.5 7.75a2.5 2.5 0 11-5 0 2.5 2.5 0 015 0zm1.43.75a4.002 4.002 0 01-7.86 0H.75a.75.75 0 110-1.5h3.32a4.001 4.001 0 017.86 0h3.32a.75.75 0 110 1.5h-3.32z"/>
                    </svg>
                    <div class="metric-content">
                        <div class="metric-value">7,102</div>
                        <div class="metric-label">Commits</div>
                    </div>
                </div>
                
                <div class="metric-card">
                    <svg class="metric-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" width="16" height="16">
                        <path fill="currentColor" fill-rule="evenodd" d="M7.177 3.073L9.573.677A.25.25 0 0110 .854v4.792a.25.25 0 01-.427.177L7.177 3.427a.25.25 0 010-.354zM3.75 2.5a.75.75 0 100 1.5.75.75 0 000-1.5zm-2.25.75a2.25 2.25 0 113 2.122v5.256a2.251 2.251 0 11-1.5 0V5.372A2.25 2.25 0 011.5 3.25zM11 2.5h-1V4h1a1 1 0 011 1v5.628a2.251 2.251 0 101.5 0V5A2.5 2.5 0 0011 2.5zm1 10.25a.75.75 0 111.5 0 .75.75 0 01-1.5 0zM3.75 12a.75.75 0 100 1.5.75.75 0 000-1.5z"/>
                    </svg>
                    <div class="metric-content">
                        <div class="metric-value">406</div>
                        <div class="metric-label">Pull Requests Opened</div>
                    </div>
                </div>
                
                <div class="metric-card">
                    <svg class="metric-icon" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 16 16" width="16" height="16">
                        <path fill="currentColor" d="M8 9.5a1.5 1.5 0 100-3 1.5 1.5 0 000 3z"/>
                        <path fill="currentColor" fill-rule="evenodd" d="M8 0a8 8 0 100 16A8 8 0 008 0zM1.5 8a6.5 6.5 0 1113 0 6.5 6.5 0 01-13 0z"/>
                    </svg>
                    <div class="metric-content">
                        <div class="metric-value">55</div>
                        <div class="metric-label">Issues Opened</div>
                    </div>
                </div>
            </div>
        </section>

        <!-- GitHub Stats Section -->
        <section class="section">
            <h2>GitHub Stats</h2>
            <div class="stats-container">
                <div class="stat-card">
                    <div class="stat-value">218</div>
                    <div class="stat-label">Repositories</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">15</div>
                    <div class="stat-label">Languages</div>
                </div>
                <div class="stat-card">
                    <div class="stat-value">3.96 GB</div>
                    <div class="stat-label">Storage Used</div>
                </div>
            </div>
        </section>

        <!-- Coding Habits Section -->
        <section class="section">
            <h2>Recent Coding Habits</h2>
            <p class="stat-label">(computed from last 90 commits)</p>
            <ul class="habits-list">
                <li>Uses spaces for indentation</li>
                <li>Has approximately 35.9 characters per line of code written</li>
                <li>Mostly pushes code around 15:00</li>
                <li>Mostly active on Monday</li>
            </ul>
        </section>

        <!-- Projects Section -->
        <section class="section">
            <h2>Featured Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h3 class="project-title">CitizenPath</h3>
                    <p>Immigration paperwork simplified with an intuitive platform.</p>
                    <a href="https://citizenpath.com/" class="project-link">citizenpath.com</a>
                </div>
                <div class="project-card">
                    <h3 class="project-title">MyZambeel Portal</h3>
                    <p>Portal for managing subscriptions and services.</p>
                    <a href="https://portal.myzambeel.com/login" class="project-link">portal.myzambeel.com</a>
                </div>
                <div class="project-card">
                    <h3 class="project-title">Moo.la</h3>
                    <p>URL shortener service with analytics.</p>
                    <a href="https://moo.la/" class="project-link">moo.la</a>
                </div>
                <div class="project-card">
                    <h3 class="project-title">Diligentsia UK</h3>
                    <p>Business consulting services website.</p>
                    <a href="https://diligentsia.co.uk/" class="project-link">diligentsia.co.uk</a>
                </div>
            </div>
        </section>
    </div>

    <footer>
        <p>Like what you see? Star some repos 💙</p>
    </footer>
</body>
</html>
