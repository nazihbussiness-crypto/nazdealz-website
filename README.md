# nazdealz-website
Professional vehicle transport services website
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>NAZDEALZ - Professional Vehicle Transport Services</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        :root {
            --primary: #1a365d;
            --secondary: #2d3748;
            --accent: #e53e3e;
            --light: #f7fafc;
            --dark: #2d3748;
            --success: #38a169;
        }
        
        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }
        
        .container {
            width: 90%;
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 15px;
        }
        
        /* Header & Navigation */
        header {
            background-color: rgba(26, 54, 93, 0.9);
            color: white;
            padding: 1rem 0;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
        }
        
        .header-container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }
        
        .logo {
            font-size: 1.8rem;
            font-weight: 700;
            color: white;
            text-decoration: none;
        }
        
        .logo span {
            color: var(--accent);
        }
        
        nav ul {
            display: flex;
            list-style: none;
        }
        
        nav ul li {
            margin-left: 1.5rem;
        }
        
        nav ul li a {
            color: white;
            text-decoration: none;
            font-weight: 500;
            transition: color 0.3s;
            padding: 0.5rem 0;
        }
        
        nav ul li a:hover {
            color: var(--accent);
        }
        
        /* Hero Section */
        .hero {
            background: linear-gradient(rgba(26, 54, 93, 0.7), rgba(26, 54, 93, 0.8)), url('https://images.unsplash.com/photo-1535732820275-9ffd998cac22?ixlib=rb-1.2.1&auto=format&fit=crop&w=1350&q=80');
            background-size: cover;
            background-position: center;
            color: white;
            padding: 8rem 0 4rem;
            text-align: center;
        }
        
        .hero h1 {
            font-size: 3rem;
            margin-bottom: 1rem;
        }
        
        .hero p {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 2rem;
        }
        
        .btn {
            display: inline-block;
            background-color: var(--accent);
            color: white;
            padding: 0.8rem 1.5rem;
            border-radius: 4px;
            text-decoration: none;
            font-weight: 600;
            transition: background-color 0.3s;
            border: none;
            cursor: pointer;
        }
        
        .btn:hover {
            background-color: #c53030;
        }
        
        /* Sections */
        section {
            padding: 4rem 0;
        }
        
        .section-title {
            text-align: center;
            margin-bottom: 3rem;
        }
        
        .section-title h2 {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1rem;
        }
        
        .section-title p {
            color: var(--secondary);
            max-width: 700px;
            margin: 0 auto;
        }
        
        /* About Section */
        .about-content {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
            align-items: center;
        }
        
        .about-text h3 {
            font-size: 1.8rem;
            margin-bottom: 1.5rem;
            color: var(--primary);
        }
        
        .about-text p {
            margin-bottom: 1.5rem;
        }
        
        /* Services Section */
        .services {
            background-color: var(--light);
        }
        
        .services-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 2rem;
        }
        
        .service-card {
            background-color: white;
            border-radius: 8px;
            padding: 2rem;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
            transition: transform 0.3s;
            text-align: center;
        }
        
        .service-card:hover {
            transform: translateY(-5px);
        }
        
        .service-icon {
            font-size: 2.5rem;
            color: var(--primary);
            margin-bottom: 1.5rem;
        }
        
        .service-card h3 {
            font-size: 1.5rem;
            margin-bottom: 1rem;
            color: var(--primary);
        }
        
        /* Contact Section */
        .contact-container {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 3rem;
        }
        
        .contact-info {
            display: flex;
            flex-direction: column;
            gap: 1.5rem;
        }
        
        .contact-method {
            display: flex;
            align-items: center;
            gap: 1rem;
        }
        
        .contact-icon {
            font-size: 1.5rem;
            color: var(--primary);
        }
        
        .contact-form {
            background-color: white;
            padding: 2rem;
            border-radius: 8px;
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
        }
        
        .form-group {
            margin-bottom: 1.5rem;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 0.5rem;
            font-weight: 500;
        }
        
        .form-group input, .form-group textarea {
            width: 100%;
            padding: 0.8rem;
            border: 1px solid #cbd5e0;
            border-radius: 4px;
            font-size: 1rem;
        }
        
        /* Footer */
        footer {
            background-color: var(--primary);
            color: white;
            padding: 3rem 0 1.5rem;
        }
        
        .footer-content {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 2rem;
            margin-bottom: 2rem;
        }
        
        .copyright {
            text-align: center;
            padding-top: 1.5rem;
            border-top: 1px solid #4a5568;
            font-size: 0.9rem;
            color: #cbd5e0;
        }
        
        @media (max-width: 768px) {
            .about-content, .contact-container {
                grid-template-columns: 1fr;
            }
            
            .hero {
                padding: 6rem 0 3rem;
            }
            
            .hero h1 {
                font-size: 2.2rem;
            }
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header>
        <div class="container header-container">
            <a href="#" class="logo">NAZ<span>DEALZ</span></a>
            <nav>
                <ul>
                    <li><a href="#home">Home</a></li>
                    <li><a href="#about">About</a></li>
                    <li><a href="#services">Services</a></li>
                    <li><a href="#contact">Contact</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section id="home" class="hero">
        <div class="container">
            <h1>Professional Vehicle Transport Services</h1>
            <p>With over 20 years of experience, we provide secure, reliable vehicle shipping with real-time tracking and VIN updates.</p>
            <a href="#contact" class="btn">Get a Quote</a>
        </div>
    </section>

    <!-- About Section -->
    <section id="about" class="about">
        <div class="container">
            <div class="section-title">
                <h2>About NAZDEALZ</h2>
                <p>20+ years of excellence in vehicle transport</p>
            </div>
            <div class="about-content">
                <div class="about-text">
                    <h3>Your Trusted Vehicle Transport Partner</h3>
                    <p>Founded with a passion for automobiles and commitment to customer satisfaction, NAZDEALZ has been a trusted name in vehicle transport for over two decades.</p>
                    <p>We specialize in secure vehicle shipping with real-time tracking and VIN updates to keep you informed every step of the way.</p>
                </div>
                <div class="about-text">
                    <h3>Why Choose Us?</h3>
                    <p>• 20+ years of experience</p>
                    <p>• Real-time vehicle tracking</p>
                    <p>• Secure shipping with insurance</p>
                    <p>• Professional customer service</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Services Section -->
    <section id="services" class="services">
        <div class="container">
            <div class="section-title">
                <h2>Our Services</h2>
                <p>Comprehensive vehicle transport solutions</p>
            </div>
            <div class="services-grid">
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-truck-loading"></i></div>
                    <h3>Vehicle Transport</h3>
                    <p>Safe and secure transportation using state-of-the-art carriers.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-map-marker-alt"></i></div>
                    <h3>Real-Time Tracking</h3>
                    <p>Track your vehicle's location with our advanced GPS system.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-barcode"></i></div>
                    <h3>VIN Updates</h3>
                    <p>Regular VIN-based status updates about your vehicle's condition.</p>
                </div>
                <div class="service-card">
                    <div class="service-icon"><i class="fas fa-shield-alt"></i></div>
                    <h3>Secure Shipping</h3>
                    <p>Comprehensive insurance coverage for complete peace of mind.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact" class="contact">
        <div class="container">
            <div class="section-title">
                <h2>Contact Us</h2>
                <p>Get in touch for quotes and support</p>
            </div>
            <div class="contact-container">
                <div class="contact-info">
                    <div class="contact-method">
                        <div class="contact-icon"><i class="fas fa-envelope"></i></div>
                        <div>
                            <h3>Email</h3>
                            <p>nazihbussiness@gmail.com</p>
                        </div>
                    </div>
                    <div class="contact-method">
                        <div class="contact-icon"><i class="fas fa-phone"></i></div>
                        <div>
                            <h3>Phone</h3>
                            <p>76917922</p>
                        </div>
                    </div>
                    <div class="contact-method">
                        <div class="contact-icon"><i class="fab fa-whatsapp"></i></div>
                        <div>
                            <h3>WhatsApp</h3>
                            <p>76917922</p>
                        </div>
                    </div>
                </div>
                <div class="contact-form">
                    <form id="contact-form">
                        <div class="form-group">
                            <label for="name">Full Name</label>
                            <input type="text" id="name" required>
                        </div>
                        <div class="form-group">
                            <label for="email">Email Address</label>
                            <input type="email" id="email" required>
                        </div>
                        <div class="form-group">
                            <label for="message">Message</label>
                            <textarea id="message" rows="5" required></textarea>
                        </div>
                        <button type="submit" class="btn" style="width: 100%;">Send Message</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <div class="container">
            <div class="footer-content">
                <div>
                    <h3>NAZDEALZ</h3>
                    <p>Professional vehicle transport services with over 20 years of experience.</p>
                </div>
                <div>
                    <h3>Contact</h3>
                    <p>Email: nazihbussiness@gmail.com</p>
                    <p>Phone: 76917922</p>
                </div>
            </div>
            <div class="copyright">
                <p>nazdealz.com © 2025 NAZDEALZ. All Rights Reserved.</p>
            </div>
        </div>
    </footer>

    <script>
        // Simple form submission
        document.getElementById('contact-form').addEventListener('submit', function(e) {
            e.preventDefault();
            const name = document.getElementById('name').value;
            alert('Thank you ' + name + '! We will contact you soon.');
            this.reset();
        });

        // Smooth scrolling
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
