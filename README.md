<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tani's GitHub Profile</title>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', 'Segoe UI', system-ui, sans-serif;
            background: radial-gradient(ellipse at top, #0f1629 0%, #0a0d14 50%, #05080c 100%);
            color: #e8eaed;
            line-height: 1.7;
            padding: 2rem;
            min-height: 100vh;
            position: relative;
            overflow-x: hidden;
        }

        body::before {
            content: '';
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: 
                radial-gradient(circle at 20% 80%, rgba(33, 150, 243, 0.15) 0%, transparent 50%),
                radial-gradient(circle at 80% 20%, rgba(3, 169, 244, 0.1) 0%, transparent 50%),
                radial-gradient(circle at 40% 40%, rgba(25, 118, 210, 0.08) 0%, transparent 50%);
            pointer-events: none;
            z-index: 0;
        }

        .container {
            max-width: 1400px;
            margin: 0 auto;
            background: rgba(15, 22, 41, 0.95);
            backdrop-filter: blur(20px);
            border-radius: 24px;
            border: 1px solid rgba(33, 150, 243, 0.2);
            overflow: hidden;
            box-shadow: 
                0 32px 64px rgba(0, 0, 0, 0.4),
                0 0 0 1px rgba(33, 150, 243, 0.1),
                inset 0 1px 0 rgba(255, 255, 255, 0.05);
            position: relative;
            z-index: 1;
        }

        .header {
            text-align: center;
            padding: 4rem 2rem;
            background: linear-gradient(135deg, #1e3a8a 0%, #1565c0 25%, #0288d1 50%, #0277bd 75%, #01579b 100%);
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
            background: 
                linear-gradient(45deg, transparent 48%, rgba(255, 255, 255, 0.03) 49%, rgba(255, 255, 255, 0.03) 51%, transparent 52%),
                radial-gradient(circle at 30% 70%, rgba(255, 255, 255, 0.1) 0%, transparent 50%);
            animation: shimmer 8s ease-in-out infinite;
        }

        @keyframes shimmer {
            0%, 100% { opacity: 0.5; }
            50% { opacity: 1; }
        }

        .header-content {
            position: relative;
            z-index: 1;
        }

        .avatar {
            width: 140px;
            height: 140px;
            border-radius: 50%;
            background: linear-gradient(135deg, #2196f3 0%, #03a9f4 50%, #00bcd4 100%);
            margin: 0 auto 1.5rem;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 3.5rem;
            font-weight: 700;
            color: white;
            box-shadow: 
                0 20px 40px rgba(33, 150, 243, 0.3),
                0 0 0 4px rgba(255, 255, 255, 0.1),
                inset 0 2px 0 rgba(255, 255, 255, 0.2);
            animation: float 6s ease-in-out infinite;
            position: relative;
        }

        .avatar::after {
            content: '';
            position: absolute;
            top: -2px;
            left: -2px;
            right: -2px;
            bottom: -2px;
            background: linear-gradient(45deg, #2196f3, #03a9f4, #00bcd4, #2196f3);
            border-radius: 50%;
            z-index: -1;
            animation: rotate 4s linear infinite;
            opacity: 0.7;
        }

        @keyframes rotate {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }

        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-12px); }
        }

        .name {
            font-size: 3rem;
            font-weight: 800;
            margin-bottom: 0.8rem;
            color: white;
            text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.4);
            letter-spacing: -0.02em;
        }

        .title {
            font-size: 1.4rem;
            color: rgba(255, 255, 255, 0.95);
            margin-bottom: 1.5rem;
            font-weight: 500;
        }

        .contact-info {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 2rem;
        }

        .contact-item {
            color: white;
            text-decoration: none;
            display: flex;
            align-items: center;
            gap: 0.8rem;
            padding: 0.8rem 1.5rem;
            background: rgba(255, 255, 255, 0.15);
            border-radius: 50px;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            font-weight: 600;
            border: 1px solid rgba(255, 255, 255, 0.2);
            backdrop-filter: blur(10px);
        }

        .contact-item:hover {
            background: rgba(255, 255, 255, 0.25);
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 12px 24px rgba(33, 150, 243, 0.3);
        }

        .content {
            padding: 3rem 2rem;
        }

        .quote {
            background: linear-gradient(135deg, rgba(33, 150, 243, 0.15), rgba(3, 169, 244, 0.1));
            border-left: 4px solid #2196f3;
            padding: 2rem;
            margin: 3rem 0;
            border-radius: 0 16px 16px 0;
            font-style: italic;
            position: relative;
            font-size: 1.1rem;
            line-height: 1.8;
            backdrop-filter: blur(10px);
            border: 1px solid rgba(33, 150, 243, 0.2);
        }

        .quote::before {
            content: '"';
            font-size: 5rem;
            color: #2196f3;
            position: absolute;
            top: -20px;
            left: 20px;
            opacity: 0.4;
            font-family: Georgia, serif;
        }

        .section {
            margin: 4rem 0;
        }

        .section-title {
            font-size: 2.2rem;
            font-weight: 700;
            margin-bottom: 2rem;
            color: #2196f3;
            display: flex;
            align-items: center;
            gap: 1rem;
            position: relative;
        }

        .section-title::after {
            content: '';
            flex: 1;
            height: 2px;
            background: linear-gradient(90deg, #2196f3, transparent);
            margin-left: 1rem;
        }

        .section-title i {
            font-size: 1.8rem;
            background: linear-gradient(135deg, #2196f3, #03a9f4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 2rem;
            margin-top: 2.5rem;
        }

        .skill-category {
            background: linear-gradient(135deg, rgba(33, 150, 243, 0.08), rgba(3, 169, 244, 0.05));
            border-radius: 20px;
            padding: 2rem;
            border: 1px solid rgba(33, 150, 243, 0.2);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
            backdrop-filter: blur(10px);
        }

        .skill-category::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, rgba(33, 150, 243, 0.1), transparent);
            opacity: 0;
            transition: opacity 0.4s ease;
        }

        .skill-category:hover::before {
            opacity: 1;
        }

        .skill-category:hover {
            transform: translateY(-8px);
            box-shadow: 
                0 24px 48px rgba(33, 150, 243, 0.2),
                0 0 0 1px rgba(33, 150, 243, 0.3);
        }

        .skill-category h3 {
            color: #2196f3;
            font-size: 1.4rem;
            margin-bottom: 1.5rem;
            display: flex;
            align-items: center;
            gap: 0.8rem;
            font-weight: 700;
            position: relative;
            z-index: 1;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.8rem;
            position: relative;
            z-index: 1;
        }

        .skill-tag {
            background: linear-gradient(135deg, #1565c0, #1976d2, #1e88e5);
            color: white;
            padding: 0.6rem 1.2rem;
            border-radius: 25px;
            font-size: 0.9rem;
            font-weight: 600;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            border: 1px solid rgba(255, 255, 255, 0.2);
            box-shadow: 0 4px 12px rgba(33, 150, 243, 0.2);
            position: relative;
            overflow: hidden;
        }

        .skill-tag::before {
            content: '';
            position: absolute;
            top: 0;
            left: -100%;
            width: 100%;
            height: 100%;
            background: linear-gradient(90deg, transparent, rgba(255, 255, 255, 0.3), transparent);
            transition: left 0.5s ease;
        }

        .skill-tag:hover::before {
            left: 100%;
        }

        .skill-tag:hover {
            transform: translateY(-3px) scale(1.05);
            box-shadow: 0 8px 20px rgba(33, 150, 243, 0.4);
            background: linear-gradient(135deg, #1976d2, #2196f3, #42a5f5);
        }

        .tech-icons {
            display: flex;
            flex-wrap: wrap;
            gap: 1.5rem;
            justify-content: center;
            margin: 3rem 0;
            padding: 3rem;
            background: linear-gradient(135deg, rgba(33, 150, 243, 0.05), rgba(3, 169, 244, 0.03));
            border-radius: 20px;
            border: 1px solid rgba(33, 150, 243, 0.1);
            backdrop-filter: blur(10px);
        }

        .tech-icon {
            width: 70px;
            height: 70px;
            background: linear-gradient(135deg, rgba(33, 150, 243, 0.1), rgba(3, 169, 244, 0.05));
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            font-size: 2.2rem;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            border: 1px solid rgba(33, 150, 243, 0.2);
            position: relative;
            overflow: hidden;
        }

        .tech-icon::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(33, 150, 243, 0.2) 0%, transparent 70%);
            opacity: 0;
            transition: opacity 0.4s ease;
        }

        .tech-icon:hover::before {
            opacity: 1;
        }

        .tech-icon:hover {
            transform: translateY(-8px) scale(1.15) rotate(5deg);
            background: linear-gradient(135deg, rgba(33, 150, 243, 0.2), rgba(3, 169, 244, 0.15));
            box-shadow: 
                0 16px 32px rgba(33, 150, 243, 0.3),
                0 0 0 2px rgba(33, 150, 243, 0.4);
        }

        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 2rem;
            margin-top: 2.5rem;
        }

        .stat-card {
            background: linear-gradient(135deg, rgba(33, 150, 243, 0.08), rgba(3, 169, 244, 0.05));
            border-radius: 20px;
            padding: 2rem;
            text-align: center;
            border: 1px solid rgba(33, 150, 243, 0.2);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
            backdrop-filter: blur(10px);
        }

        .stat-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(135deg, rgba(33, 150, 243, 0.1), transparent);
            opacity: 0;
            transition: opacity 0.4s ease;
        }

        .stat-card:hover::before {
            opacity: 1;
        }

        .stat-card:hover {
            transform: translateY(-8px);
            box-shadow: 0 20px 40px rgba(33, 150, 243, 0.2);
        }

        .stat-number {
            font-size: 2.5rem;
            font-weight: bold;
            color: #2196f3;
            margin-bottom: 0.8rem;
            position: relative;
            z-index: 1;
        }

        .about-section {
            background: linear-gradient(135deg, rgba(33, 150, 243, 0.05), rgba(3, 169, 244, 0.03));
            border-radius: 20px;
            padding: 2.5rem;
            margin: 3rem 0;
            border: 1px solid rgba(33, 150, 243, 0.15);
            backdrop-filter: blur(10px);
        }

        .about-section p {
            font-size: 1.1rem;
            margin-bottom: 1rem;
            display: flex;
            align-items: center;
            gap: 1rem;
        }

        .footer {
            text-align: center;
            padding: 3rem 2rem;
            background: linear-gradient(135deg, rgba(33, 150, 243, 0.08), rgba(3, 169, 244, 0.05));
            color: rgba(255, 255, 255, 0.8);
            border-top: 1px solid rgba(33, 150, 243, 0.2);
            font-size: 1.1rem;
        }

        .footer p {
            margin: 0.5rem 0;
            font-weight: 500;
        }

        @keyframes ripple {
            to {
                transform: scale(2);
                opacity: 0;
            }
        }

        @keyframes particle {
            0% {
                transform: translateY(0) scale(1);
                opacity: 1;
            }
            100% {
                transform: translateY(-20px) scale(0);
                opacity: 0;
            }
        }

        @media (max-width: 768px) {
            .skills-grid {
                grid-template-columns: 1fr;
            }
            
            .contact-info {
                flex-direction: column;
                align-items: center;
                gap: 1rem;
            }
            
            .tech-icons {
                gap: 1rem;
                padding: 2rem;
            }
            
            .tech-icon {
                width: 60px;
                height: 60px;
                font-size: 1.8rem;
            }

            .name {
                font-size: 2.5rem;
            }

            .section-title {
                font-size: 1.8rem;
            }
        }

        /* Smooth scroll and enhanced animations */
        html {
            scroll-behavior: smooth;
        }

        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: all 0.8s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="header-content">
                <div class="avatar">T</div>
                <h1 class="name">Hello, I'm Tani ツ</h1>
                <p class="title">🌱 Dedicated, Self-Driven Full-Stack Software Engineer</p>
                <div class="contact-info">
                    <a href="mailto:ifegbesan6@gmail.com" class="contact-item">
                        <i class="fas fa-envelope"></i>
                        Get In Touch
                    </a>
                    <a href="#" class="contact-item">
                        <i class="fab fa-github"></i>
                        GitHub
                    </a>
                    <a href="#" class="contact-item">
                        <i class="fab fa-linkedin"></i>
                        LinkedIn
                    </a>
                </div>
            </div>
        </div>

        <div class="content">
            <div class="quote fade-in">
                Software, like all technologies, is a powerful expression of our values and visions.
                Code inevitably reflects the choices, biases, and desires of its creators, 
                shaping the future we collectively build.
            </div>

            <div class="section fade-in">
                <h2 class="section-title">
                    <i class="fas fa-rocket"></i>
                    About Me
                </h2>
                <div class="about-section">
                    <p><span style="font-size: 1.5rem;">❤️</span> I'm open to collaboration on any interesting and/or open-source projects</p>
                    <p><span style="font-size: 1.5rem;">💬</span> Always excited to discuss new technologies, innovative solutions, and impactful projects</p>
                    <p><span style="font-size: 1.5rem;">🚀</span> Passionate about building scalable, efficient, and cutting-edge software solutions</p>
                </div>
            </div>

            <div class="section fade-in">
                <h2 class="section-title">
                    <i class="fas fa-code"></i>
                    Technical Arsenal
                </h2>
                
                <div class="tech-icons">
                    <div class="tech-icon" style="color: #f7df1e;" title="JavaScript"><i class="fab fa-js-square"></i></div>
                    <div class="tech-icon" style="color: #3178c6;" title="TypeScript"><i class="fab fa-js-square"></i></div>
                    <div class="tech-icon" style="color: #3776ab;" title="Python"><i class="fab fa-python"></i></div>
                    <div class="tech-icon" style="color: #61dafb;" title="React"><i class="fab fa-react"></i></div>
                    <div class="tech-icon" style="color: #68217a;" title=".NET"><i class="fab fa-microsoft"></i></div>
                    <div class="tech-icon" style="color: #339933;" title="Node.js"><i class="fab fa-node-js"></i></div>
                    <div class="tech-icon" style="color: #ff9900;" title="AWS"><i class="fab fa-aws"></i></div>
                    <div class="tech-icon" style="color: #0db7ed;" title="Docker"><i class="fab fa-docker"></i></div>
                    <div class="tech-icon" style="color: #fcc624;" title="Linux"><i class="fab fa-linux"></i></div>
                    <div class="tech-icon" style="color: #2196f3;" title="Database"><i class="fas fa-database"></i></div>
                    <div class="tech-icon" style="color: #4caf50;" title="MongoDB"><i class="fas fa-leaf"></i></div>
                    <div class="tech-icon" style="color: #e535ab;" title="GraphQL"><i class="fas fa-project-diagram"></i></div>
                </div>

                <div class="skills-grid">
                    <div class="skill-category fade-in">
                        <h3><i class="fas fa-code"></i> Programming Languages</h3>
                        <div class="skill-tags">
                            <span class="skill-tag">Python</span>
                            <span class="skill-tag">TypeScript</span>
                            <span class="skill-tag">JavaScript</span>
                            <span class="skill-tag">C#</span>
                            <span class="skill-tag">Go</span>
                        </div>
                    </div>

                    <div class="skill-category fade-in">
                        <h3><i class="fas fa-layer-group"></i> Frameworks & Libraries</h3>
                        <div class="skill-tags">
                            <span class="skill-tag">FastAPI</span>
                            <span class="skill-tag">Django</span>
                            <span class="skill-tag">Node.js</span>
                            <span class="skill-tag">.NET</span>
                            <span class="skill-tag">Gin</span>
                            <span class="skill-tag">Web3.js</span>
                            <span class="skill-tag">React</span>
                            <span class="skill-tag">Angular</span>
                        </div>
                    </div>

                    <div class="skill-category fade-in">
                        <h3><i class="fas fa-database"></i> Tools & Technologies</h3>
                        <div class="skill-tags">
                            <span class="skill-tag">PostgreSQL</span>
                            <span class="skill-tag">MongoDB</span>
                            <span class="skill-tag">Redis</span>
                            <span class="skill-tag">SQLAlchemy</span>
                            <span class="skill-tag">GraphQL</span>
                            <span class="skill-tag">gRPC</span>
                            <span class="skill-tag">Kubernetes</span>
                            <span class="skill-tag">CI/CD</span>
                            <span class="skill-tag">Terraform</span>
                            <span class="skill-tag">Prometheus</span>
                            <span class="skill-tag">Grafana</span>
                            <span class="skill-tag">Kafka</span>
                        </div>
                    </div>

                    <div class="skill-category fade-in">
                        <h3><i class="fas fa-cogs"></i> DevOps & Infrastructure</h3>
                        <div class="skill-tags">
                            <span class="skill-tag">Docker</span>
                            <span class="skill-tag">Kubernetes</span>
                            <span class="skill-tag">Terraform</span>
                            <span class="skill-tag">CI/CD Pipelines</span>
                            <span class="skill-tag">Prometheus</span>
                            <span class="skill-tag">Grafana</span>
                            <span class="skill-tag">Kafka</span>
                            <span class="skill-tag">Monitoring & Logging</span>
                        </div>
                    </div>

                    <div class="skill-category fade-in">
                        <h3><i class="fas fa-cloud"></i> Cloud Platforms</h3>
                        <div class="skill-tags">
                            <span class="skill-tag">AWS S3</span>
                            <span class="skill-tag">AWS EC2</span>
                            <span class="skill-tag">AWS VPC</span>
                            <span class="skill-tag">AWS Athena</span>
                            <span class="skill-tag">AWS Glue</span>
                            <span class="skill-tag">AWS IAM</span>
                            <span class="skill-tag">AWS RDS</span>
                            <span class="skill-tag">AWS RedShift</span>
                            <span class="skill-tag">AWS SQS</span>
                            <span class="skill-tag">GCP Cloud Functions</span>
                            <span class="skill-tag">GCP Cloud Storage</span>
                            <span class="skill-tag">GCP Compute Engine</span>
                            <span class="skill-tag">Azure</span>
                        </div>
                    </div>

                    <div class="skill-category fade-in">
                        <h3><i class="fas fa-brain"></i> Technical Skills & Concepts</h3>
                        <div class="skill-tags">
                            <span class="skill-tag">Data Structures & Algorithms</span>
                            <span class="skill-tag">Microservices Architecture</span>
                            <span class="skill-tag">Test-Driven Development</span>
                            <span class="skill-tag">RAG (Retrieval-Augmented Generation)</span>
                            <span class="skill-tag">ETL Pipelines</span>
                            <span class="skill-tag">Distributed Systems</span>
                            <span class="skill-tag">Networking</span>
                            <span class="skill-tag">Blockchain Technology</span>
                            <span class="skill-tag">System Design</span>
                            <span class="skill-tag">API Development</span>
                        </div>
                    </div>
                </div>
            </div>

            <div class="section fade-in">
                <h2 class="section-title">
                    <i class="fas fa-chart-line"></i>
                    GitHub Analytics
                </h2>
                <div class="stats-grid">
                    <div class="stat-card">
                        <div class="stat-number">🔥</div>
                        <p><strong>Contribution Streak</strong></p>
                        <small>Consistent daily commits</small>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">📊</div>
                        <p><strong>Code Statistics</strong></p>
                        <small>Languages & commits</small>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">🌟</div>
                        <p><strong>Repository Insights</strong></p>
                        <small>Stars & contributions</small>
                    </div>
                    <div class="stat-card">
                        <div class="stat-number">🚀</div>
                        <p><strong>Project Impact</strong></p>
                        <small>Open source contributions</small>
                    </div>
                </div>
            </div>
        </div>

        <div class="footer">
            <p>💼 <strong>Open to exciting collaborations and innovative projects</strong></p>
            <p>🚀 <strong>Let's build something extraordinary together!</strong></p>
            <p>📧 Ready to discuss your next big idea? Drop me a line!</p>
        </div>
    </div>

    <script>
        // Enhanced animations and interactions
        document.addEventListener('DOMContentLoaded', function() {
            // Intersection Observer for fade-in animations
            const observerOptions = {
                threshold: 0.1,
                rootMargin: '0px 0px -50px 0px'
            };

            const observer = new IntersectionObserver(function(entries) {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.classList.add('visible');
                    }
                });
            }, observerOptions);

            // Observe all fade-in elements
            document.querySelectorAll('.fade-in').forEach(el => {
                observer.observe(el);
            });

            // Enhanced tech icon interactions
            document.querySelectorAll('.tech-icon').forEach(icon => {
                icon.addEventListener('mouseenter', function() {
                    this.style.transform = 'translateY(-8px) scale(1.15) rotate(5deg)';
                    
                    // Create a ripple effect
                    const ripple = document.createElement('div');
                    ripple.style.cssText = `
                        position: absolute;
                        border-radius: 50%;
                        background: rgba(33, 150, 243, 0.3);
                        transform: scale(0);
                        animation: ripple 0.6s linear;
                        left: 50%;
                        top: 50%;
                        width: 100px;
                        height: 100px;
                        margin-left: -50px;
                        margin-top: -50px;
                        pointer-events: none;
                    `;
                    
                    this.appendChild(ripple);
                    
                    setTimeout(() => {
                        ripple.remove();
                    }, 600);
                });
                
                icon.addEventListener('mouseleave', function() {
                    this.style.transform = '';
                });
            });

            // Enhanced skill tag interactions with particle effects
            document.querySelectorAll('.skill-tag').forEach(tag => {
                tag.addEventListener('mouseenter', function(e) {
                    // Create floating particles
                    for (let i = 0; i < 3; i++) {
                        setTimeout(() => {
                            const particle = document.createElement('div');
                            particle.style.cssText = `
                                position: absolute;
                                width: 4px;
                                height: 4px;
                                background: #2196f3;
                                border-radius: 50%;
                                pointer-events: none;
                                animation: particle 1s ease-out forwards;
                                left: ${Math.random() * 100}%;
                                top: 100%;
                                z-index: 10;
                            `;
                            
                            this.appendChild(particle);
                            
                            setTimeout(() => {
                                particle.remove();
                            }, 1000);
                        }, i * 100);
                    }
                });
            });

            // Enhanced contact item interactions
            document.querySelectorAll('.contact-item').forEach(item => {
                item.addEventListener('click', function(e) {
                    // Create expanding ring effect
                    const ring = document.createElement('div');
                    ring.style.cssText = `
                        position: absolute;
                        border: 2px solid rgba(255, 255, 255, 0.6);
                        border-radius: 50%;
                        transform: scale(0);
                        animation: ripple 0.8s ease-out;
                        left: 50%;
                        top: 50%;
                        width: 100px;
                        height: 100px;
                        margin-left: -50px;
                        margin-top: -50px;
                        pointer-events: none;
                    `;
                    
                    this.style.position = 'relative';
                    this.appendChild(ring);
                    
                    setTimeout(() => {
                        ring.remove();
                    }, 800);
                });
            });

            // Smooth scrolling for any internal links
            document.querySelectorAll('a[href^="#"]').forEach(anchor => {
                anchor.addEventListener('click', function (e) {
                    e.preventDefault();
                    const target = document.querySelector(this.getAttribute('href'));
                    if (target) {
                        target.scrollIntoView({
                            behavior: 'smooth',
                            block: 'start'
                        });
                    }
                });
            });

            // Add dynamic background particles
            function createBackgroundParticles() {
                const container = document.body;
                
                setInterval(() => {
                    const particle = document.createElement('div');
                    particle.style.cssText = `
                        position: fixed;
                        width: 2px;
                        height: 2px;
                        background: rgba(33, 150, 243, 0.3);
                        border-radius: 50%;
                        pointer-events: none;
                        left: ${Math.random() * 100}vw;
                        top: 100vh;
                        z-index: 0;
                        animation: floatUp 8s linear forwards;
                    `;
                    
                    container.appendChild(particle);
                    
                    setTimeout(() => {
                        particle.remove();
                    }, 8000);
                }, 2000);
            }

            // Add CSS for floating particles
            const style = document.createElement('style');
            style.textContent = `
                @keyframes floatUp {
                    to {
                        transform: translateY(-100vh) rotate(360deg);
                        opacity: 0;
                    }
                }
            `;
            document.head.appendChild(style);

            // Start background particles
            createBackgroundParticles();

            // Add typing effect to the name
            const nameElement = document.querySelector('.name');
            const originalText = nameElement.textContent;
            nameElement.textContent = '';
            
            let i = 0;
            const typeWriter = () => {
                if (i < originalText.length) {
                    nameElement.textContent += originalText.charAt(i);
                    i++;
                    setTimeout(typeWriter, 100);
                }
            };
            
            setTimeout(typeWriter, 1000);
        });
    </script>
</body>
</html>
