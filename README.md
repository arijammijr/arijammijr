<!DOCTYPE html>
<html lang="en" class="light">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Daniel Arinze - Portfolio</title>
    <style>
        /* Base Styles */
        :root {
            --primary-color: #1e293b
            --heading-color: #2
            --text-color: #6373
            --background: #ffff
            --card-background: 
            --border-color: #e5
            --shadow-color: rgb 0.1);
            --transition: all 0.3s ease;
        }

        html.dark {
            --primary-color: #4a6cf7;
            --heading-color: #ffffff;
            --text-color: #b3c5d5;
            --background: #0f172a;
            --card-background: #1e293b;
            --border-color: #334155;
            --shadow-color: rgba(0, 0, 0, 0.25);
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Inter', sans-serif;
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--background);
            transition: var(--transition);
        }

        h1, h2, h3, h4, h5, h6 {
            color: var(--heading-color);
            transition: var(--transition);
        }

        a {
            text-decoration: none;
            color: var(--primary-color);
            transition: var(--transition);
        }

        /* Header Styles */
        header {
            padding: 1.5rem 0;
            background-color: var(--background);
            box-shadow: 0 2px 10px var(--shadow-color);
            position: sticky;
            top: 0;
            z-index: 100;
            transition: var(--transition);
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 2rem;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--heading-color);
        }

        .nav-menu {
            display: flex;
            list-style: none;
            gap: 2rem;
            align-items: center;
        }

        .nav-link {
            color: var(--text-color);
            font-weight: 500;
            position: relative;
        }

        .nav-link:hover {
            color: var(--primary-color);
        }

        .nav-link::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--primary-color);
            transition: width 0.3s;
        }

        .nav-link:hover::after {
            width: 100%;
        }

        /* Hero Section */
        .hero {
            padding: 6rem 0;
            display: flex;
            align-items: center;
            min-height: calc(100vh - 80px);
        }

        .hero-content {
            display: flex;
            align-items: center;
            gap: 3rem;
        }

        .hero-text {
            flex: 1;
        }

        .hero-image {
            flex: 1;
            text-align: center;
        }

        .hero-image img {
            max-width: 100%;
            height: auto;
            border-radius: 20px;
            box-shadow: 0 20px 40px var(--shadow-color);
            transition: var(--transition);
        }

        .subtitle {
            font-size: 1.125rem;
            font-weight: 500;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }

        .title {
            font-size: 3.5rem;
            font-weight: 700;
            line-height: 1.2;
            margin-bottom: 1.5rem;
        }

        .description {
            font-size: 1.125rem;
            margin-bottom: 2rem;
            max-width: 600px;
        }

        .btn {
            display: inline-block;
            padding: 0.75rem 1.5rem;
            background-color: var(--primary-color);
            color: white;
            border-radius: 8px;
            font-weight: 500;
            text-align: center;
            transition: all 0.3s ease;
        }

        .btn:hover {
            background-color: #3a5bd9;
            transform: translateY(-3px);
        }

        /* About Section */
        .section {
            padding: 5rem 0;
        }

        .section-title {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }

        .about-image img {
            max-width: 100%;
            border-radius: 20px;
            box-shadow: 0 20px 40px var(--shadow-color);
            transition: var(--transition);
        }

        .skills {
            margin-top: 2rem;
        }

        .skill-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 1rem;
            margin-top: 1rem;
        }

        .skill-tag {
            background-color: var(--card-background);
            color: var(--text-color);
            padding: 0.5rem 1rem;
            border-radius: 50px;
            font-size: 0.875rem;
            transition: var(--transition);
        }

        /* Projects Section */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background-color: var(--card-background);
            border-radius: 12px;
            overflow: hidden;
            box-shadow: 0 10px 30px var(--shadow-color);
            transition: var(--transition);
        }

        .project-card:hover {
            transform: translateY(-10px);
        }

        .project-image {
            height: 200px;
            overflow: hidden;
        }

        .project-image img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            transition: transform 0.5s ease;
        }

        .project-card:hover .project-image img {
            transform: scale(1.1);
        }

        .project-content {
            padding: 1.5rem;
        }

        .project-title {
            font-size: 1.25rem;
            margin-bottom: 0.5rem;
        }

        .project-tags {
            display: flex;
            flex-wrap: wrap;
            gap: 0.5rem;
            margin: 1rem 0;
        }

        .project-tag {
            background-color: rgba(74, 108, 247, 0.1);
            color: var(--primary-color);
            font-size: 0.75rem;
            padding: 0.25rem 0.75rem;
            border-radius: 50px;
        }

        .project-link {
            display: inline-flex;
            align-items: center;
            gap: 0.5rem;
            font-weight: 500;
            margin-top: 1rem;
        }

        /* Contact Section */
        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
            gap: 2rem;
            margin-bottom: 3rem;
        }

        .contact-card {
            background-color: var(--card-background);
            padding: 2rem;
            border-radius: 12px;
            text-align: center;
            box-shadow: 0 10px 30px var(--shadow-color);
            transition: var(--transition);
        }

        .contact-card:hover {
            transform: translateY(-5px);
        }

        .contact-icon {
            width: 60px;
            height: 60px;
            background-color: rgba(74, 108, 247, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            margin: 0 auto 1rem;
        }

        .contact-icon svg {
            width: 30px;
            height: 30px;
            fill: var(--primary-color);
        }

        .contact-method {
            font-weight: 600;
            margin-bottom: 0.5rem;
            color: var(--heading-color);
        }

        .contact-detail {
            color: var(--text-color);
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
        }

        .form-group {
            margin-bottom: 1.5rem;
        }

        .form-label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
            color: var(--heading-color);
        }

        .form-input {
            width: 100%;
            padding: 0.75rem 1rem;
            background-color: var(--card-background);
            border: 1px solid var(--border-color);
            border-radius: 8px;
            color: var(--text-color);
            transition: var(--transition);
        }

        .form-input:focus {
            outline: none;
            border-color: var(--primary-color);
            box-shadow: 0 0 0 3px rgba(74, 108, 247, 0.1);
        }

        textarea.form-input {
            resize: vertical;
            min-height: 150px;
        }

        /* Footer */
        footer {
            background-color: var(--card-background);
            padding: 3rem 0;
            text-align: center;
            margin-top: 3rem;
            transition: var(--transition);
        }

        .footer-content {
            max-width: 600px;
            margin: 0 auto;
        }

        .social-links {
            display: flex;
            justify-content: center;
            gap: 1rem;
            margin: 1.5rem 0;
        }

        .social-link {
            width: 40px;
            height: 40px;
            background-color: var(--background);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            transition: var(--transition);
        }

        .social-link:hover {
            background-color: var(--primary-color);
        }

        .social-link svg {
            width: 20px;
            height: 20px;
            fill: var(--heading-color);
            transition: var(--transition);
        }

        .social-link:hover svg {
            fill: white;
        }

        .copyright {
            color: var(--text-color);
            font-size: 0.875rem;
        }

        /* Dark Mode Toggle */
        .theme-toggle {
            position: relative;
            display: inline-block;
            width: 60px;
            height: 30px;
            margin-left: 20px;
        }

        .theme-toggle input {
            opacity: 0;
            width: 0;
            height: 0;
        }

        .slider {
            position: absolute;
            cursor: pointer;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: #ccc;
            transition: .4s;
            border-radius: 30px;
        }

        .slider:before {
            position: absolute;
            content: "";
            height: 22px;
            width: 22px;
            left: 4px;
            bottom: 4px;
            background-color: white;
            transition: .4s;
            border-radius: 50%;
        }

        input:checked + .slider {
            background-color: var(--primary-color);
        }

        input:focus + .slider {
            box-shadow: 0 0 1px var(--primary-color);
        }

        input:checked + .slider:before {
            transform: translateX(30px);
        }

        .slider .icons {
            display: flex;
            justify-content: space-between;
            padding: 0 8px;
            color: white;
            font-size: 14px;
            height: 100%;
            align-items: center;
        }

        .theme-icon {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            font-size: 14px;
            color: white;
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .hero-content {
                flex-direction: column-reverse;
                text-align: center;
            }

            .hero-text {
                margin-top: 2rem;
            }

            .description {
                margin: 0 auto 2rem;
            }

            .about-content {
                grid-template-columns: 1fr;
            }

            .about-image {
                text-align: center;
            }
        }

        @media (max-width: 768px) {
            .navbar {
                flex-direction: column;
                gap: 1rem;
            }

            .title {
                font-size: 2.5rem;
            }

            .section-title {
                font-size: 2rem;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <nav class="navbar">
                <a href="#" class="logo">Daniel Arinze</a>
                <ul class="nav-menu">
                    <li><a href="#home" class="nav-link">Home</a></li>
                    <li><a href="#about" class="nav-link">About</a></li>
                    <li><a href="#projects" class="nav-link">Projects</a></li>
                    <li><a href="#contact" class="nav-link">Contact</a></li>
                    <li>
                        <label class="theme-toggle">
                            <input type="checkbox" id="theme-toggle">
                            <span class="slider">
                                <div class="icons">
                                    <span class="theme-icon">☀️</span>
                                    <span class="theme-icon">🌙</span>
                                </div>
                            </span>
                        </label>
                    </li>
                </ul>
            </nav>
        </div>
    </header>

    <section id="home" class="hero">
        <div class="container">
            <div class="hero-content">
                <div class="hero-text">
                    <h3 class="subtitle">Hello, I'm</h3>
                    <h1 class="title">Daniel Arinze</h1>
                    <p class="description">
                        A passionate Full-Stack Developer specializing in building exceptional digital experiences. I focus on creating responsive and user-friendly applications with modern technologies.
                    </p>
                    <a href="#contact" class="btn">Get In Touch</a>
                </div>
                <div class="hero-image">
                    <img src="/api/placeholder/450/450" alt="Daniel Arinze">
                </div>
            </div>
        </div>
    </section>

    <section id="about" class="section">
        <div class="container">
            <h2 class="section-title">About Me</h2>
            <div class="about-content">
                <div class="about-image">
                    <img src="/api/placeholder/500/400" alt="Daniel working">
                </div>
                <div class="about-text">
                    <p>
                        I'm a Full-Stack Developer with a passion for building beautiful, functional, and user-centered digital experiences. With 5+ years of experience in web development, I enjoy working on both client-side and server-side applications.
                    </p>
                    <p>
                        My journey in tech started when I built my first website back in college. Since then, I've worked with various startups and companies to help them achieve their business goals through technology.
                    </p>
                    <div class="skills">
                        <h3>My Skills</h3>
                        <div class="skill-tags">
                            <span class="skill-tag">HTML5</span>
                            <span class="skill-tag">CSS3</span>
                            <span class="skill-tag">JavaScript</span>
                            <span class="skill-tag">React</span>
                            <span class="skill-tag">Node.js</span>
                            <span class="skill-tag">Express</span>
                            <span class="skill-tag">MongoDB</span>
                            <span class="skill-tag">PostgreSQL</span>
                            <span class="skill-tag">Git</span>
                            <span class="skill-tag">Responsive Design</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="projects" class="section">
        <div class="container">
            <h2 class="section-title">My Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-image">
                        <img src="/api/placeholder/400/300" alt="Project 1">
                    </div>
                    <div class="project-content">
                        <h3 class="project-title">E-commerce Platform</h3>
                        <p>A full-featured e-commerce platform with payment integration, user authentication, and admin dashboard.</p>
                        <div class="project-tags">
                            <span class="project-tag">React</span>
                            <span class="project-tag">Node.js</span>
                            <span class="project-tag">MongoDB</span>
                        </div>
                        <a href="#" class="project-link">View Project →</a>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-image">
                        <img src="/api/placeholder/400/300" alt="Project 2">
                    </div>
                    <div class="project-content">
                        <h3 class="project-title">Task Management App</h3>
                        <p>A collaborative task management application with real-time updates and team workspaces.</p>
                        <div class="project-tags">
                            <span class="project-tag">React</span>
                            <span class="project-tag">Firebase</span>
                            <span class="project-tag">Redux</span>
                        </div>
                        <a href="#" class="project-link">View Project →</a>
                    </div>
                </div>

                <div class="project-card">
                    <div class="project-image">
                        <img src="/api/placeholder/400/300" alt="Project 3">
                    </div>
                    <div class="project-content">
                        <h3 class="project-title">Fitness Tracker</h3>
                        <p>A mobile-responsive fitness tracking application with workout planning and progress visualization.</p>
                        <div class="project-tags">
                            <span class="project-tag">React Native</span>
                            <span class="project-tag">Express</span>
                            <span class="project-tag">Chart.js</span>
                        </div>
                        <a href="#" class="project-link">View Project →</a>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" class="section">
        <div class="container">
            <h2 class="section-title">Get In Touch</h2>
            <div class="contact-info">
                <div class="contact-card">
                    <div class="contact-icon">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                            <path d="M20 4H4a2 2 0 00-2 2v12a2 2 0 002 2h16a2 2 0 002-2V6a2 2 0 00-2-2zm0 4.7l-8 5.334L4 8.7V6.297l8 5.333 8-5.333V8.7z"/>
                        </svg>
                    </div>
                    <h3 class="contact-method">Email</h3>
                    <p class="contact-detail">daniel@example.com</p>
                </div>

                <div class="contact-card">
                    <div class="contact-icon">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                            <path d="M21 16.42v3.536a1 1 0 01-.93.998c-.437.03-.794.046-1.07.046-8.837 0-16-7.163-16-16 0-.276.015-.633.046-1.07A1 1 0 014.044 3H7.58a.5.5 0 01.498.45c.023.23.044.413.064.552a13.9 13.9 0 00.7 2.3c.058.147.025.315-.08.45l-1.795 2.31a13.415 13.415 0 006.12 6.12l2.34-1.795c.135-.105.3-.137.45-.08a13.9 13.9 0 002.3.7c.137.02.32.042.55.064a.5.5 0 01.449.498z"/>
                        </svg>
                    </div>
                    <h3 class="contact-method">Phone</h3>
                    <p class="contact-detail">+123 456 7890</p>
                </div>

                <div class="contact-card">
                    <div class="contact-icon">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                            <path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5a2.5 2.5 0 010-5 2.5 2.5 0 010 5z"/>
                        </svg>
                    </div>
                    <h3 class="contact-method">Location</h3>
                    <p class="contact-detail">Lagos, Nigeria</p>
                </div>
            </div>

            <div class="contact-form">
                <form>
                    <div class="form-group">
                        <label for="name" class="form-label">Your Name</label>
                        <input type="text" id="name" class="form-input" required>
                    </div>
                    <div class="form-group">
                        <label for="email" class="form-label">Your Email</label>
                        <input type="email" id="email" class="form-input" required>
                    </div>
                    <div class="form-group">
                        <label for="subject" class="form-label">Subject</label>
                        <input type="text" id="subject" class="form-input" required>
                    </div>
                    <div class="form-group">
                        <label for="message" class="form-label">Message</label>
                        <textarea id="message" class="form-input" required></textarea>
                    </div>
                    <button type="submit" class="btn">Send Message</button>
                </form>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <div class="footer-content">
                <h3>Daniel Arinze</h3>
                <p>Full-Stack Developer creating impactful digital experiences.</p>
                <div class="social-links">
                    <a href="#" class="social-link">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                            <path d="M12 0C5.373 0 0 5.373 0 12s5.373 12 12 12 12-5.373 12-12S18.627 0 12 0zm-2 16h-2v-6h2v6zm-1-6.891c-.607 0-1.1-.496-1.1-1.109 0-.612.492-1.109 1.1-1.109s1.1.497 1.1 1.109c0 .613-.493 1.109-1.1 1.109zm8 6.891h-1.998v-2.861c0-1.881-2.002-1.722-2.002 0v2.861h-2v-6h2v1.093c.872-1.616 4-1.736 4 1.548v3.359z"/>
                        </svg>
                    </a>
                    <a href="#" class="social-link">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                            <path d="M12 0C5.373 0 0 5.373 0 12s5.373 12 12 12 12-5.373 12-12S18.627 0 12 0zm5.066 9.645c.183 4.04-2.83 8.544-8.164 8.544-1.622 0-3.131-.476-4.402-1.291 1.524.18 3.045-.244 4.252-1.189-1.256-.023-2.317-.854-2.684-1.995.451.086.895.061 1.298-.049-1.381-.278-2.335-1.522-2.304-2.853.388.215.83.344 1.301.359-1.279-.855-1.641-2.544-.889-3.835 1.416 1.738 3.533 2.881 5.92 3.001-.419-1.796.944-3.527 2.799-3.527.825 0 1.572.349 2.096.907.654-.128 1.27-.368 1.824-.697-.215.671-.67 1.233-1.263 1.589.581-.07 1.135-.224 1.649-.453-.384.578-.87 1.084-1.433 1.489z"/>
                        </svg>
                    </a>
                    <a href="#" class="social-link">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                            <path d="M12 0C5.374 0 0 5.373 0 12c0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23A11.509 11.509 0 0112 5.803c1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576C20.566 21.797 24 17.3 24 12c0-6.627-5.373-12-12-12z"/>
                        </svg>
                    </a>
                    <a href="#" class="social-link">
                        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24">
                            <path d="M12 0C5.372 0 0 5.373 0 12s5.372 12 12 12 12-5.373 12-12S18.628 0 12 0zm6.885 8.166c-.476 7.543-4.886 11.77-12.039 11.989h-.311c-3.06-.001-5.63-1.414-6.535-3.435 1.51.378 3.442.305 4.847-.493-1.259-.362-2.948-2.594-3.585-4.815 1.33.23 2.035.105 2.035.105-2.1-1.05-2.884-4.329-1.462-6.275 4.241 4.66 7.689 4.503 7.689 4.503s-.91-5.261 5.194-5.261c2.087 0 3.15 1.356 3.15 1.356s1.858-.215 2.873-.832c0 .815-1.099 2.384-1.099 2.384s1.302-.126 2.171-.611c0 .543-1.198 2.104-2.928 3.385z"/>
                        </svg>
                    </a>
                </div>
                <p class="copyright">&copy; 2025 Daniel Arinze. All rights reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Theme Toggle Script
        const themeToggle = document.getElementById('theme-toggle');
        const body = document.body;

        themeToggle.addEventListener('change', () => {
            if (themeToggle.checked) {
                body.classList.add('dark');
            } else {
                body.classList.remove('dark');
            }
        });
    </script>
</body> 
</html>
<!-- End of HTML Document -->
<!-- This is a simple portfolio template for Daniel Arinze. It includes sections for home, about, projects, and contact. The design is responsive and includes a dark mode toggle. The code is structured with HTML, CSS, and JavaScript. -->
