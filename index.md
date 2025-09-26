<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Niharika K Thilak | CSE Portfolio</title>
    <!-- Use a modern, clean font -->
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
    <style>
        /* Custom Properties for easy color changes */
        :root {
            --primary-color: #FF69B4; /* Hot Pink/Deep Pink - for highlights */
            --secondary-color: #111111; /* Deep Black - for background */
            --text-color: #f4f4f4; /* Light text for contrast */
            --accent-color: #c0c0c0; /* Lighter grey for subtle details */
        }

        /* Global Styles & Cherry Blossom Background Setup */
        body {
            font-family: 'Poppins', sans-serif;
            margin: 0;
            padding: 0;
            background-color: var(--secondary-color);
            color: var(--text-color);
            line-height: 1.6;
            min-height: 100vh;
            
            /* Cherry Blossom Background Setup: Requires a file named 'cherry-blossom-long.png' in the root folder */
            background-image: url('cherry-blossom-long.png'), 
                              linear-gradient(135deg, var(--secondary-color) 0%, #000000 100%);
            background-size: cover;
            background-position: center top;
            background-repeat: no-repeat;
            background-attachment: fixed;
        }

        /* Utility classes for content alignment */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }

        /* Typography */
        h1, h2, h3 {
            color: var(--primary-color);
            font-weight: 700;
        }

        h2 {
            font-size: 2.2em;
            margin-bottom: 25px;
            /* Minimalistic: Thin, clean line for definition */
            border-bottom: 1px solid var(--primary-color); 
            display: inline-block;
            padding-bottom: 5px;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Header and Navigation - Minimalist Sticky Bar */
        header {
            background-color: rgba(0, 0, 0, 0.98); 
            padding: 15px 0;
            position: sticky;
            top: 0;
            z-index: 1000;
            /* Minimalistic: Only a subtle pink glow on the bottom edge */
            box-shadow: 0 1px 0 0 rgba(255, 105, 180, 0.1); 
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo {
            font-size: 1.8em;
            font-weight: 700;
            color: var(--primary-color);
        }

        nav ul {
            list-style: none;
            display: flex;
            margin: 0;
            padding: 0;
        }

        nav ul li a {
            color: var(--text-color);
            text-decoration: none;
            font-weight: 500;
            padding: 10px 15px;
            transition: color 0.3s;
            /* Minimalistic: Use underline on hover instead of background fill */
            border-bottom: 2px solid transparent; 
        }

        nav ul li a:hover {
            color: var(--primary-color);
            border-bottom-color: var(--primary-color);
        }

        /* Hero Section (Introduction) */
        .hero-section {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            align-items: center;
            padding: 100px 20px;
            text-align: left;
            min-height: 80vh;
        }

        .hero-content h1 {
            font-size: 3.5em;
            margin-bottom: 0.1em;
            line-height: 1.1;
        }

        .hero-image img {
            width: 220px; 
            height: 220px;
            border-radius: 50%;
            object-fit: cover;
            /* Minimalist: Thin, clean border */
            border: 3px solid var(--primary-color); 
            box-shadow: 0 0 15px rgba(255, 105, 180, 0.5); /* Subtle glow */
            margin-top: 30px;
        }

        .cta-button {
            display: inline-block;
            padding: 12px 25px;
            margin-top: 25px;
            background-color: var(--primary-color);
            color: var(--secondary-color);
            text-decoration: none;
            font-weight: 600;
            border-radius: 4px; /* Slightly sharper edges */
            transition: background-color 0.3s, box-shadow 0.3s;
            text-transform: uppercase;
            letter-spacing: 0.5px;
        }

        .cta-button:hover {
            background-color: #ff85c1;
            box-shadow: 0 5px 10px rgba(255, 105, 180, 0.3); /* Minimalistic shadow */
            transform: none; /* No scaling/lifting */
        }

        /* Content Sections - Increased transparency for minimalism */
        .content-section {
            padding: 70px 30px;
            background-color: rgba(0, 0, 0, 0.6); /* Lighter transparency */
            border-radius: 10px; /* Reduced rounding */
            margin: 40px auto;
            box-shadow: 0 0 15px rgba(0, 0, 0, 0.4); /* Subtler shadow */
            max-width: 900px;
        }

        /* Separator */
        .separator {
            border: none;
            height: 1px;
            background: linear-gradient(to right, transparent, var(--primary-color), transparent);
            margin: 50px auto;
            max-width: 60%;
            opacity: 0.5;
        }

        /* Skills Grid */
        .skills-grid {
            display: flex;
            flex-wrap: wrap;
            gap: 12px;
            margin-top: 30px;
        }

        .skill-card {
            background-color: rgba(255, 105, 180, 0.1); 
            color: var(--text-color);
            padding: 8px 15px;
            border-radius: 4px; /* Minimalistic rounding */
            border: 1px solid rgba(255, 105, 180, 0.5); /* Faint border */
            font-weight: 500;
            transition: background-color 0.2s;
            cursor: default;
        }

        .skill-card:hover {
            background-color: var(--primary-color);
            color: var(--secondary-color);
            transform: none; /* Removed scale transform */
        }

        /* Projects */
        .project-card {
            background-color: rgba(255, 255, 255, 0.03);
            padding: 20px;
            margin-top: 15px;
            /* Minimalist: Thin, clean left border */
            border-left: 3px solid var(--primary-color); 
            border-radius: 5px;
            transition: background-color 0.2s;
        }

        .project-card:hover {
            background-color: rgba(255, 105, 180, 0.05);
            border-left-width: 3px; /* Keep consistent width on hover */
        }

        /* Contact Form Styles */
        .contact-form label {
            display: block;
            margin-top: 15px;
            margin-bottom: 5px;
            font-weight: 500;
            color: var(--accent-color); /* Subtle label color */
        }

        .contact-form input[type="text"],
        .contact-form input[type="email"],
        .contact-form textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid rgba(255, 105, 180, 0.3);
            border-radius: 4px;
            background-color: rgba(0, 0, 0, 0.5);
            color: var(--text-color);
            box-sizing: border-box;
            font-family: 'Poppins', sans-serif;
            transition: border-color 0.3s;
        }

        .contact-form textarea {
            resize: vertical;
            min-height: 120px;
        }

        .contact-form input:focus,
        .contact-form textarea:focus {
            border-color: var(--primary-color);
            background-color: rgba(255, 105, 180, 0.05);
            outline: none;
            box-shadow: none; /* Removed heavy focus glow */
        }

        .contact-form .cta-button {
            width: 100%;
            border: none;
            cursor: pointer;
            text-align: center;
        }


        /* Footer and Social Links */
        footer {
            text-align: center;
            padding: 20px 0;
            background-color: var(--secondary-color);
            color: var(--accent-color);
            border-top: 1px solid rgba(255, 105, 180, 0.1); /* Very light border */
        }

        .social-links {
            margin-top: 15px;
        }
        .social-links a {
            color: var(--primary-color);
            text-decoration: none;
            font-size: 1em;
            margin: 0 15px;
            transition: color 0.3s;
        }

        .social-links a:hover {
            color: var(--text-color);
            border-bottom: 1px solid var(--text-color);
        }

        /* Media Queries for responsiveness */
        @media (max-width: 768px) {
            .hero-section {
                flex-direction: column;
                text-align: center;
                padding: 60px 20px;
            }
            .hero-content h1 {
                font-size: 2.2em;
            }
            .hero-content p {
                font-size: 1em;
            }
            nav ul {
                display: none; 
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <nav>
                <div class="logo">Niharika K Thilak</div>
                <ul>
                    <li><a href="#about">About</a></li>
                    <li><a href="#skills">Skills</a></li>
                    <li><a href="#projects">Projects</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <main>
        <div class="container">
            <section id="hero" class="hero-section">
                <div class="hero-content">
                    <h1>Code meets Craft.</h1>
                    <p>
                        I'm Niharika, a Computer Science student at **VAST Thrissur**.
                        My passion is turning complex challenges into clean, efficient code.
                    </p>
                    <a href="#projects" class="cta-button">Explore My Codebase</a>
                </div>
                <div class="hero-image">
                    <!-- CHANGE THIS URL -->
                    <img src="https://placehold.co/220x220/FF69B4/111111?text=Your+Photo" alt="Niharika K Thilak">
                </div>
            </section>
        </div>
        
        <div class="separator"></div>

        <section id="about" class="content-section">
            <div class="container">
                <h2>About Me 🌸</h2>
                <p>
                    Currently pursuing Computer Science and Engineering at the **Vidya Academy Of Science and Technology, Thrissur**. I am driven by the sheer joy of **Coding**. Whether it's optimizing algorithms or building interactive projects, I love the problem-solving journey that technology offers.
                </p>
                <p>
                    My goal is to blend strong technical foundations (DSA, C/C++) with practical application in modern software development. I'm always looking for opportunities to contribute and learn!
                </p>
            </div>
        </section>

        <section id="skills" class="content-section">
            <div class="container">
                <h2>Core Competencies 💻</h2>
                <div class="skills-grid">
                    <div class="skill-card">C / C++</div>
                    <div class="skill-card">Data Structures & Algorithms (DSA)</div>
                    <div class="skill-card">Python</div>
                    <div class="skill-card">HTML & CSS</div>
                    <div class="skill-card">Git & GitHub</div>
                    <div class="skill-card">Operating Systems Concepts</div>
                    <div class="skill-card">Database Management (SQL)</div>
                    <div class="skill-card">... (Add frameworks/libraries like React, Django, etc.)</div>
                </div>
            </div>
        </section>

        <section id="projects" class="content-section">
            <div class="container">
                <h2>Featured Projects ✨</h2>
                <div class="project-card">
                    <h3>DSA Visualizer Tool</h3>
                    <p>A web-based application demonstrating how sorting and searching algorithms work in real-time. Built using JavaScript and visualizing the steps with clear, graphical representation.</p>
                    <a href="https://github.com/yourusername/dsa-project" target="_blank">View on GitHub</a>
                </div>
                <div class="project-card">
                    <h3>College Event Management System</h3>
                    <p>A full-stack system designed to manage registrations, schedules, and results for college technical events. Focus was on secure login and robust database design.</p>
                    <a href="https://github.com/yourusername/event-management" target="_blank">View on GitHub</a>
                </div>
                <!-- Add more project cards here! -->
            </div>
        </section>

        <section id="contact" class="content-section">
            <div class="container">
                <h2>Get In Touch ✉️</h2>
                <p>I am actively seeking internship opportunities and collaborations. Use the form below or connect via my social channels!</p>
                
                <!-- 
                    IMPORTANT: To make this form work on GitHub Pages, you must use a service like Formspree.
                    1. Go to Formspree.io and create an account.
                    2. Create a new form endpoint.
                    3. Replace "https://formspree.io/f/yourformid" with your actual Formspree endpoint URL.
                -->
                <form action="https://formspree.io/f/yourformid" method="POST" class="contact-form">
                    <label for="name">Your Name</label>
                    <input type="text" id="name" name="name" required>

                    <label for="email">Your Email</label>
                    <input type="email" id="email" name="_replyto" required>
                    
                    <label for="subject">Subject</label>
                    <input type="text" id="subject" name="subject" required>

                    <label for="message">Message</label>
                    <textarea id="message" name="message" required></textarea>

                    <button type="submit" class="cta-button" style="margin-top: 25px;">Send Message</button>
                </form>

                <div class="social-links" style="margin-top: 35px;">
                    <a href="mailto:your.email@example.com">Email</a> 
                    | 
                    <a href="link-to-your-linkedin" target="_blank">LinkedIn</a> 
                    | 
                    <a href="link-to-your-github" target="_blank">GitHub</a>
                </div>
            </div>
        </section>
    </main>

    <footer>
        <p>&copy; 2024 Niharika K Thilak. Crafted with Code & Passion.</p>
    </footer>
</body>
</html>
