<!DOCTYPE html>
<html lang="en" class="light">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Daniel Arinze - Portfolio</title>
    <style>
        /* Base Styles */
        :root {
            --primary-color: #1e293b;
            --heading-color: #222;
            --text-color: #637373;
            --background: #ffffff;
            --card-background: #f9f9f9;
            --border-color: #e5e5e5;
            --shadow-color: rgba(0, 0, 0, 0.1);
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

        .btn-long {
            padding: 1rem 2rem;
            display: block;
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
                            <span class="slider"></span>
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
                        A passionate Full-Stack Developer specializing in building exceptional digital experiences.
                    </p>
                    <a href="#contact" class="btn">Get In Touch</a>
                </div>
                <div class="hero-image">
                    <img src="/api/placeholder/450/450" alt="Professional portrait of Daniel Arinze">
                </div>
            </div>
        </div>
    </section>

    <footer>
        <div class="container">
            <p>&copy; 2025 Daniel Arinze. All rights reserved.</p>
        </div>
    </footer>

    <script>
        const themeToggle = document.getElementById('theme-toggle');
        const body = document.body;
        const savedTheme = localStorage.getItem('theme');
        if (savedTheme === 'dark') {
            body.classList.add('dark');
            themeToggle.checked = true;
        }

        themeToggle.addEventListener('change', () => {
            if (themeToggle.checked) {
                body.classList.add('dark');
                localStorage.setItem('theme', 'dark');
            } else {
                body.classList.remove('dark');
                localStorage.setItem('theme', 'light');
            }
        });
    </script>
</body>
</html>
