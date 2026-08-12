<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Abdalla Ayman | Backend Software Engineer</title>

    <meta
        name="description"
        content="Abdalla Ayman - Backend Software Engineer specializing in Python, Django, PostgreSQL, Docker, REST APIs and web scraping."
    >

    <style>
        :root {
            --bg: #0d1117;
            --bg-secondary: #161b22;
            --border: #30363d;
            --text: #e6edf3;
            --muted: #8b949e;
            --accent: #58a6ff;
            --accent-soft: rgba(88, 166, 255, 0.1);
            --green: #3fb950;
            --max-width: 1100px;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family:
                Inter,
                -apple-system,
                BlinkMacSystemFont,
                "Segoe UI",
                Roboto,
                Helvetica,
                Arial,
                sans-serif;

            background: var(--bg);
            color: var(--text);
            line-height: 1.6;
        }

        a {
            color: inherit;
            text-decoration: none;
        }

        .container {
            width: min(92%, var(--max-width));
            margin: auto;
        }

        /* Navigation */

        nav {
            position: sticky;
            top: 0;
            z-index: 100;

            background: rgba(13, 17, 23, 0.9);
            backdrop-filter: blur(10px);

            border-bottom: 1px solid var(--border);
        }

        .nav-container {
            min-height: 64px;

            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .logo {
            font-size: 18px;
            font-weight: 700;
            letter-spacing: -0.5px;
        }

        .logo span {
            color: var(--accent);
        }

        .nav-links {
            display: flex;
            gap: 28px;
            list-style: none;
        }

        .nav-links a {
            color: var(--muted);
            font-size: 14px;
            transition: 0.2s;
        }

        .nav-links a:hover {
            color: var(--text);
        }

        /* Hero */

        .hero {
            min-height: 90vh;

            display: flex;
            align-items: center;

            border-bottom: 1px solid var(--border);
        }

        .hero-content {
            max-width: 850px;
        }

        .status {
            display: inline-flex;
            align-items: center;
            gap: 8px;

            padding: 6px 12px;
            margin-bottom: 24px;

            border: 1px solid var(--border);
            border-radius: 20px;

            color: var(--muted);
            font-size: 13px;

            background: var(--bg-secondary);
        }

        .status-dot {
            width: 7px;
            height: 7px;

            border-radius: 50%;
            background: var(--green);
        }

        .hero h1 {
            font-size: clamp(42px, 7vw, 76px);
            line-height: 1.05;

            letter-spacing: -3px;
            margin-bottom: 18px;
        }

        .hero h1 span {
            color: var(--accent);
        }

        .hero h2 {
            font-size: clamp(20px, 3vw, 30px);
            font-weight: 500;

            color: var(--muted);
            margin-bottom: 25px;
        }

        .hero-description {
            max-width: 700px;

            color: var(--muted);
            font-size: 17px;

            margin-bottom: 32px;
        }

        .buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
        }

        .button {
            padding: 10px 18px;

            border-radius: 6px;
            border: 1px solid var(--border);

            font-size: 14px;
            font-weight: 600;

            transition: 0.2s;
        }

        .button-primary {
            background: var(--text);
            color: var(--bg);

            border-color: var(--text);
        }

        .button-primary:hover {
            opacity: 0.85;
        }

        .button-secondary {
            color: var(--text);
        }

        .button-secondary:hover {
            background: var(--bg-secondary);
            border-color: #484f58;
        }

        /* Sections */

        section {
            padding: 100px 0;
            border-bottom: 1px solid var(--border);
        }

        .section-header {
            margin-bottom: 45px;
        }

        .section-number {
            color: var(--accent);
            font-family: monospace;
            font-size: 13px;
            margin-bottom: 8px;
        }

        .section-title {
            font-size: 32px;
            letter-spacing: -1px;
        }

        .section-description {
            max-width: 700px;
            color: var(--muted);
            margin-top: 10px;
        }

        /* Skills */

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 16px;
        }

        .skill-group {
            padding: 24px;

            background: var(--bg-secondary);
            border: 1px solid var(--border);
            border-radius: 8px;

            transition: 0.2s;
        }

        .skill-group:hover {
            border-color: #484f58;
            transform: translateY(-2px);
        }

        .skill-group h3 {
            font-size: 15px;
            margin-bottom: 14px;
        }

        .skills {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
        }

        .skill {
            padding: 5px 9px;

            background: var(--accent-soft);
            border: 1px solid rgba(88, 166, 255, 0.2);
            border-radius: 5px;

            color: #b6d7ff;
            font-family: monospace;
            font-size: 12px;
        }

        /* Experience */

        .experience {
            padding: 30px;

            background: var(--bg-secondary);
            border: 1px solid var(--border);
            border-radius: 8px;
        }

        .experience-top {
            display: flex;
            justify-content: space-between;
            gap: 20px;

            margin-bottom: 22px;
        }

        .experience h3 {
            font-size: 20px;
        }

        .experience-role {
            color: var(--accent);
            font-size: 14px;
            margin-top: 4px;
        }

        .experience-date {
            color: var(--muted);
            font-family: monospace;
            font-size: 13px;
        }

        .experience ul {
            padding-left: 20px;
            color: var(--muted);
        }

        .experience li {
            margin-bottom: 8px;
        }

        /* Projects */

        .projects {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
        }

        .project {
            display: flex;
            flex-direction: column;

            padding: 28px;

            background: var(--bg-secondary);
            border: 1px solid var(--border);
            border-radius: 8px;

            transition: 0.2s;
        }

        .project:hover {
            transform: translateY(-4px);
            border-color: #484f58;
        }

        .project-label {
            color: var(--accent);
            font-family: monospace;
            font-size: 12px;
            margin-bottom: 12px;
        }

        .project h3 {
            font-size: 22px;
            margin-bottom: 10px;
        }

        .project-description {
            color: var(--muted);
            margin-bottom: 20px;
        }

        .project-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 7px;

            margin-bottom: 25px;
        }

        .project-stack span {
            padding: 4px 8px;

            border: 1px solid var(--border);
            border-radius: 4px;

            color: var(--muted);
            font-family: monospace;
            font-size: 11px;
        }

        .project ul {
            padding-left: 18px;
            color: var(--muted);

            margin-bottom: 25px;
        }

        .project li {
            margin-bottom: 7px;
        }

        .project-link {
            margin-top: auto;

            color: var(--accent);
            font-size: 14px;
            font-weight: 600;
        }

        .project-link:hover {
            text-decoration: underline;
        }

        /* Learning */

        .learning-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 12px;
        }

        .learning-item {
            padding: 18px;

            background: var(--bg-secondary);
            border: 1px solid var(--border);
            border-radius: 7px;

            color: var(--muted);
            font-size: 14px;
        }

        /* GitHub */

        .github-box {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 30px;

            padding: 35px;

            background: var(--bg-secondary);
            border: 1px solid var(--border);
            border-radius: 8px;
        }

        .github-box h3 {
            font-size: 22px;
            margin-bottom: 8px;
        }

        .github-box p {
            color: var(--muted);
            max-width: 650px;
        }

        /* Footer */

        footer {
            padding: 35px 0;

            color: var(--muted);
            font-size: 13px;
        }

        .footer-content {
            display: flex;
            align-items: center;
            justify-content: space-between;
            gap: 20px;
        }

        .footer-links {
            display: flex;
            gap: 18px;
        }

        .footer-links a:hover {
            color: var(--text);
        }

        /* Responsive */

        @media (max-width: 800px) {

            .nav-links {
                display: none;
            }

            .skills-grid,
            .projects {
                grid-template-columns: 1fr;
            }

            .learning-grid {
                grid-template-columns: repeat(2, 1fr);
            }

            .github-box {
                flex-direction: column;
                align-items: flex-start;
            }

            .experience-top {
                flex-direction: column;
            }

            section {
                padding: 70px 0;
            }
        }

        @media (max-width: 500px) {

            .hero h1 {
                letter-spacing: -2px;
            }

            .learning-grid {
                grid-template-columns: 1fr;
            }

            .footer-content {
                flex-direction: column;
                align-items: flex-start;
            }
        }
    </style>
</head>

<body>

    <!-- Navigation -->

    <nav>
        <div class="container nav-container">

            <a href="#" class="logo">
                Abdalla<span>.</span>
            </a>

            <ul class="nav-links">
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#projects">Projects</a></li>
                <li><a href="#learning">Learning</a></li>
            </ul>

        </div>
    </nav>


    <!-- Hero -->

    <header class="hero">

        <div class="container">

            <div class="hero-content">

                <div class="status">
                    <span class="status-dot"></span>
                    Available for software engineering opportunities
                </div>

                <h1>
                    Abdalla <span>Ayman</span>
                </h1>

                <h2>
                    Backend Software Engineer
                </h2>

                <p class="hero-description">
                    Backend-focused software engineer working mainly with
                    Python, Django, PostgreSQL, and Docker.
                    I build backend systems, REST APIs, web scraping pipelines,
                    and data-driven applications for businesses and personal projects.
                </p>

                <div class="buttons">

                    <a
                        href="https://github.com/YOUR_USERNAME"
                        class="button button-primary"
                        target="_blank"
                    >
                        GitHub
                    </a>

                    <a
                        href="https://www.linkedin.com/in/YOUR_USERNAME/"
                        class="button button-secondary"
                        target="_blank"
                    >
                        LinkedIn
                    </a>

                    <a
                        href="#projects"
                        class="button button-secondary"
                    >
                        View Projects
                    </a>

                </div>

            </div>

        </div>

    </header>


    <!-- About -->

    <section id="about">

        <div class="container">

            <div class="section-header">

                <div class="section-number">01 / ABOUT</div>

                <h2 class="section-title">
                    Building reliable backend systems.
                </h2>

                <p class="section-description">
                    I focus on designing and building backend systems that are
                    practical, maintainable, and ready to integrate with real applications.
                </p>

            </div>

            <div class="experience">

                <p style="color: var(--muted); max-width: 850px;">
                    My work covers backend development, REST API design,
                    database architecture, web scraping, data processing,
                    search systems, and application infrastructure.
                    I am comfortable working across the backend, database,
                    and infrastructure layers of a project.
                </p>

            </div>

        </div>

    </section>


    <!-- Skills -->

    <section id="skills">

        <div class="container">

            <div class="section-header">

                <div class="section-number">02 / TECH STACK</div>

                <h2 class="section-title">
                    Technologies I work with.
                </h2>

            </div>

            <div class="skills-grid">

                <div class="skill-group">

                    <h3>Languages</h3>

                    <div class="skills">
                        <span class="skill">Python</span>
                        <span class="skill">C++</span>
                        <span class="skill">JavaScript</span>
                        <span class="skill">TypeScript</span>
                        <span class="skill">SQL</span>
                    </div>

                </div>


                <div class="skill-group">

                    <h3>Backend</h3>

                    <div class="skills">
                        <span class="skill">Django</span>
                        <span class="skill">Django REST Framework</span>
                        <span class="skill">REST APIs</span>
                    </div>

                </div>


                <div class="skill-group">

                    <h3>Databases</h3>

                    <div class="skills">
                        <span class="skill">PostgreSQL</span>
                        <span class="skill">SQL</span>
                    </div>

                </div>


                <div class="skill-group">

                    <h3>Web Scraping</h3>

                    <div class="skills">
                        <span class="skill">Scrapy</span>
                        <span class="skill">Playwright</span>
                        <span class="skill">Scrapy-Playwright</span>
                    </div>

                </div>


                <div class="skill-group">

                    <h3>Search</h3>

                    <div class="skills">
                        <span class="skill">Meilisearch</span>
                    </div>

                </div>


                <div class="skill-group">

                    <h3>DevOps</h3>

                    <div class="skills">
                        <span class="skill">Docker</span>
                        <span class="skill">Docker Compose</span>
                        <span class="skill">Linux</span>
                    </div>

                </div>


                <div class="skill-group">

                    <h3>Frontend</h3>

                    <div class="skills">
                        <span class="skill">Next.js</span>
                        <span class="skill">React</span>
                        <span class="skill">TypeScript</span>
                    </div>

                </div>


                <div class="skill-group">

                    <h3>Tools</h3>

                    <div class="skills">
                        <span class="skill">Git</span>
                        <span class="skill">GitHub</span>
                        <span class="skill">Postman</span>
                        <span class="skill">VS Code</span>
                    </div>

                </div>

            </div>

        </div>

    </section>


    <!-- Experience -->

    <section id="experience">

        <div class="container">

            <div class="section-header">

                <div class="section-number">03 / EXPERIENCE</div>

                <h2 class="section-title">
                    Freelance Software Engineer
                </h2>

            </div>

            <div class="experience">

                <div class="experience-top">

                    <div>

                        <h3>Freelance Software Engineer</h3>

                        <div class="experience-role">
                            Backend Development
                        </div>

                    </div>

                    <div class="experience-date">
                        Software Engineering
                    </div>

                </div>

                <ul>

                    <li>
                        Building custom backend systems for businesses.
                    </li>

                    <li>
                        Developing REST APIs using Django REST Framework.
                    </li>

                    <li>
                        Designing PostgreSQL databases and data models.
                    </li>

                    <li>
                        Building web scraping and data extraction systems.
                    </li>

                    <li>
                        Integrating search engines and external services.
                    </li>

                    <li>
                        Containerizing applications using Docker.
                    </li>

                    <li>
                        Working across backend, database, and infrastructure layers.
                    </li>

                </ul>

            </div>

        </div>

    </section>


    <!-- Projects -->

    <section id="projects">

        <div class="container">

            <div class="section-header">

                <div class="section-number">04 / PROJECTS</div>

                <h2 class="section-title">
                    Selected projects.
                </h2>

                <p class="section-description">
                    A selection of systems I have designed and built.
                </p>

            </div>


            <div class="projects">


                <!-- MarketLens -->

                <article class="project">

                    <div class="project-label">
                        PROJECT / 01
                    </div>

                    <h3>MarketLens</h3>

                    <p class="project-description">
                        Product search and price comparison platform
                        for collecting, processing, indexing, and searching
                        e-commerce product data.
                    </p>

                    <div class="project-stack">

                        <span>Python</span>
                        <span>Scrapy</span>
                        <span>Playwright</span>
                        <span>Django REST Framework</span>
                        <span>PostgreSQL</span>
                        <span>Meilisearch</span>
                        <span>Next.js</span>
                        <span>React</span>
                        <span>Docker</span>

                    </div>

                    <ul>

                        <li>
                            Built the scraping system for collecting
                            e-commerce product data.
                        </li>

                        <li>
                            Implemented dynamic scraping using
                            Scrapy and Playwright.
                        </li>

                        <li>
                            Built data processing and storage pipelines.
                        </li>

                        <li>
                            Designed the backend API using Django REST Framework.
                        </li>

                        <li>
                            Implemented product search using Meilisearch.
                        </li>

                        <li>
                            Containerized the application using Docker.
                        </li>

                        <li>
                            Integrated the backend, search engine,
                            database, and frontend.
                        </li>

                    </ul>

                    <a
                        href="https://github.com/YOUR_USERNAME/MARKETLENS_REPO"
                        target="_blank"
                        class="project-link"
                    >
                        View repository →
                    </a>

                </article>


                <!-- Daar Al-Bnaa -->

                <article class="project">

                    <div class="project-label">
                        PROJECT / 02
                    </div>

                    <h3>Daar Al-Bnaa</h3>

                    <p class="project-description">
                        Backend system developed for a construction company,
                        providing APIs for consultations, services,
                        portfolio management, and administration.
                    </p>

                    <div class="project-stack">

                        <span>Python</span>
                        <span>Django</span>
                        <span>DRF</span>
                        <span>PostgreSQL</span>
                        <span>Docker</span>

                    </div>

                    <ul>

                        <li>
                            Built the backend architecture and REST APIs.
                        </li>

                        <li>
                            Implemented consultation request management.
                        </li>

                        <li>
                            Built services and portfolio management.
                        </li>

                        <li>
                            Implemented authentication and authorization.
                        </li>

                        <li>
                            Designed database models and API structure.
                        </li>

                        <li>
                            Prepared the backend for frontend integration.
                        </li>

                    </ul>

                    <a
                        href="https://github.com/YOUR_USERNAME/DAAR_ALBNAA_REPO"
                        target="_blank"
                        class="project-link"
                    >
                        View repository →
                    </a>

                </article>

            </div>

        </div>

    </section>


    <!-- Learning -->

    <section id="learning">

        <div class="container">

            <div class="section-header">

                <div class="section-number">05 / CURRENTLY LEARNING</div>

                <h2 class="section-title">
                    Going deeper into computer science.
                </h2>

                <p class="section-description">
                    Beyond frameworks, I am strengthening the fundamentals
                    behind the systems I build.
                </p>

            </div>

            <div class="learning-grid">

                <div class="learning-item">
                    Data Structures & Algorithms
                </div>

                <div class="learning-item">
                    System Design
                </div>

                <div class="learning-item">
                    Database Internals
                </div>

                <div class="learning-item">
                    Computer Networks
                </div>

                <div class="learning-item">
                    Operating Systems
                </div>

                <div class="learning-item">
                    C++
                </div>

                <div class="learning-item">
                    Backend Architecture
                </div>

                <div class="learning-item">
                    Distributed Systems
                </div>

            </div>

        </div>

    </section>


    <!-- GitHub -->

    <section>

        <div class="container">

            <div class="github-box">

                <div>

                    <h3>Explore my GitHub</h3>

                    <p>
                        Most of my repositories focus on backend development,
                        Django applications, web scraping, APIs, databases,
                        automation, and full-stack systems.
                    </p>

                </div>

                <a
                    href="https://github.com/YOUR_USERNAME"
                    target="_blank"
                    class="button button-primary"
                >
                    GitHub Profile
                </a>

            </div>

        </div>

    </section>


    <!-- Footer -->

    <footer>

        <div class="container footer-content">

            <div>
                © 2026 Abdalla Ayman
            </div>

            <div class="footer-links">

                <a
                    href="https://github.com/YOUR_USERNAME"
                    target="_blank"
                >
                    GitHub
                </a>

                <a
                    href="https://www.linkedin.com/in/YOUR_USERNAME/"
                    target="_blank"
                >
                    LinkedIn
                </a>

            </div>

        </div>

    </footer>

</body>
</html>
