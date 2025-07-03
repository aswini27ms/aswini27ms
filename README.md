<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Aswini M S - GitHub Profile</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
            background: linear-gradient(135deg, #0a0a0a 0%, #1a1a2e 50%, #16213e 100%);
            color: #e2e8f0;
            line-height: 1.6;
            min-height: 100vh;
            overflow-x: hidden;
        }

        .container {
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
        }

        .header {
            text-align: center;
            margin-bottom: 50px;
            padding: 40px 0;
            background: linear-gradient(135deg, rgba(139, 92, 246, 0.1) 0%, rgba(59, 130, 246, 0.1) 100%);
            border-radius: 20px;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(255, 255, 255, 0.1);
            position: relative;
            overflow: hidden;
        }

        .header::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(45deg, transparent, rgba(139, 92, 246, 0.1), transparent);
            animation: shimmer 3s infinite;
        }

        @keyframes shimmer {
            0% { transform: translateX(-100%); }
            100% { transform: translateX(100%); }
        }

        .header h1 {
            font-size: 3.5rem;
            font-weight: 800;
            background: linear-gradient(135deg, #f59e0b, #ef4444, #8b5cf6, #06b6d4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            margin-bottom: 15px;
            z-index: 1;
            position: relative;
        }

        .header p {
            font-size: 1.3rem;
            color: #94a3b8;
            z-index: 1;
            position: relative;
        }

        .badges {
            display: flex;
            justify-content: center;
            gap: 10px;
            flex-wrap: wrap;
            margin-top: 20px;
            z-index: 1;
            position: relative;
        }

        .badge {
            background: linear-gradient(135deg, #8b5cf6, #06b6d4);
            color: white;
            padding: 8px 16px;
            border-radius: 20px;
            font-size: 0.9rem;
            font-weight: 600;
            text-decoration: none;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(139, 92, 246, 0.3);
        }

        .badge:hover {
            transform: translateY(-2px);
            box-shadow: 0 8px 25px rgba(139, 92, 246, 0.5);
        }

        .section {
            margin-bottom: 40px;
            background: rgba(30, 41, 59, 0.5);
            border-radius: 15px;
            padding: 30px;
            border: 1px solid rgba(255, 255, 255, 0.1);
            backdrop-filter: blur(10px);
            transition: all 0.3s ease;
        }

        .section:hover {
            transform: translateY(-5px);
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
            border-color: rgba(139, 92, 246, 0.3);
        }

        .section h3 {
            font-size: 1.8rem;
            margin-bottom: 20px;
            color: #f1f5f9;
            display: flex;
            align-items: center;
            gap: 10px;
        }

        .emoji {
            font-size: 2rem;
            filter: drop-shadow(0 0 10px rgba(139, 92, 246, 0.5));
        }

        .skill-category {
            margin-bottom: 15px;
        }

        .skill-title {
            font-weight: 700;
            color: #f59e0b;
            margin-bottom: 8px;
            font-size: 1.1rem;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .skill {
            background: linear-gradient(135deg, #374151, #4b5563);
            color: #e2e8f0;
            padding: 6px 12px;
            border-radius: 15px;
            font-size: 0.9rem;
            border: 1px solid rgba(139, 92, 246, 0.3);
            transition: all 0.3s ease;
        }

        .skill:hover {
            background: linear-gradient(135deg, #8b5cf6, #06b6d4);
            transform: scale(1.05);
            box-shadow: 0 4px 15px rgba(139, 92, 246, 0.4);
        }

        .project {
            background: linear-gradient(135deg, rgba(139, 92, 246, 0.1), rgba(59, 130, 246, 0.1));
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 20px;
            border: 1px solid rgba(139, 92, 246, 0.2);
            transition: all 0.3s ease;
        }

        .project:hover {
            transform: translateX(10px);
            box-shadow: 0 10px 30px rgba(139, 92, 246, 0.2);
        }

        .project h4 {
            font-size: 1.3rem;
            margin-bottom: 8px;
            color: #06b6d4;
        }

        .project-desc {
            color: #94a3b8;
            margin-bottom: 8px;
            font-style: italic;
        }

        .project-tech {
            color: #64748b;
            font-size: 0.9rem;
        }

        .achievement {
            background: linear-gradient(135deg, rgba(34, 197, 94, 0.1), rgba(59, 130, 246, 0.1));
            border-left: 4px solid #22c55e;
            padding: 15px;
            margin-bottom: 15px;
            border-radius: 0 10px 10px 0;
            transition: all 0.3s ease;
        }

        .achievement:hover {
            background: linear-gradient(135deg, rgba(34, 197, 94, 0.2), rgba(59, 130, 246, 0.2));
            transform: translateX(5px);
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-top: 30px;
        }

        .social-link {
            background: linear-gradient(135deg, #8b5cf6, #06b6d4);
            color: white;
            padding: 12px 24px;
            border-radius: 25px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s ease;
            box-shadow: 0 4px 15px rgba(139, 92, 246, 0.3);
        }

        .social-link:hover {
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(139, 92, 246, 0.5);
        }

        .motto {
            text-align: center;
            font-size: 1.2rem;
            font-style: italic;
            color: #94a3b8;
            margin: 40px 0;
            padding: 20px;
            background: linear-gradient(135deg, rgba(139, 92, 246, 0.1), rgba(59, 130, 246, 0.1));
            border-radius: 15px;
            border: 1px solid rgba(139, 92, 246, 0.2);
        }

        .footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            color: #64748b;
            font-size: 0.9rem;
        }

        .glow-text {
            text-shadow: 0 0 20px rgba(139, 92, 246, 0.5);
        }

        @media (max-width: 768px) {
            .header h1 {
                font-size: 2.5rem;
            }
            
            .container {
                padding: 10px;
            }
            
            .section {
                padding: 20px;
            }
            
            .badges {
                gap: 8px;
            }
            
            .social-links {
                flex-direction: column;
                align-items: center;
            }
        }

        .floating-elements {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            z-index: -1;
        }

        .floating-circle {
            position: absolute;
            border-radius: 50%;
            background: linear-gradient(135deg, rgba(139, 92, 246, 0.1), rgba(59, 130, 246, 0.1));
            animation: float 6s ease-in-out infinite;
        }

        .floating-circle:nth-child(1) {
            width: 100px;
            height: 100px;
            top: 20%;
            left: 10%;
            animation-delay: 0s;
        }

        .floating-circle:nth-child(2) {
            width: 150px;
            height: 150px;
            top: 60%;
            right: 10%;
            animation-delay: 2s;
        }

        .floating-circle:nth-child(3) {
            width: 80px;
            height: 80px;
            top: 40%;
            left: 80%;
            animation-delay: 4s;
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }
    </style>
</head>
<body>
    <div class="floating-elements">
        <div class="floating-circle"></div>
        <div class="floating-circle"></div>
        <div class="floating-circle"></div>
    </div>

    <div class="container">
        <div class="header">
            <h1 class="glow-text">👋 Hey, I'm Aswini M S</h1>
            <p><strong>Founder. Futurist. Full-stack Warlock.<br>
            I don't just build websites—I build realms.</strong></p>
            <div class="badges">
                <span class="badge">Founder - Script & Style</span>
                <span class="badge">Founder - Orivox</span>
                <span class="badge">NASA Space Apps Global Nominee</span>
                <span class="badge">Hackathon Explorer</span>
            </div>
        </div>

        <div class="section">
            <h3><span class="emoji">🎓</span> Profession / Current Role</h3>
            <p><strong>3rd Year B.E. Electrical and Electronics Engineering</strong> @ Sri Eshwar College of Engineering</p>
            <p><strong>Founder:</strong> Script & Style – Freelance Web Design Studio</p>
            <p><strong>Founder:</strong> Orivox – Innovating Futuristic Display & Embedded Tech</p>
            <p>Web Designer | Freelancer | Hackathon Explorer | Builder of Tech for Good</p>
        </div>

        <div class="section">
            <h3><span class="emoji">🔧</span> Top Skills & Technologies</h3>
            <div class="skill-category">
                <div class="skill-title">Frontend:</div>
                <div class="skills">
                    <span class="skill">React.js</span>
                    <span class="skill">Next.js</span>
                    <span class="skill">Tailwind CSS</span>
                    <span class="skill">DaisyUI</span>
                    <span class="skill">Framer Motion</span>
                </div>
            </div>
            <div class="skill-category">
                <div class="skill-title">Backend:</div>
                <div class="skills">
                    <span class="skill">Node.js</span>
                    <span class="skill">Express.js</span>
                    <span class="skill">MongoDB</span>
                    <span class="skill">Spring Boot</span>
                </div>
            </div>
            <div class="skill-category">
                <div class="skill-title">Full Stack:</div>
                <div class="skills">
                    <span class="skill">MERN Stack</span>
                    <span class="skill">REST APIs</span>
                    <span class="skill">Mongoose</span>
                    <span class="skill">JWT Auth</span>
                </div>
            </div>
            <div class="skill-category">
                <div class="skill-title">App Dev:</div>
                <div class="skills">
                    <span class="skill">Flutter</span>
                    <span class="skill">Firebase</span>
                </div>
            </div>
            <div class="skill-category">
                <div class="skill-title">Programming:</div>
                <div class="skills">
                    <span class="skill">Python</span>
                    <span class="skill">C</span>
                    <span class="skill">Java</span>
                </div>
            </div>
            <div class="skill-category">
                <div class="skill-title">Design/UX:</div>
                <div class="skills">
                    <span class="skill">Figma</span>
                    <span class="skill">Three.js</span>
                </div>
            </div>
            <div class="skill-category">
                <div class="skill-title">Data Tools:</div>
                <div class="skills">
                    <span class="skill">Power BI</span>
                    <span class="skill">Pandas</span>
                    <span class="skill">NumPy</span>
                    <span class="skill">Matplotlib</span>
                </div>
            </div>
        </div>

        <div class="section">
            <h3><span class="emoji">🌟</span> Notable Projects & Startups</h3>
            <div class="project">
                <h4>🚀 Script & Style</h4>
                <div class="project-desc">Freelance Web Design Studio – Building portfolios & websites for students/startups</div>
                <div class="project-tech">Founder | Full Stack Developer | UI/UX Designer | React.js • Tailwind • Firebase</div>
            </div>
            <div class="project">
                <h4>🪟 Orivox Transparent Display</h4>
                <div class="project-desc">Smart Display Technology – R&D for transparent LCD panels, futuristic interfaces</div>
                <div class="project-tech">Founder | Embedded Tech & Product Design | Embedded Systems</div>
            </div>
            <div class="project">
                <h4>🌐 Developer Community Forum</h4>
                <div class="project-desc">Collaboration space for aspiring developers</div>
                <div class="project-tech">Community Building & Collaboration</div>
            </div>
            <div class="project">
                <h4>🌍 Clima360</h4>
                <div class="project-desc">NASA Space App Challenge Project – Interactive Power BI dashboards for climate data</div>
                <div class="project-tech">Global Nominee (Top 947 teams) – NASA Space Apps 2024</div>
            </div>
            <div class="project">
                <h4>🛟 DCON</h4>
                <div class="project-desc">LoRa-based disaster communication app for NGOs/aid providers</div>
                <div class="project-tech">Hackfest @ SSN College</div>
            </div>
            <div class="project">
                <h4>🍏 Healthify Me</h4>
                <div class="project-desc">Diet & wellness app using Edamam API</div>
                <div class="project-tech">Internal Hackathon Finalist</div>
            </div>
        </div>

        <div class="section">
            <h3><span class="emoji">🏆</span> Achievements & Recognitions</h3>
            <div class="achievement">🥇 <strong>First Rank Holder</strong> (2 years, EEE Dept)</div>
            <div class="achievement">🚀 <strong>Founder</strong> – Script & Style & Orivox</div>
            <div class="achievement">🌍 <strong>NASA Space App Challenge – Global Nominee</strong></div>
            <div class="achievement">🪟 <strong>Built transparent display prototype</strong> (Orivox)</div>
            <div class="achievement">🎓 <strong>Participant</strong> – Hackfest @ SSN & E-Summit @ IIT Madras</div>
            <div class="achievement">🥇 <strong>1st Place</strong> – Mini Project (Dept level)</div>
            <div class="achievement">🏅 <strong>6th Place</strong> – College Hackathon</div>
            <div class="achievement">📊 <strong>Balanced high academic performance with project leadership</strong></div>
        </div>

        <div class="section">
            <h3><span class="emoji">🧠</span> Interests & Passions</h3>
            <p>🚀 Startup Ideation & Building Futuristic Tech</p>
            <p>🌌 Passionate about Astrobiology, Space Science, and Sci-fi Research</p>
            <p>🏏 Hardcore Cricket Lover</p>
        </div>

        <div class="section">
            <h3><span class="emoji">🔗</span> Let's Connect</h3>
            <div class="social-links">
                <a href="https://www.linkedin.com/in/aswini-m-s-8b10a8310/" class="social-link">LinkedIn</a>
                <a href="https://github.com/aswini27ms" class="social-link">GitHub</a>
                <a href="mailto:aswini.ms2023eee@sece.ac.in" class="social-link">Email</a>
            </div>
        </div>

        <div class="motto">
            <p>"Where creativity meets code, innovation begins—and that's where I thrive."</p>
        </div>

        <div class="footer">
            <p>⚡ Always open to connect, collaborate & create something magical!</p>
        </div>
    </div>
</body>
</html>
