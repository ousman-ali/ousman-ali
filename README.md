<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Ousman Ali Seid - Full-Stack Developer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    <style>
        :root {
            --primary: #6C63FF;
            --secondary: #4A44C6;
            --dark: #2A2A3C;
            --light: #F5F5F7;
            --accent: #FF6584;
            --success: #36D1DC;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #0f0c29, #302b63, #24243e);
            color: var(--light);
            line-height: 1.6;
            padding: 2rem;
            min-height: 100vh;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
        }
        
        /* Header Styles */
        .header {
            text-align: center;
            margin-bottom: 3rem;
            animation: fadeIn 1s ease-out;
        }
        
        .profile-img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            object-fit: cover;
            border: 4px solid var(--primary);
            box-shadow: 0 10px 30px rgba(108, 99, 255, 0.3);
            margin-bottom: 1.5rem;
            animation: float 6s ease-in-out infinite;
        }
        
        .name {
            font-size: 2.5rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            background: linear-gradient(90deg, var(--primary), var(--success));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .tagline {
            font-size: 1.2rem;
            color: #B8B8D1;
            margin-bottom: 1.5rem;
        }
        
        /* Card Styles */
        .card {
            background: rgba(42, 42, 60, 0.7);
            backdrop-filter: blur(10px);
            border-radius: 16px;
            padding: 1.5rem;
            margin-bottom: 2rem;
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            border: 1px solid rgba(255, 255, 255, 0.1);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            animation: slideUp 0.8s ease-out;
        }
        
        .card:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 40px rgba(108, 99, 255, 0.3);
        }
        
        .card-title {
            font-size: 1.5rem;
            margin-bottom: 1.2rem;
            color: var(--primary);
            display: flex;
            align-items: center;
            gap: 10px;
        }
        
        .card-title i {
            font-size: 1.3rem;
        }
        
        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 1.5rem;
        }
        
        .skill-category {
            margin-bottom: 1.5rem;
        }
        
        .skill-category h3 {
            font-size: 1.2rem;
            margin-bottom: 0.8rem;
            color: var(--success);
        }
        
        .tech-icons {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }
        
        .tech-icon {
            width: 50px;
            height: 50px;
            display: flex;
            align-items: center;
            justify-content: center;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 10px;
            transition: all 0.3s ease;
        }
        
        .tech-icon:hover {
            background: var(--primary);
            transform: scale(1.1);
        }
        
        .tech-icon img {
            width: 30px;
            height: 30px;
        }
        
        /* Experience Section */
        .experience-item {
            margin-bottom: 1.5rem;
            padding-bottom: 1.5rem;
            border-bottom: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .experience-item:last-child {
            border-bottom: none;
        }
        
        .experience-title {
            font-size: 1.2rem;
            margin-bottom: 0.5rem;
            color: var(--light);
        }
        
        .experience-desc {
            color: #B8B8D1;
            margin-bottom: 0.8rem;
        }
        
        .feature-list {
            list-style-type: none;
            padding-left: 1rem;
        }
        
        .feature-list li {
            margin-bottom: 0.5rem;
            position: relative;
        }
        
        .feature-list li:before {
            content: "▹";
            color: var(--primary);
            position: absolute;
            left: -1rem;
        }
        
        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 1.5rem;
        }
        
        .project-card {
            background: rgba(42, 42, 60, 0.9);
            border-radius: 12px;
            padding: 1.5rem;
            transition: all 0.3s ease;
            border: 1px solid rgba(255, 255, 255, 0.1);
        }
        
        .project-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 25px rgba(108, 99, 255, 0.2);
        }
        
        .project-title {
            font-size: 1.2rem;
            margin-bottom: 0.8rem;
            color: var(--light);
            display: flex;
            align-items: center;
            gap: 8px;
        }
        
        .project-title i {
            color: var(--accent);
        }
        
        .project-tech {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 1rem;
        }
        
        .tech-tag {
            background: rgba(108, 99, 255, 0.2);
            color: var(--primary);
            padding: 4px 10px;
            border-radius: 20px;
            font-size: 0.8rem;
        }
        
        .project-desc {
            color: #B8B8D1;
            font-size: 0.9rem;
        }
        
        /* Learning Section */
        .learning-items {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
        }
        
        .learning-item {
            background: rgba(54, 209, 220, 0.1);
            padding: 10px 15px;
            border-radius: 8px;
            display: flex;
            align-items: center;
            gap: 8px;
            transition: all 0.3s ease;
        }
        
        .learning-item:hover {
            background: rgba(54, 209, 220, 0.2);
            transform: translateY(-3px);
        }
        
        .learning-item i {
            color: var(--success);
        }
        
        /* Contact Section */
        .contact-links {
            display: flex;
            justify-content: center;
            gap: 1.5rem;
            margin-top: 1.5rem;
        }
        
        .contact-link {
            display: flex;
            align-items: center;
            gap: 8px;
            padding: 10px 20px;
            background: rgba(108, 99, 255, 0.2);
            border-radius: 8px;
            color: var(--light);
            text-decoration: none;
            transition: all 0.3s ease;
        }
        
        .contact-link:hover {
            background: var(--primary);
            transform: translateY(-3px);
        }
        
        /* Animations */
        @keyframes fadeIn {
            from { opacity: 0; }
            to { opacity: 1; }
        }
        
        @keyframes slideUp {
            from { 
                opacity: 0;
                transform: translateY(30px);
            }
            to { 
                opacity: 1;
                transform: translateY(0);
            }
        }
        
        @keyframes float {
            0% { transform: translateY(0px); }
            50% { transform: translateY(-15px); }
            100% { transform: translateY(0px); }
        }
        
        /* Responsive Design */
        @media (max-width: 768px) {
            .skills-grid, .projects-grid {
                grid-template-columns: 1fr;
            }
            
            .contact-links {
                flex-direction: column;
                align-items: center;
            }
            
            .name {
                font-size: 2rem;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <!-- Header Section -->
        <header class="header">
            <img src="https://avatars.githubusercontent.com/u/12345678?v=4" alt="Ousman Ali Seid" class="profile-img">
            <h1 class="name">Ousman Ali Seid</h1>
            <p class="tagline">Full-Stack Developer | MERN & Laravel Expert | Always Learning & Exploring</p>
            <div class="contact-links">
                <a href="https://ousman-portfolio.vercel.app/" class="contact-link">
                    <i class="fas fa-globe"></i> Portfolio
                </a>
                <a href="https://github.com/ousman" class="contact-link">
                    <i class="fab fa-github"></i> GitHub
                </a>
                <a href="https://linkedin.com/in/ousman" class="contact-link">
                    <i class="fab fa-linkedin"></i> LinkedIn
                </a>
            </div>
        </header>
        
        <!-- About Section -->
        <section class="card">
            <h2 class="card-title"><i class="fas fa-user"></i> About Me</h2>
            <p>I'm a passionate full-stack developer who loves building real-world applications that solve meaningful problems. Curiosity drives me — I'm always eager to learn, discover, and create using modern technologies across frontend, backend, and mobile development.</p>
        </section>
        
        <!-- Skills Section -->
        <section class="card">
            <h2 class="card-title"><i class="fas fa-code"></i> Skills & Technologies</h2>
            <div class="skills-grid">
                <div class="skill-category">
                    <h3>Frontend</h3>
                    <div class="tech-icons">
                        <div class="tech-icon">
                            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/react/react-original.svg" alt="React">
                        </div>
                        <div class="tech-icon">
                            <img src="https://skillicons.dev/icons?i=nextjs" alt="Next.js">
                        </div>
                        <div class="tech-icon">
                            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/flutter/flutter-original.svg" alt="Flutter">
                        </div>
                        <div class="tech-icon">
                            <img src="https://skillicons.dev/icons?i=javascript" alt="JavaScript">
                        </div>
                        <div class="tech-icon">
                            <img src="https://skillicons.dev/icons?i=html" alt="HTML">
                        </div>
                        <div class="tech-icon">
                            <img src="https://skillicons.dev/icons?i=css" alt="CSS">
                        </div>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>Backend</h3>
                    <div class="tech-icons">
                        <div class="tech-icon">
                            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/laravel/laravel-plain-wordmark.svg" alt="Laravel">
                        </div>
                        <div class="tech-icon">
                            <img src="https://raw.githubusercontent.com/devicons/devicon/master/icons/nodejs/nodejs-original.svg" alt="Node.js">
                        </div>
                        <div class="tech-icon">
                            <img src="https://skillicons.dev/icons?i=express" alt="Express">
                        </div>
                        <div class="tech-icon">
                            <img src="https://skillicons.dev/icons?i=mongodb" alt="MongoDB">
                        </div>
                        <div class="tech-icon">
                            <img src="https://skillicons.dev/icons?i=mysql" alt="MySQL">
                        </div>
                    </div>
                </div>
                
                <div class="skill-category">
                    <h3>Tools & Others</h3>
                    <div class="tech-icons">
                        <div class="tech-icon">
                            <img src="https://skillicons.dev/icons?i=git" alt="Git">
                        </div>
                        <div class="tech-icon">
                            <img src="https://skillicons.dev/icons?i=docker" alt="Docker">
                        </div>
                        <div class="tech-icon">
                            <img src="https://skillicons.dev/icons?i=aws" alt="AWS">
                        </div>
                        <div class="tech-icon">
                            <img src="https://skillicons.dev/icons?i=figma" alt="Figma">
                        </div>
                    </div>
                </div>
            </div>
        </section>
        
        <!-- Experience Section -->
        <section class="card">
            <h2 class="card-title"><i class="fas fa-briefcase"></i> Experience</h2>
            <div class="experience-item">
                <h3 class="experience-title">Full-Stack Development</h3>
                <p class="experience-desc">Built full web applications using React, Next.js, and Laravel</p>
                <ul class="feature-list">
                    <li>Developed advanced inventory systems</li>
                    <li>Stock management and order processing</li>
                    <li>Invoicing and product movement tracking</li>
                    <li>Integrated dashboards and authentication systems</li>
                    <li>Designed clean API architectures</li>
                    <li>Created scalable backend logic using Laravel and SQL databases</li>
                </ul>
            </div>
        </section>
        
        <!-- Projects Section -->
        <section class="card">
            <h2 class="card-title"><i class="fas fa-project-diagram"></i> Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <h3 class="project-title"><i class="fas fa-star"></i> Star Family Industry PLC Website</h3>
                    <div class="project-tech">
                        <span class="tech-tag">React</span>
                        <span class="tech-tag">Laravel</span>
                        <span class="tech-tag">Next.js</span>
                    </div>
                    <p class="project-desc">A modern business website with integrated admin dashboard for content and product management.</p>
                </div>
                
                <div class="project-card">
                    <h3 class="project-title"><i class="fas fa-store"></i> Dematsa Trading Website</h3>
                    <div class="project-tech">
                        <span class="tech-tag">Next.js</span>
                        <span class="tech-tag">Laravel</span>
                        <span class="tech-tag">UI/UX</span>
                    </div>
                    <p class="project-desc">A dynamic web platform for managing business operations with a clean UI and seamless backend integration.</p>
                </div>
            </div>
        </section>
        
        <!-- Learning Section -->
        <section class="card">
            <h2 class="card-title"><i class="fas fa-seedling"></i> Currently Learning & Improving</h2>
            <div class="learning-items">
                <div class="learning-item">
                    <i class="fas fa-rocket"></i>
                    <span>Advanced Next.js patterns</span>
                </div>
                <div class="learning-item">
                    <i class="fas fa-sitemap"></i>
                    <span>System architecture & scalable backend design</span>
                </div>
                <div class="learning-item">
                    <i class="fas fa-mobile-alt"></i>
                    <span>Flutter for cross-platform mobile apps</span>
                </div>
            </div>
        </section>
        
        <!-- Contact Section -->
        <section class="card">
            <h2 class="card-title"><i class="fas fa-envelope"></i> Let's Connect</h2>
            <p>Feel free to reach out if you want to collaborate on a project, have questions, or just want to connect!</p>
            <div class="contact-links">
                <a href="https://ousman-portfolio.vercel.app/" class="contact-link">
                    <i class="fas fa-globe"></i> Portfolio
                </a>
                <a href="mailto:ousman@example.com" class="contact-link">
                    <i class="fas fa-envelope"></i> Email
                </a>
                <a href="https://linkedin.com/in/ousman" class="contact-link">
                    <i class="fab fa-linkedin"></i> LinkedIn
                </a>
                <a href="https://twitter.com/ousman" class="contact-link">
                    <i class="fab fa-twitter"></i> Twitter
                </a>
            </div>
        </section>
    </div>

    <script>
        // Add scroll animations
        document.addEventListener('DOMContentLoaded', function() {
            const cards = document.querySelectorAll('.card');
            
            const observer = new IntersectionObserver((entries) => {
                entries.forEach(entry => {
                    if (entry.isIntersecting) {
                        entry.target.style.animation = 'slideUp 0.8s ease-out forwards';
                        observer.unobserve(entry.target);
                    }
                });
            }, { threshold: 0.1 });
            
            cards.forEach(card => {
                observer.observe(card);
            });
            
            // Add typing effect to name
            const nameElement = document.querySelector('.name');
            const nameText = nameElement.textContent;
            nameElement.textContent = '';
            
            let i = 0;
            function typeWriter() {
                if (i < nameText.length) {
                    nameElement.textContent += nameText.charAt(i);
                    i++;
                    setTimeout(typeWriter, 100);
                }
            }
            
            setTimeout(typeWriter, 1000);
        });
    </script>
</body>
</html>
