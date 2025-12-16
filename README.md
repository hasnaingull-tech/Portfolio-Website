<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Muhammad Hasnain Gull | Networking & Surveillance Engineer</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        :root {
            --primary: #003B4A;
            --primary-light: #005A6B;
            --accent: #FF7A3D;
            --accent-light: #FF9A6C;
            --light: #F4F6F9;
            --white: #fff;
            --dark: #333;
            --gray: #6c757d;
        }

        body {
            font-family: 'Roboto', sans-serif;
            background: var(--light);
            color: var(--dark);
            line-height: 1.6;
            overflow-x: hidden;
        }

        .container {
            width: 90%;
            max-width: 1200px;
            margin: auto;
        }

        /* Header & Navigation */
        header {
            position: fixed;
            width: 100%;
            top: 0;
            background: rgba(0, 59, 74, 0.98);
            z-index: 1000;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }

        .navbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 0;
        }

        .logo {
            color: #fff;
            font-size: 26px;
            font-weight: 700;
            text-decoration: none;
            font-family: 'Poppins', sans-serif;
        }

        .logo span {
            color: var(--accent);
        }

        .nav-links {
            list-style: none;
            display: flex;
        }

        .nav-links li {
            margin-left: 30px;
            position: relative;
        }

        .nav-links a {
            color: #fff;
            text-decoration: none;
            font-weight: 500;
            font-size: 16px;
            transition: color 0.3s ease;
            padding: 5px 0;
        }

        .nav-links a:hover {
            color: var(--accent);
        }

        .nav-links a::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 2px;
            background-color: var(--accent);
            transition: width 0.3s ease;
        }

        .nav-links a:hover::after {
            width: 100%;
        }

        .menu-toggle {
            display: none;
            font-size: 24px;
            color: #fff;
            cursor: pointer;
            transition: transform 0.3s ease;
        }

        .menu-toggle:hover {
            transform: scale(1.1);
        }

        /* Hero Section */
        .hero {
            padding: 200px 0 120px;
            background: linear-gradient(135deg, var(--primary), var(--primary-light));
            color: #fff;
            text-align: center;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: url('data:image/svg+xml,<svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" preserveAspectRatio="none"><path d="M0,0 L100,0 L100,100 Z" fill="rgba(255,122,61,0.1)"/></svg>');
            background-size: cover;
        }

        .icon-container {
            margin-bottom: 40px;
            position: relative;
            z-index: 2;
        }

        .professional-icon {
            width: 120px;
            height: 120px;
            margin: auto;
            background: rgba(255, 122, 61, 0.1);
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            border: 4px solid var(--accent);
            box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2);
            transition: transform 0.5s ease;
        }

        .professional-icon:hover {
            transform: scale(1.1);
        }

        .professional-icon i {
            font-size: 50px;
            color: var(--accent);
        }

        .hero h1 {
            font-size: 48px;
            margin: 20px 0 15px;
            font-family: 'Poppins', sans-serif;
            position: relative;
            z-index: 2;
        }

        .hero .tagline {
            font-size: 24px;
            color: var(--accent-light);
            font-weight: 500;
            margin-bottom: 20px;
            position: relative;
            z-index: 2;
        }

        .hero p {
            max-width: 800px;
            margin: 0 auto 30px;
            font-size: 18px;
            opacity: 0.9;
            position: relative;
            z-index: 2;
        }

        .highlight {
            color: var(--accent);
            font-weight: 600;
        }

        .btn {
            display: inline-block;
            margin-top: 30px;
            padding: 16px 36px;
            border-radius: 30px;
            background: var(--accent);
            color: #fff;
            text-decoration: none;
            font-weight: 600;
            font-size: 16px;
            transition: all 0.3s ease;
            border: 2px solid var(--accent);
            position: relative;
            z-index: 2;
            box-shadow: 0 5px 15px rgba(255, 122, 61, 0.3);
        }

        .btn:hover {
            background: transparent;
            color: var(--accent);
            transform: translateY(-3px);
            box-shadow: 0 8px 20px rgba(255, 122, 61, 0.4);
        }

        /* Section Common Styles */
        section {
            padding: 100px 0;
        }

        .section-title {
            text-align: center;
            margin-bottom: 60px;
        }

        .section-title h2 {
            font-size: 36px;
            color: var(--primary);
            font-family: 'Poppins', sans-serif;
            position: relative;
            display: inline-block;
            padding-bottom: 15px;
        }

        .section-title h2::after {
            content: '';
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translateX(-50%);
            width: 70px;
            height: 3px;
            background: var(--accent);
        }

        /* About Section */
        #about {
            background: #fff;
        }

        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 50px;
            align-items: center;
        }

        .about-text h3 {
            font-size: 28px;
            margin-bottom: 20px;
            color: var(--primary);
        }

        .about-text p {
            margin-bottom: 20px;
            color: var(--dark);
        }

        .about-stats {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 20px;
            margin-top: 30px;
        }

        .stat-item {
            text-align: center;
            padding: 20px;
            background: var(--light);
            border-radius: 8px;
            transition: transform 0.3s ease;
        }

        .stat-item:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
        }

        .stat-number {
            font-size: 36px;
            font-weight: 700;
            color: var(--accent);
            display: block;
        }

        .stat-label {
            font-size: 16px;
            color: var(--dark);
        }

        /* Skills Section */
        .skills-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
        }

        .skill-box {
            background: #fff;
            padding: 35px 30px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease;
            border-top: 4px solid transparent;
        }

        .skill-box:hover {
            transform: translateY(-10px);
            box-shadow: 0 15px 30px rgba(0, 0, 0, 0.1);
            border-top-color: var(--accent);
        }

        .skill-box i {
            font-size: 48px;
            color: var(--accent);
            margin-bottom: 20px;
        }

        .skill-box h3 {
            font-size: 22px;
            margin-bottom: 15px;
            color: var(--primary);
        }

        .skill-box p {
            color: var(--gray);
        }

        /* Experience Section */
        #experience {
            background: var(--light);
        }

        .timeline {
            position: relative;
            max-width: 800px;
            margin: 0 auto;
        }

        .timeline::after {
            content: '';
            position: absolute;
            width: 4px;
            background-color: var(--accent);
            top: 0;
            bottom: 0;
            left: 50%;
            margin-left: -2px;
        }

        .timeline-item {
            padding: 10px 40px;
            position: relative;
            width: 50%;
            box-sizing: border-box;
        }

        .timeline-item:nth-child(odd) {
            left: 0;
        }

        .timeline-item:nth-child(even) {
            left: 50%;
        }

        .timeline-content {
            padding: 20px;
            background-color: white;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.08);
        }

        .timeline-content h3 {
            color: var(--primary);
            margin-bottom: 10px;
        }

        .timeline-content .date {
            color: var(--accent);
            font-weight: 600;
            margin-bottom: 10px;
            display: block;
        }

        .timeline-item::after {
            content: '';
            position: absolute;
            width: 20px;
            height: 20px;
            right: -10px;
            background-color: white;
            border: 4px solid var(--accent);
            top: 20px;
            border-radius: 50%;
            z-index: 1;
        }

        .timeline-item:nth-child(even)::after {
            left: -10px;
        }

        /* Contact Section */
        #contact {
            background: linear-gradient(rgba(0, 59, 74, 0.9), rgba(0, 59, 74, 0.9)), url('https://images.unsplash.com/photo-1552664730-d307ca884978?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1000&q=80');
            background-size: cover;
            background-position: center;
            color: #fff;
            text-align: center;
        }

        #contact .section-title h2 {
            color: #fff;
        }

        #contact .section-title h2::after {
            background: var(--accent);
        }

        .contact-info {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .contact-box {
            background: rgba(255, 255, 255, 0.1);
            padding: 30px;
            border-radius: 10px;
            backdrop-filter: blur(5px);
            transition: all 0.3s ease;
        }

        .contact-box:hover {
            background: rgba(255, 255, 255, 0.15);
            transform: translateY(-5px);
        }

        .contact-box i {
            font-size: 36px;
            color: var(--accent);
            margin-bottom: 20px;
        }

        .contact-box p {
            font-size: 18px;
        }

        /* Footer */
        footer {
            background: var(--primary);
            color: #fff;
            text-align: center;
            padding: 40px 0;
        }

        .social-links {
            display: flex;
            justify-content: center;
            margin: 20px 0 30px;
        }

        .social-links a {
            display: inline-flex;
            align-items: center;
            justify-content: center;
            width: 40px;
            height: 40px;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            margin: 0 10px;
            color: #fff;
            font-size: 18px;
            transition: all 0.3s ease;
        }

        .social-links a:hover {
            background: var(--accent);
            transform: translateY(-5px);
        }

        .copyright {
            font-size: 14px;
            opacity: 0.8;
        }

        /* Responsive Design */
        @media (max-width: 992px) {
            .about-content {
                grid-template-columns: 1fr;
            }
            
            .timeline::after {
                left: 31px;
            }
            
            .timeline-item {
                width: 100%;
                padding-left: 70px;
                padding-right: 25px;
            }
            
            .timeline-item:nth-child(even) {
                left: 0;
            }
            
            .timeline-item::after {
                left: 21px;
            }
            
            .timeline-item:nth-child(even)::after {
                left: 21px;
            }
        }

        @media (max-width: 768px) {
            .menu-toggle {
                display: block;
            }
            
            .nav-links {
                position: absolute;
                top: 80px;
                left: 0;
                width: 100%;
                background: var(--primary);
                flex-direction: column;
                display: none;
                padding: 20px 0;
                box-shadow: 0 10px 20px rgba(0, 0, 0, 0.1);
            }
            
            .nav-links.active {
                display: flex;
            }
            
            .nav-links li {
                margin: 10px 0;
                text-align: center;
            }
            
            .nav-links a {
                display: block;
                padding: 10px 0;
            }
            
            .hero h1 {
                font-size: 36px;
            }
            
            .hero .tagline {
                font-size: 20px;
            }
            
            .hero p {
                font-size: 16px;
            }
            
            .section-title h2 {
                font-size: 30px;
            }
            
            .about-stats {
                grid-template-columns: 1fr;
            }
            
            .professional-icon {
                width: 100px;
                height: 100px;
            }
            
            .professional-icon i {
                font-size: 40px;
            }
        }

        @media (max-width: 576px) {
            .hero {
                padding: 180px 0 80px;
            }
            
            section {
                padding: 80px 0;
            }
            
            .hero h1 {
                font-size: 32px;
            }
            
            .hero .tagline {
                font-size: 18px;
            }
        }
    </style>
</head>

<body>
    <!-- Header & Navigation -->
    <header>
        <div class="container navbar">
            <a href="#" class="logo">Muhammad <span>Hasnain Gull</span></a>
            <div class="menu-toggle" id="menu">
                <i class="fas fa-bars"></i>
            </div>
            <ul class="nav-links" id="nav">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About</a></li>
                <li><a href="#skills">Skills</a></li>
                <li><a href="#experience">Experience</a></li>
                <li><a href="#contact">Contact</a></li>
            </ul>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero" id="home">
        <div class="container">
            <div class="icon-container">
                <div class="professional-icon">
                    <i class="fas fa-network-wired"></i>
                </div>
            </div>

            <h1>Muhammad Hasnain Gull</h1>
            <div class="tagline">Networking & Surveillance Engineer</div>
            <p>
                Specializing in enterprise networking, CCTV systems, IP addressing, cloud management, and intelligent building solutions. With extensive experience in designing and implementing secure, scalable network infrastructures.
            </p>
            
            <a href="#contact" class="btn">Get In Touch</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about">
        <div class="container">
            <div class="section-title">
                <h2>About Me</h2>
            </div>
            
            <div class="about-content">
                <div class="about-text">
                    <h3>Professional Networking & Surveillance Expert</h3>
                    <p>I am a dedicated Networking & Surveillance Engineer with over 8 years of experience in designing, implementing, and maintaining enterprise-level network infrastructures and surveillance systems.</p>
                    <p>My expertise spans across various domains including IP networking, CCTV installation and configuration, cloud infrastructure management, and smart building automation solutions.</p>
                    <p>I'm passionate about creating secure, efficient, and scalable technological solutions that meet the evolving needs of modern businesses and organizations.</p>
                    
                    <div class="about-stats">
                        <div class="stat-item">
                            <span class="stat-number">8+</span>
                            <span class="stat-label">Years Experience</span>
                        </div>
                        <div class="stat-item">
                            <span class="stat-number">200+</span>
                            <span class="stat-label">Projects Completed</span>
                        </div>
                        <div class="stat-item">
                            <span class="stat-number">50+</span>
                            <span class="stat-label">Happy Clients</span>
                        </div>
                        <div class="stat-item">
                            <span class="stat-number">24/7</span>
                            <span class="stat-label">Support Available</span>
                        </div>
                    </div>
                </div>
                
                <div class="about-text">
                    <h3>Core Competencies</h3>
                    <p><strong>Network Design & Implementation:</strong> Planning and deploying robust network infrastructures for enterprises of all sizes.</p>
                    <p><strong>Surveillance Systems:</strong> End-to-end CCTV solutions including installation, configuration, and monitoring.</p>
                    <p><strong>Security Solutions:</strong> Implementing comprehensive security measures to protect network integrity and data.</p>
                    <p><strong>Cloud Integration:</strong> Seamless integration of on-premise systems with cloud-based infrastructure.</p>
                    <p><strong>Technical Consultation:</strong> Providing expert advice on technology solutions tailored to specific business needs.</p>
                    
                    <a href="#contact" class="btn" style="margin-top: 20px;">Contact For Consultation</a>
                </div>
            </div>
        </div>
    </section>

    <!-- Skills Section -->
    <section id="skills">
        <div class="container">
            <div class="section-title">
                <h2>Professional Skills</h2>
            </div>

            <div class="skills-grid">
                <div class="skill-box">
                    <i class="fas fa-network-wired"></i>
                    <h3>Enterprise Networking</h3>
                    <p>Design, implementation, and troubleshooting of complex enterprise network infrastructures including routers, switches, and firewalls.</p>
                </div>

                <div class="skill-box">
                    <i class="fas fa-video"></i>
                    <h3>CCTV & Surveillance Systems</h3>
                    <p>Complete surveillance solutions including IP cameras, NVR/DVR systems, video analytics, and remote monitoring setups.</p>
                </div>

                <div class="skill-box">
                    <i class="fas fa-cloud"></i>
                    <h3>Cloud Management</h3>
                    <p>Cloud-based systems deployment, management, and integration with existing infrastructure for scalable solutions.</p>
                </div>

                <div class="skill-box">
                    <i class="fas fa-building"></i>
                    <h3>Smart Building Solutions</h3>
                    <p>Intelligent automation systems integration for modern buildings including access control and environmental monitoring.</p>
                </div>
                
                <div class="skill-box">
                    <i class="fas fa-shield-alt"></i>
                    <h3>Network Security</h3>
                    <p>Implementation of comprehensive security protocols, firewall configurations, and intrusion detection systems.</p>
                </div>
                
                <div class="skill-box">
                    <i class="fas fa-wifi"></i>
                    <h3>Wireless Networking</h3>
                    <p>Design and deployment of enterprise-grade wireless networks with seamless coverage and robust security.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Experience Section -->
    <section id="experience">
        <div class="container">
            <div class="section-title">
                <h2>Professional Experience</h2>
            </div>
            
            <div class="timeline">
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Senior Networking Engineer</h3>
                        <span class="date">2020 - Present</span>
                        <p>Leading network infrastructure projects for enterprise clients, designing scalable solutions, and implementing advanced surveillance systems.</p>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Network Solutions Specialist</h3>
                        <span class="date">2017 - 2020</span>
                        <p>Implemented and maintained network systems for various organizations, specializing in CCTV integration and cloud management solutions.</p>
                    </div>
                </div>
                
                <div class="timeline-item">
                    <div class="timeline-content">
                        <h3>Junior Network Engineer</h3>
                        <span class="date">2015 - 2017</span>
                        <p>Assisted in network setup and surveillance system installations, gaining hands-on experience with enterprise-level equipment and protocols.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Me</h2>
                <p style="margin-top: 20px; opacity: 0.9;">Ready to discuss your networking or surveillance project? Get in touch today.</p>
            </div>

            <div class="contact-info">
                <div class="contact-box">
                    <i class="fas fa-envelope"></i>
                    <h3>Email</h3>
                    <p>hasnaingull@gmail.com</p>
                </div>

                <div class="contact-box">
                    <i class="fas fa-phone"></i>
                    <h3>Phone</h3>
                    <p>0309 793****</p>
                </div>

                <div class="contact-box">
                    <i class="fas fa-map-marker-alt"></i>
                    <h3>Location</h3>
                    <p>DHA Multan, Pakistan</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="social-links">
                <a href="#"><i class="fab fa-linkedin-in"></i></a>
                <a href="#"><i class="fab fa-twitter"></i></a>
                <a href="#"><i class="fab fa-facebook-f"></i></a>
                <a href="#"><i class="fab fa-instagram"></i></a>
            </div>
            
            <p class="copyright">© <span id="year"></span> Muhammad Hasnain Gull | All Rights Reserved</p>
            <p style="margin-top: 10px; font-size: 14px; opacity: 0.7;">Networking & Surveillance Engineer</p>
        </div>
    </footer>

    <script>
        // Mobile menu toggle
        document.getElementById("menu").onclick = function() {
            document.getElementById("nav").classList.toggle("active");
        }
        
        // Set current year in footer
        document.getElementById("year").innerText = new Date().getFullYear();
        
        // Close mobile menu when clicking on a link
        const navLinks = document.querySelectorAll('.nav-links a');
        navLinks.forEach(link => {
            link.addEventListener('click', () => {
                document.getElementById("nav").classList.remove("active");
            });
        });
        
        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function(e) {
                e.preventDefault();
                
                const targetId = this.getAttribute('href');
                if(targetId === '#') return;
                
                const targetElement = document.querySelector(targetId);
                if(targetElement) {
                    window.scrollTo({
                        top: targetElement.offsetTop - 80,
                        behavior: 'smooth'
                    });
                }
            });
        });
        
        // Header scroll effect
        window.addEventListener('scroll', function() {
            const header = document.querySelector('header');
            if (window.scrollY > 50) {
                header.style.padding = '0';
                header.style.background = 'rgba(0, 59, 74, 0.98)';
            } else {
                header.style.padding = '';
                header.style.background = 'rgba(0, 59, 74, 0.98)';
            }
        });
    </script>
</body>
</html>
