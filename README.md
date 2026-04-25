<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ch1llc0d3 — AI Engineer • Cybersecurity • Full Stack</title>
    
    <!-- Google Fonts: VEIDT Brand Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700;900&family=Rajdhani:wght@400;600;700&family=Inter:wght@300;400;500;600&family=JetBrains+Mono:wght@400;500&family=Bebas+Neue&display=swap" rel="stylesheet">
    
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            /* VEIDT Brand Colors */
            --hermit-purple: #8A2BE2;
            --hamon-gold: #FFD700;
            --void: #050505;
            --carbon: #1A1A2E;
            --steel: #16213E;
            --smoke: #0F3460;
            --white-smoke: #F5F5F5;
            --silver: #A0A0B0;
            --crimson: #E63946;
            --matrix-green: #39FF14;
            --arc-blue: #00B4D8;
            
            /* Typography */
            --font-display: 'Orbitron', 'Arial Black', sans-serif;
            --font-heading: 'Rajdhani', 'Arial', sans-serif;
            --font-body: 'Inter', 'Arial', sans-serif;
            --font-code: 'JetBrains Mono', monospace;
        }

        html {
            scroll-behavior: smooth;
        }

        body {
            font-family: var(--font-body);
            background: linear-gradient(135deg, var(--void) 0%, var(--carbon) 50%, var(--void) 100%);
            color: var(--white-smoke);
            line-height: 1.6;
            min-height: 100vh;
        }

        /* HEADER / HERO */
        header {
            position: relative;
            padding: 60px 20px;
            text-align: center;
            border-bottom: 1px solid rgba(138, 43, 226, 0.3);
            background: linear-gradient(180deg, rgba(138, 43, 226, 0.05) 0%, transparent 100%);
            animation: fadeInDown 0.8s ease-out;
        }

        .hero-title {
            font-family: var(--font-display);
            font-size: clamp(2.5rem, 8vw, 4rem);
            font-weight: 900;
            color: var(--hamon-gold);
            letter-spacing: 0.05em;
            text-transform: uppercase;
            margin-bottom: 10px;
            text-shadow: 0 0 20px rgba(138, 43, 226, 0.5);
        }

        .hero-subtitle {
            font-family: var(--font-heading);
            font-size: 1.2rem;
            color: var(--hermit-purple);
            letter-spacing: 0.08em;
            text-transform: uppercase;
            margin-bottom: 30px;
        }

        .hero-tagline {
            font-size: 1rem;
            color: var(--silver);
            max-width: 600px;
            margin: 0 auto 40px;
            line-height: 1.8;
        }

        .hero-badges {
            display: flex;
            flex-wrap: wrap;
            gap: 15px;
            justify-content: center;
            margin-bottom: 30px;
        }

        .badge {
            display: inline-block;
            padding: 8px 16px;
            background: rgba(138, 43, 226, 0.1);
            border: 1px solid var(--hermit-purple);
            border-radius: 4px;
            font-family: var(--font-code);
            font-size: 0.85rem;
            color: var(--hamon-gold);
            text-transform: uppercase;
            letter-spacing: 0.05em;
            transition: all 0.3s ease;
            cursor: pointer;
        }

        .badge:hover {
            background: var(--hermit-purple);
            color: var(--void);
            box-shadow: 0 0 20px rgba(138, 43, 226, 0.6);
            transform: translateY(-2px);
        }

        /* NAVIGATION */
        nav {
            position: sticky;
            top: 0;
            z-index: 100;
            background: rgba(5, 5, 5, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid rgba(138, 43, 226, 0.2);
            padding: 0 20px;
        }

        nav ul {
            display: flex;
            justify-content: center;
            gap: 30px;
            flex-wrap: wrap;
            padding: 15px 0;
            list-style: none;
            max-width: 1200px;
            margin: 0 auto;
        }

        nav a {
            font-family: var(--font-heading);
            font-size: 0.9rem;
            color: var(--white-smoke);
            text-decoration: none;
            text-transform: uppercase;
            letter-spacing: 0.05em;
            transition: color 0.3s ease;
            position: relative;
            padding-bottom: 5px;
        }

        nav a::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 0;
            width: 0;
            height: 2px;
            background: var(--hamon-gold);
            transition: width 0.3s ease;
        }

        nav a:hover::after {
            width: 100%;
        }

        nav a:hover {
            color: var(--hamon-gold);
        }

        /* MAIN CONTAINER */
        main {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* SECTIONS */
        section {
            margin: 80px 0;
            animation: fadeInUp 0.8s ease-out;
        }

        section h2 {
            font-family: var(--font-heading);
            font-size: 2.2rem;
            color: var(--hermit-purple);
            text-transform: uppercase;
            letter-spacing: 0.08em;
            margin-bottom: 40px;
            padding-bottom: 15px;
            border-bottom: 2px solid var(--hamon-gold);
            position: relative;
        }

        section h2::before {
            content: '';
            position: absolute;
            left: 0;
            bottom: -2px;
            width: 50px;
            height: 2px;
            background: var(--hamon-gold);
        }

        /* ABOUT SECTION */
        .about-grid {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 40px;
            margin-bottom: 40px;
        }

        .about-text {
            font-size: 1rem;
            line-height: 1.8;
            color: var(--white-smoke);
        }

        .about-code {
            background: var(--carbon);
            border: 1px solid rgba(138, 43, 226, 0.4);
            border-left: 3px solid var(--hamon-gold);
            border-radius: 4px;
            padding: 20px;
            font-family: var(--font-code);
            font-size: 0.9rem;
            color: var(--matrix-green);
            overflow-x: auto;
            line-height: 1.6;
        }

        @media (max-width: 768px) {
            .about-grid {
                grid-template-columns: 1fr;
            }
        }

        /* TECH STACK */
        .tech-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-bottom: 40px;
        }

        .tech-category {
            background: var(--carbon);
            border: 1px solid rgba(138, 43, 226, 0.3);
            border-radius: 4px;
            padding: 25px;
            transition: all 0.3s ease;
        }

        .tech-category:hover {
            border-color: var(--hamon-gold);
            background: rgba(138, 43, 226, 0.1);
            box-shadow: 0 0 20px rgba(138, 43, 226, 0.3);
        }

        .tech-category h3 {
            font-family: var(--font-heading);
            color: var(--hamon-gold);
            margin-bottom: 15px;
            text-transform: uppercase;
            letter-spacing: 0.05em;
        }

        .tech-items {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
        }

        .tech-item {
            display: inline-block;
            padding: 6px 12px;
            background: rgba(255, 215, 0, 0.1);
            border: 1px solid var(--hamon-gold);
            border-radius: 4px;
            font-family: var(--font-code);
            font-size: 0.8rem;
            color: var(--hamon-gold);
            text-transform: uppercase;
            letter-spacing: 0.03em;
            transition: all 0.3s ease;
        }

        .tech-item:hover {
            background: var(--hamon-gold);
            color: var(--void);
        }

        /* PROJECTS */
        .projects-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px;
        }

        .project-card {
            background: linear-gradient(135deg, rgba(26, 26, 46, 0.8) 0%, rgba(22, 33, 62, 0.8) 100%);
            border: 1px solid rgba(138, 43, 226, 0.3);
            border-radius: 4px;
            padding: 30px;
            transition: all 0.3s ease;
            position: relative;
            overflow: hidden;
        }

        .project-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            height: 3px;
            background: linear-gradient(90deg, var(--hermit-purple), var(--hamon-gold));
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        .project-card:hover {
            border-color: var(--hamon-gold);
            background: linear-gradient(135deg, rgba(138, 43, 226, 0.1) 0%, rgba(22, 33, 62, 0.8) 100%);
            transform: translateY(-5px);
            box-shadow: 0 10px 30px rgba(138, 43, 226, 0.3);
        }

        .project-card:hover::before {
            opacity: 1;
        }

        .project-title {
            font-family: var(--font-heading);
            font-size: 1.5rem;
            color: var(--hamon-gold);
            margin-bottom: 10px;
            text-transform: uppercase;
            letter-spacing: 0.05em;
        }

        .project-status {
            display: inline-block;
            font-size: 0.8rem;
            padding: 4px 10px;
            border-radius: 4px;
            margin-bottom: 15px;
            font-family: var(--font-code);
            text-transform: uppercase;
            letter-spacing: 0.03em;
        }

        .status-winner {
            background: rgba(57, 255, 20, 0.1);
            color: var(--matrix-green);
            border: 1px solid var(--matrix-green);
        }

        .status-active {
            background: rgba(255, 215, 0, 0.1);
            color: var(--hamon-gold);
            border: 1px solid var(--hamon-gold);
        }

        .status-building {
            background: rgba(0, 180, 216, 0.1);
            color: var(--arc-blue);
            border: 1px solid var(--arc-blue);
        }

        .project-description {
            color: var(--silver);
            margin-bottom: 15px;
            line-height: 1.7;
        }

        .project-stack {
            display: flex;
            flex-wrap: wrap;
            gap: 8px;
            margin-bottom: 15px;
        }

        .stack-tag {
            font-size: 0.75rem;
            padding: 4px 8px;
            background: rgba(138, 43, 226, 0.2);
            border: 1px solid rgba(138, 43, 226, 0.5);
            border-radius: 3px;
            font-family: var(--font-code);
            color: var(--hermit-purple);
            text-transform: uppercase;
            letter-spacing: 0.02em;
        }

        .project-link {
            display: inline-block;
            margin-top: 15px;
            padding: 10px 16px;
            background: var(--hermit-purple);
            color: var(--white-smoke);
            text-decoration: none;
            border-radius: 4px;
            font-family: var(--font-heading);
            font-size: 0.85rem;
            text-transform: uppercase;
            letter-spacing: 0.05em;
            transition: all 0.3s ease;
        }

        .project-link:hover {
            background: var(--hamon-gold);
            color: var(--void);
            transform: translateX(5px);
        }

        /* ACHIEVEMENTS */
        .achievements-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 25px;
        }

        .achievement-item {
            padding: 20px;
            background: rgba(138, 43, 226, 0.05);
            border: 1px solid rgba(138, 43, 226, 0.3);
            border-left: 3px solid var(--hamon-gold);
            border-radius: 4px;
            transition: all 0.3s ease;
        }

        .achievement-item:hover {
            background: rgba(138, 43, 226, 0.1);
            border-color: var(--hamon-gold);
            transform: translateX(5px);
        }

        .achievement-icon {
            font-size: 2rem;
            margin-bottom: 10px;
        }

        .achievement-title {
            font-family: var(--font-heading);
            color: var(--hamon-gold);
            margin-bottom: 8px;
            text-transform: uppercase;
            letter-spacing: 0.05em;
        }

        .achievement-desc {
            color: var(--silver);
            font-size: 0.9rem;
            line-height: 1.6;
        }

        /* CONTACT */
        .contact-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 25px;
            margin-bottom: 40px;
        }

        .contact-item {
            display: flex;
            align-items: flex-start;
            gap: 15px;
            padding: 20px;
            background: var(--carbon);
            border: 1px solid rgba(138, 43, 226, 0.3);
            border-radius: 4px;
            transition: all 0.3s ease;
        }

        .contact-item:hover {
            border-color: var(--hamon-gold);
            background: rgba(138, 43, 226, 0.1);
        }

        .contact-icon {
            font-size: 1.5rem;
            color: var(--hamon-gold);
            min-width: 30px;
        }

        .contact-info h3 {
            font-family: var(--font-heading);
            color: var(--hamon-gold);
            margin-bottom: 5px;
            text-transform: uppercase;
            font-size: 0.9rem;
        }

        .contact-info p {
            color: var(--white-smoke);
            font-size: 0.95rem;
        }

        .contact-info a {
            color: var(--arc-blue);
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .contact-info a:hover {
            color: var(--hamon-gold);
            text-decoration: underline;
        }

        /* FOOTER */
        footer {
            border-top: 1px solid rgba(138, 43, 226, 0.3);
            padding: 40px 20px;
            text-align: center;
            color: var(--silver);
            background: linear-gradient(180deg, transparent 0%, rgba(138, 43, 226, 0.05) 100%);
            margin-top: 80px;
        }

        footer p {
            margin: 10px 0;
        }

        .footer-tagline {
            font-family: var(--font-display);
            color: var(--hamon-gold);
            font-size: 1.3rem;
            margin-bottom: 20px;
            letter-spacing: 0.05em;
        }

        .footer-credit {
            font-family: var(--font-code);
            font-size: 0.85rem;
            color: var(--silver);
        }

        /* ANIMATIONS */
        @keyframes fadeInDown {
            from {
                opacity: 0;
                transform: translateY(-30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        @keyframes glow {
            0%, 100% {
                box-shadow: 0 0 10px rgba(138, 43, 226, 0.3);
            }
            50% {
                box-shadow: 0 0 20px rgba(138, 43, 226, 0.6);
            }
        }

        .glow {
            animation: glow 2s ease-in-out infinite;
        }

        /* RESPONSIVE */
        @media (max-width: 768px) {
            header {
                padding: 40px 20px;
            }

            .hero-title {
                font-size: 2rem;
            }

            nav ul {
                gap: 15px;
            }

            nav a {
                font-size: 0.8rem;
            }

            section h2 {
                font-size: 1.8rem;
            }

            .tech-grid {
                grid-template-columns: 1fr;
            }

            .projects-grid {
                grid-template-columns: 1fr;
            }

            .about-grid {
                gap: 20px;
            }
        }

        /* SCROLL ANIMATIONS */
        .fade-in {
            opacity: 0;
            animation: fadeInUp 0.8s ease-out forwards;
        }

        /* LOADING STATE */
        .loading {
            display: inline-block;
            width: 20px;
            height: 20px;
            border: 3px solid rgba(138, 43, 226, 0.3);
            border-top: 3px solid var(--hamon-gold);
            border-radius: 50%;
            animation: spin 1s linear infinite;
        }

        @keyframes spin {
            to { transform: rotate(360deg); }
        }
    </style>
</head>
<body>
    <!-- NAVIGATION -->
    <nav>
        <ul>
            <li><a href="#about">About</a></li>
            <li><a href="#tech">Tech Stack</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#achievements">Achievements</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- HEADER / HERO -->
    <header>
        <h1 class="hero-title">ch1llc0d3</h1>
        <p class="hero-subtitle">AI Engineer • Cybersecurity • Full Stack • Indie Hacker</p>
        <p class="hero-tagline">Founder @ VEIDT LLC | 4x Hackathon Winner | Bug Bounty Hunter | Legacy Specialist</p>
        
        <div class="hero-badges">
            <span class="badge">AI Engineer</span>
            <span class="badge">Full Stack</span>
            <span class="badge">Cybersecurity</span>
            <span class="badge">DevOps</span>
            <span class="badge">Paraguay 🇵🇾</span>
        </div>
    </header>

    <main>
        <!-- ABOUT -->
        <section id="about">
            <h2>🎯 About Me</h2>
            <div class="about-grid">
                <div class="about-text">
                    <p><strong>I bridge legacy systems & modern AI.</strong></p>
                    <p style="margin-top: 15px;">From COBOL telemetry at ANDE to Claude API pipelines at Mandi, I build systems that work under pressure—whether it's a pentesting framework, a food traceability SaaS, or a bug bounty submission.</p>
                    <p style="margin-top: 15px;">I'm a founder obsessed with financial sovereignty via SaaS, high-ticket consulting, and edtech monetization. ISFP with AuDHD (high pattern recognition). Polyglot: Spanish • Guaraní • English • Portuguese • Mandarin.</p>
                    <p style="margin-top: 15px; color: var(--hamon-gold); font-style: italic;">Philosophy: "VibeCoding" — AI-first, iterative, MVP-first. Everything is Grace.</p>
                </div>
                <div class="about-code">
<pre>ceci = {
  "handle": "ch1llc0d3",
  "location": "Paraguay 🇵🇾",
  "current_roles": [
    "AI Developer @ Wexare",
    "Legacy Specialist @ PTI/ANDE"
  ],
  "founder": "VEIDT LLC",
  "personality": "ISFP | AuDHD",
  "mission": "Sovereignty via SaaS",
  "philosophy": "VibeCoding",
  "tech_mood": "Next.js + Claude + Convex",
  "non_tech": ["FL Studio", "JoJo", "nature"]
}</pre>
                </div>
            </div>
        </section>

        <!-- TECH STACK -->
        <section id="tech">
            <h2>💻 Tech Stack</h2>
            <div class="tech-grid">
                <div class="tech-category">
                    <h3>🔤 Languages</h3>
                    <div class="tech-items">
                        <span class="tech-item">C</span>
                        <span class="tech-item">C++</span>
                        <span class="tech-item">Python</span>
                        <span class="tech-item">JavaScript</span>
                        <span class="tech-item">TypeScript</span>
                        <span class="tech-item">Java</span>
                        <span class="tech-item">PL/SQL</span>
                        <span class="tech-item">COBOL</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>🎨 Frontend</h3>
                    <div class="tech-items">
                        <span class="tech-item">Next.js</span>
                        <span class="tech-item">React</span>
                        <span class="tech-item">Tailwind</span>
                        <span class="tech-item">TypeScript</span>
                        <span class="tech-item">Figma</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>⚙️ Backend</h3>
                    <div class="tech-items">
                        <span class="tech-item">FastAPI</span>
                        <span class="tech-item">Convex</span>
                        <span class="tech-item">Node.js</span>
                        <span class="tech-item">PostgreSQL</span>
                        <span class="tech-item">Oracle</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>🚀 Infrastructure</h3>
                    <div class="tech-items">
                        <span class="tech-item">Docker</span>
                        <span class="tech-item">Kubernetes</span>
                        <span class="tech-item">Terraform</span>
                        <span class="tech-item">Linux</span>
                        <span class="tech-item">AWS</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>🤖 AI / ML</h3>
                    <div class="tech-items">
                        <span class="tech-item">Claude API</span>
                        <span class="tech-item">PyTorch</span>
                        <span class="tech-item">OpenCV</span>
                        <span class="tech-item">LangChain</span>
                        <span class="tech-item">RAG</span>
                    </div>
                </div>

                <div class="tech-category">
                    <h3>🔐 Cybersecurity</h3>
                    <div class="tech-items">
                        <span class="tech-item">Burp Suite</span>
                        <span class="tech-item">Kali Linux</span>
                        <span class="tech-item">Metasploit</span>
                        <span class="tech-item">Nuclei</span>
                        <span class="tech-item">Nmap</span>
                    </div>
                </div>
            </div>
        </section>

        <!-- PROJECTS -->
        <section id="projects">
            <h2>🚀 Current Projects</h2>
            <div class="projects-grid">
                <div class="project-card">
                    <div class="project-status status-winner">🏆 #1 Winner</div>
                    <h3 class="project-title">Mandi</h3>
                    <p class="project-description">Food traceability SaaS for Paraguayan micro-enterprises (MIPymes). Winner of Startup Weekend Women Edition Asunción 2026.</p>
                    <div class="project-stack">
                        <span class="stack-tag">Next.js</span>
                        <span class="stack-tag">Convex</span>
                        <span class="stack-tag">Claude API</span>
                        <span class="stack-tag">PyTorch</span>
                    </div>
                    <a href="https://github.com/ch1llc0d3/mandi-saas" class="project-link">View on GitHub →</a>
                </div>

                <div class="project-card">
                    <div class="project-status status-building">🔄 Building</div>
                    <h3 class="project-title">NobrainerAcademy</h3>
                    <p class="project-description">Edtech platform with gamification. Risk series: casino math, global lotteries, sports betting, crypto.</p>
                    <div class="project-stack">
                        <span class="stack-tag">Edtech</span>
                        <span class="stack-tag">Gamification</span>
                        <span class="stack-tag">Self-hosted</span>
                    </div>
                    <a href="https://nobraineracademy.lat" class="project-link">Visit Platform →</a>
                </div>

                <div class="project-card">
                    <div class="project-status status-building">🌱 Growing</div>
                    <h3 class="project-title">NitroGarage</h3>
                    <p class="project-description">LATAM vehicle SaaS ecosystem. Fan site for movie/game/anime vehicles. Long-term: vehicle data marketplace.</p>
                    <div class="project-stack">
                        <span class="stack-tag">Next.js</span>
                        <span class="stack-tag">Tailwind</span>
                        <span class="stack-tag">FastAPI</span>
                    </div>
                    <a href="https://nitrogarage.lat" class="project-link">Visit Site →</a>
                </div>

                <div class="project-card">
                    <div class="project-status status-active">✅ Live</div>
                    <h3 class="project-title">alivioparatudolor</h3>
                    <p class="project-description">Physiotherapy booking platform for my mom's spa. WhatsApp-first, real-time sync, PagoPar integration.</p>
                    <div class="project-stack">
                        <span class="stack-tag">Next.js</span>
                        <span class="stack-tag">Convex</span>
                        <span class="stack-tag">Auth.js</span>
                    </div>
                    <a href="https://alivioparatudolor.com" class="project-link">Visit Site →</a>
                </div>

                <div class="project-card">
                    <div class="project-status status-active">🔴 Active</div>
                    <h3 class="project-title">Bug Bounty Hunting</h3>
                    <p class="project-description">Pentesting & security research on HackerOne, Bugcrowd, YesWeHack. OWASP Top 10, PTES, real-world scenarios.</p>
                    <div class="project-stack">
                        <span class="stack-tag">Burp Suite</span>
                        <span class="stack-tag">Nuclei</span>
                        <span class="stack-tag">Pentesting</span>
                    </div>
                    <a href="https://hackerone.com/ch1llc0d3" class="project-link">HackerOne Profile →</a>
                </div>

                <div class="project-card">
                    <div class="project-status status-building">📚 Open Source</div>
                    <h3 class="project-title">Legacy System Bridge</h3>
                    <p class="project-description">Bridging COBOL/Oracle systems with modern stacks. SAMR telemetry, PL/SQL optimization, modernization patterns.</p>
                    <div class="project-stack">
                        <span class="stack-tag">COBOL</span>
                        <span class="stack-tag">Oracle</span>
                        <span class="stack-tag">Python</span>
                    </div>
                    <a href="https://github.com/ch1llc0d3/legacy-bridge" class="project-link">View on GitHub →</a>
                </div>
            </div>
        </section>

        <!-- ACHIEVEMENTS -->
        <section id="achievements">
            <h2>🏆 Achievements</h2>
            <div class="achievements-list">
                <div class="achievement-item">
                    <div class="achievement-icon">🥇</div>
                    <h3 class="achievement-title">4x Hackathon Winner</h3>
                    <p class="achievement-desc">Mandi (Startup Weekend Women 2026) • Ñambyaty Go (SNJ 2024) • My Digital Tree (Penguin 2023) • ParkFinder (2023)</p>
                </div>

                <div class="achievement-item">
                    <div class="achievement-icon">🔐</div>
                    <h3 class="achievement-title">Security Research</h3>
                    <p class="achievement-desc">Active bug bounty hunter. Pentesting: OWASP Top 10, PTES/OSSTM. PortSwigger Academy in progress.</p>
                </div>

                <div class="achievement-item">
                    <div class="achievement-icon">🎓</div>
                    <h3 class="achievement-title">Community Leadership</h3>
                    <p class="achievement-desc">Cybersecurity mentor at AI Tinkerers, WOMCY. Speaker: Women Tech Makers, First Lego League, Girls Code.</p>
                </div>

                <div class="achievement-item">
                    <div class="achievement-icon">💼</div>
                    <h3 class="achievement-title">Full Stack Expertise</h3>
                    <p class="achievement-desc">COBOL → Python. Oracle PL/SQL → Convex. Legacy systems + modern AI. Critical infrastructure reliability.</p>
                </div>

                <div class="achievement-item">
                    <div class="achievement-icon">🚀</div>
                    <h3 class="achievement-title">Founder Mindset</h3>
                    <p class="achievement-desc">CEO @ VEIDT LLC. Building SaaS for financial sovereignty. Mandi: food traceability MVP → production in weeks.</p>
                </div>

                <div class="achievement-item">
                    <div class="achievement-icon">🌍</div>
                    <h3 class="achievement-title">Polyglot & Global</h3>
                    <p class="achievement-desc">Spanish • Guaraní • English • Portuguese • Mandarin. Cultural bridges for LATAM tech ecosystem.</p>
                </div>
            </div>
        </section>

        <!-- CONTACT -->
        <section id="contact">
            <h2>🔗 Get In Touch</h2>
            <div class="contact-grid">
                <div class="contact-item">
                    <div class="contact-icon">📧</div>
                    <div class="contact-info">
                        <h3>Email</h3>
                        <p><a href="mailto:chillcrib7@duck.com">chillcrib7@duck.com</a></p>
                    </div>
                </div>

                <div class="contact-item">
                    <div class="contact-icon">🐙</div>
                    <div class="contact-info">
                        <h3>GitHub</h3>
                        <p><a href="https://github.com/ch1llc0d3" target="_blank">github.com/ch1llc0d3</a></p>
                    </div>
                </div>

                <div class="contact-item">
                    <div class="contact-icon">💼</div>
                    <div class="contact-info">
                        <h3>LinkedIn</h3>
                        <p><a href="https://linkedin.com/in/c-b-3b9a7718b" target="_blank">linkedin.com/in/c-b-3b9a7718b</a></p>
                    </div>
                </div>

                <div class="contact-item">
                    <div class="contact-icon">🔒</div>
                    <div class="contact-info">
                        <h3>HackerOne</h3>
                        <p><a href="https://hackerone.com/ch1llc0d3" target="_blank">hackerone.com/ch1llc0d3</a></p>
                    </div>
                </div>

                <div class="contact-item">
                    <div class="contact-icon">🕷️</div>
                    <div class="contact-info">
                        <h3>Bugcrowd</h3>
                        <p><a href="https://bugcrowd.com/ch1llc0d3" target="_blank">bugcrowd.com/ch1llc0d3</a></p>
                    </div>
                </div>

                <div class="contact-item">
                    <div class="contact-icon">📱</div>
                    <div class="contact-info">
                        <h3>WhatsApp</h3>
                        <p><a href="https://wa.me/595972340373">+595 972 340 373</a></p>
                    </div>
                </div>
            </div>
        </section>
    </main>

    <!-- FOOTER -->
    <footer>
        <p class="footer-tagline">Build. Secure. Scale.</p>
        <p><strong>VEIDT LLC</strong> — AI Engineering & Security Consulting</p>
        <p style="margin-top: 20px; font-style: italic;">Made with 💜 by ch1llc0d3</p>
        <p class="footer-credit">Hermit Purple × Hamon Gold × Void | VibeCoding Philosophy</p>
    </footer>

    <script>
        // Smooth scroll for nav links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({ behavior: 'smooth', block: 'start' });
                }
            });
        });

        // Intersection Observer for fade-in animations
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -100px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.style.opacity = '1';
                    entry.target.style.animation = 'fadeInUp 0.8s ease-out';
                }
            });
        }, observerOptions);

        document.querySelectorAll('section').forEach(section => {
            section.style.opacity = '0';
            observer.observe(section);
        });

        // Interactive badge hover effects
        document.querySelectorAll('.badge').forEach(badge => {
            badge.addEventListener('mouseenter', function() {
                this.style.transform = 'translateY(-2px) scale(1.05)';
            });
            badge.addEventListener('mouseleave', function() {
                this.style.transform = 'translateY(0) scale(1)';
            });
        });
    </script>
</body>
</html>
