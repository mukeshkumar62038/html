<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Developer Portfolio</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        /* Reset and base styles */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', sans-serif;
        }

        body {
            background: #2110d6;
            color: #8892b0;
            line-height: 1.6;
        }

        /* Navigation */
        .navbar {
            padding: 1.5rem 10%;
            position: fixed;
            width: 100%;
            background: rgba(10, 25, 47, 0.95);
            backdrop-filter: blur(10px);
            z-index: 100;
        }

        .nav-links {
            display: flex;
            justify-content: flex-end;
            list-style: none;
            gap: 2rem;
        }

        .nav-links a {
            color: #64ffda;
            text-decoration: none;
            font-size: 1.1rem;
            transition: all 0.3s ease;
        }

        .nav-links a:hover {
            color: #fff;
        }

        /* Hero Section */
        .hero {
            min-height: 100vh;
            display: flex;
            align-items: center;
            padding: 0 10%;
        }

        .hero-content {
            opacity: 0;
            transform: translateY(20px);
            animation: fadeInUp 1s ease forwards;
        }

        .hero h1 {
            font-size: 4rem;
            color: #ccd6f6;
            margin-bottom: 1rem;
        }

        .hero h2 {
            font-size: 2.5rem;
            color: #64ffda;
            margin-bottom: 2rem;
        }

        .hero p {
            max-width: 600px;
            margin-bottom: 2rem;
        }

        /* Projects Section */
        .projects {
            padding: 5rem 10%;
        }

        .project-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }

        .project-card {
            background: #112240;
            padding: 2rem;
            border-radius: 8px;
            transition: transform 0.3s ease;
        }

        .project-card:hover {
            transform: translateY(-10px);
        }

        /* Skills Section */
        .skills {
            padding: 5rem 10%;
        }

        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(120px, 1fr));
            gap: 2rem;
            text-align: center;
        }

        .skill-item i {
            font-size: 3rem;
            color: #64ffda;
            margin-bottom: 1rem;
        }

        /* Contact Section */
        .contact {
            padding: 5rem 10%;
            text-align: center;
        }

        .btn {
            display: inline-block;
            padding: 1rem 2rem;
            background: transparent;
            border: 2px solid #64ffda;
            color: #64ffda;
            text-decoration: none;
            border-radius: 4px;
            transition: all 0.3s ease;
        }

        .btn:hover {
            background: rgba(100, 255, 218, 0.1);
        }

        /* Animations */
        @keyframes fadeInUp {
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .fade-in {
            opacity: 0;
            transform: translateY(20px);
            transition: all 1s ease;
        }

        .visible {
            opacity: 1;
            transform: translateY(0);
        }
    </style>
</head>
<body>
    <nav class="navbar">
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#projects">Projects</a></li>
            <li><a href="#skills">Skills</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <section id="home" class="hero">
        <div class="hero-content">
            <h1>Hi, I'm  Mukesh Yadav</h1>
            <h2>Web  Developer</h2>
            <p>I'm a passionate Web  developer specializing in building exceptional digital experiences. Currently, I'm focused on building accessible, human-centered products.</p>
            <a href="#contact" class="btn">Get In Touch</a>
        </div>
        
    </section>
    

    <section id="projects" class="projects">
        <h2>Featured Projects</h2>
        <div class="project-grid">
            <div class="project-card fade-in">
                <h3>Project 1</h3>
                <p>Description of your amazing project goes here.</p>
                <div class="tech-stack">
                    <span>React</span>
                    <span>Node.js</span>
                    <span>MongoDB</span>
                </div>
            </div>
            <!-- Add more project cards as needed -->
        </div>
    </section>

    <section id="skills" class="skills">
        <h2>Skills</h2>
        <div class="skills-grid">
            <div class="skill-item fade-in">
                <i class="fab fa-html5"></i>
                <p>HTML5</p>
            </div>
            <div class="skill-item fade-in">
                <i class="fab fa-css3-alt"></i>
                <p>CSS3</p>
            </div>
            <div class="skill-item fade-in">
                <i class="fab fa-js"></i>
                <p>JavaScript</p>
            </div>
            <!-- Add more skills as needed -->
        </div>
    </section>

    <section id="contact" class="contact">
        <h2>Get In Touch</h2>
        <p>I'm currently looking for new opportunities. Whether you have a question or just want to say hi, I'll try my best to get back to you!</p>
        <a href="mailto:your.email@example.com" class="btn">Say Hello</a>
    </section>

    <script>
        // Intersection Observer for fade-in animations
        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, { threshold: 0.1 });

        // Observe all elements with fade-in class
        document.querySelectorAll('.fade-in').forEach((element) => {
            observer.observe(element);
        });
    </script>
</body>
</html>
