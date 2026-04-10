<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ZABKA MB SOLUTIONS PVT LTD</title>
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">
    
    <style>
        /* --- CSS Variables --- */
        :root {
            --brand-primary: #1d4ed8; 
            --brand-primary-hover: #1e40af; 
            --brand-dark: #0f172a; 
            --text-main: #475569; 
            --text-light: #94a3b8; 
            --bg-body: #f8fafc; 
            --bg-white: #ffffff; 
            --border-color: #e2e8f0; 
            --shadow-sm: 0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1);
            --shadow-md: 0 4px 6px -1px rgb(0 0 0 / 0.05), 0 2px 4px -2px rgb(0 0 0 / 0.05);
            --shadow-lg: 0 10px 15px -3px rgb(0 0 0 / 0.05), 0 4px 6px -4px rgb(0 0 0 / 0.05);
        }

        /* Global CSS Reset */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Inter', sans-serif;
        }

        html { scroll-behavior: smooth; }

        body {
            line-height: 1.7;
            color: var(--text-main);
            background-color: var(--bg-body);
            -webkit-font-smoothing: antialiased;
            -moz-osx-font-smoothing: grayscale;
        }

        /* --- Navigation Bar --- */
        header {
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            border-bottom: 1px solid var(--border-color);
            position: fixed;
            width: 100%;
            top: 0;
            z-index: 1000;
            transition: all 0.3s ease;
        }

        nav {
            display: flex;
            justify-content: space-between;
            align-items: center;
            padding: 20px 50px;
            max-width: 1200px;
            margin: auto;
            position: relative;
        }

        nav .logo {
            font-size: 24px; 
            font-weight: 900; 
            letter-spacing: 1px; 
            text-transform: uppercase;
            text-rendering: optimizeLegibility;
            background: linear-gradient(90deg, #facc15, #ec4899, #3b82f6, #0ea5e9, #f97316, #8b5cf6, #facc15);
            background-size: 300% 100%;
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            animation: gradient-flow 6s linear infinite;
            filter: drop-shadow(0px 2px 4px rgba(0, 0, 0, 0.15));
        }

        @keyframes gradient-flow {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        nav ul {
            list-style: none;
            display: flex;
            flex-wrap: wrap; 
        }

        nav ul li { margin-left: 35px; }

        nav ul li a {
            text-decoration: none;
            color: var(--text-main);
            font-weight: 600; 
            font-size: 15px;
            transition: color 0.3s;
        }

        nav ul li a:hover { color: var(--brand-primary); }

        .menu-toggle {
            display: none;
            font-size: 24px;
            cursor: pointer;
            color: var(--brand-dark);
        }

        /* --- Image Slider / Hero Section --- */
        #home {
            position: relative;
            width: 100%;
            height: 100vh; /* Full viewport height */
            background-color: var(--brand-dark);
            overflow: hidden;
            display: flex;
            justify-content: center;
            align-items: center;
            padding-top: 80px; /* Offset for header */
        }

        .slide {
            position: absolute;
            top: 80px; /* Below header */
            left: 0;
            width: 100%;
            height: calc(100% - 80px);
            opacity: 0;
            transition: opacity 1s ease-in-out;
            display: flex;
            justify-content: center;
            align-items: center;
            background: linear-gradient(135deg, #0f172a 0%, #1e3a8a 100%);
        }

        .slide.active { opacity: 1; z-index: 2; }

        .slide img {
            width: 90%;
            height: 90%;
            max-width: 1200px;
            object-fit: contain; /* Prevents text cropping on posters */
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            border-radius: 10px;
        }

        /* Slider Controls (Optional visual dots) */
        .slider-dots {
            position: absolute;
            bottom: 30px;
            left: 50%;
            transform: translateX(-50%);
            display: flex;
            gap: 10px;
            z-index: 10;
        }

        .dot {
            width: 12px;
            height: 12px;
            background-color: rgba(255, 255, 255, 0.4);
            border-radius: 50%;
            cursor: pointer;
            transition: background-color 0.3s ease;
        }

        .dot.active { background-color: var(--bg-white); }


        /* --- General Section Styles --- */
        section { padding: 100px 20px; text-align: center; }
        .container { max-width: 1200px; margin: auto; }
        h1, h2, h3, h4 { color: var(--brand-dark); font-weight: 700; letter-spacing: -0.02em; }
        
        h2 { font-size: 36px; margin-bottom: 15px; position: relative; display: inline-block; }
        h2::after {
            content: ''; width: 60px; height: 4px; background: var(--brand-primary);
            position: absolute; bottom: -15px; left: 50%; transform: translateX(-50%); border-radius: 2px;
        }
        h2.white-text { color: var(--bg-white); }
        h2.white-text::after { background: var(--bg-white); }

        .section-subtitle {
            color: var(--text-light); max-width: 700px; margin: 30px auto 50px;
            font-weight: 400; font-size: 1.15rem;
        }

        /* --- Buttons --- */
        .btn {
            padding: 14px 32px; background: var(--bg-white); color: var(--brand-dark);
            text-decoration: none; border-radius: 6px; font-weight: 600; transition: all 0.3s ease;
            display: inline-block; border: 1px solid transparent; cursor: pointer;
            font-size: 16px; box-shadow: var(--shadow-sm);
        }
        .btn:hover { box-shadow: var(--shadow-md); transform: translateY(-2px); }
        .btn-primary { background: var(--brand-primary); color: var(--bg-white); }
        .btn-primary:hover { background: var(--brand-primary-hover); color: var(--bg-white); }

        /* --- About Us feature cards --- */
        .about-features-container {
            display: flex; flex-wrap: wrap; justify-content: space-between; gap: 25px;
            margin-top: 50px; max-width: 1000px; margin-left: auto; margin-right: auto; text-align: left;
        }
        .about-feature-card {
            flex: 1 1 calc(50% - 25px); min-width: 280px; display: flex; align-items: center;
            background: var(--bg-white); padding: 25px; border-radius: 8px;
            border: 1px solid var(--border-color); box-shadow: var(--shadow-sm); transition: transform 0.3s ease;
        }
        .about-feature-card:hover { transform: translateY(-3px); box-shadow: var(--shadow-md); }
        .about-feature-card i {
            font-size: 22px; color: var(--brand-primary); background-color: rgba(29, 78, 216, 0.08);
            border-radius: 8px; padding: 15px; margin-right: 20px; display: flex;
            align-items: center; justify-content: center; width: 55px; height: 55px;
        }
        .about-feature-card strong { color: var(--brand-dark); font-size: 16px; }

        /* --- Cards (Services & Features) --- */
        .service-category-title {
            font-size: 26px; color: var(--brand-dark); margin: 60px 0 30px; text-align: left;
            border-left: 4px solid var(--brand-primary); padding-left: 15px;
        }
        .grid-container {
            display: grid; grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
            gap: 30px; margin-bottom: 30px;
        }
        .card {
            background: var(--bg-white); padding: 40px 30px; border-radius: 8px;
            box-shadow: var(--shadow-sm); transition: all 0.3s ease;
            border: 1px solid var(--border-color); text-align: left;
        }
        .card:hover {
            transform: translateY(-8px); box-shadow: var(--shadow-lg);
            border-color: rgba(29, 78, 216, 0.3);
        }
        .card i { font-size: 32px; color: var(--brand-primary); margin-bottom: 25px; display: block; }
        .card.center-align { text-align: center; }
        .card.center-align i { display: inline-block; }
        .card h3 { font-size: 20px; margin-bottom: 15px; color: var(--brand-dark); }
        .card p { color: var(--text-main); font-size: 15px; line-height: 1.6; }

        /* --- Contact Us Section --- */
        .contact-wrapper { display: flex; flex-wrap: wrap; gap: 50px; margin-top: 50px; text-align: left; }
        .contact-form-box {
            flex: 1.2; min-width: 320px; background: var(--bg-white); padding: 45px;
            border-radius: 8px; box-shadow: var(--shadow-md); border: 1px solid var(--border-color);
        }
        .contact-form-box h3 { font-size: 24px; margin-bottom: 10px; }
        .contact-form-box p { color: var(--text-light); margin-bottom: 30px; font-size: 15px; }
        .form-group { margin-bottom: 22px; }
        .form-control {
            width: 100%; padding: 14px 18px; border: 1px solid var(--border-color);
            border-radius: 6px; font-size: 15px; transition: all 0.3s ease;
            background-color: var(--bg-body); color: var(--brand-dark);
        }
        .form-control:focus {
            outline: none; border-color: var(--brand-primary); background-color: var(--bg-white);
            box-shadow: 0 0 0 3px rgba(29, 78, 216, 0.1);
        }
        textarea.form-control { resize: vertical; }

        .contact-details-box { flex: 1; min-width: 320px; display: flex; flex-direction: column; gap: 25px; }
        .info-card {
            background: var(--bg-white); padding: 30px; border-radius: 8px; display: flex;
            align-items: flex-start; border: 1px solid var(--border-color); box-shadow: var(--shadow-sm);
            transition: transform 0.3s ease;
        }
        .info-card:hover { transform: translateX(5px); border-color: var(--brand-primary); }
        .info-card i {
            font-size: 22px; color: var(--brand-primary); background: rgba(29, 78, 216, 0.08);
            width: 50px; height: 50px; display: flex; align-items: center; justify-content: center;
            border-radius: 8px; margin-right: 20px; flex-shrink: 0;
        }
        .info-card h4 { font-size: 17px; margin-bottom: 8px; }
        .info-card p { color: var(--text-main); font-size: 15px; line-height: 1.6; }
        .info-card strong { color: var(--brand-dark); font-weight: 600; }

        /* --- CTA Section --- */
        .cta-section { background: var(--brand-primary); padding: 80px 20px; text-align: center; color: white; }
        .cta-section h2 { color: var(--bg-white); }
        .cta-section h2::after { display: none; }
        .cta-section p { color: rgba(255, 255, 255, 0.9); }
        .cta-section .btn { color: var(--brand-primary); }
        .cta-section .btn:hover { background: var(--brand-dark); color: var(--bg-white); }

        /* --- Footer Section --- */
        footer { background: var(--brand-dark); color: #cbd5e1; padding: 70px 20px 25px; }
        .footer-container {
            max-width: 1200px; margin: auto; display: flex; flex-wrap: wrap; justify-content: space-between;
            border-bottom: 1px solid rgba(255,255,255,0.1); padding-bottom: 50px; gap: 40px;
        }
        .footer-box { flex: 1; min-width: 280px; }
        .footer-box h3 { color: var(--bg-white); margin-bottom: 20px; font-size: 20px; }
        .contact-info p { margin: 18px 0; display: flex; align-items: center; color: #94a3b8; }
        .contact-info i {
            width: 38px; height: 38px; background: rgba(255,255,255,0.05); border-radius: 8px;
            display: flex; align-items: center; justify-content: center; margin-right: 15px; color: #60a5fa;
        }
        .copyright { text-align: center; padding-top: 25px; color: #64748b; font-size: 14px; }

        @media (max-width: 900px) { nav ul li { margin-left: 20px; } }

        /* --- MOBILE RESPONSIVE MEDIA QUERY --- */
        @media (max-width: 768px) {
            nav { padding: 18px 25px; flex-direction: row; }
            .menu-toggle { display: block; }
            nav ul {
                display: none; flex-direction: column; position: absolute; top: 100%; left: 0;
                width: 100%; background-color: var(--bg-white); box-shadow: var(--shadow-md);
                padding: 15px 0; gap: 0; border-top: 1px solid var(--border-color);
            }
            nav ul.active { display: flex; }
            nav ul li { margin: 0; text-align: left; width: 100%; }
            nav ul li a { display: block; padding: 15px 30px; font-size: 16px; border-bottom: 1px solid var(--bg-body); }
            section { padding: 70px 20px; }
            .contact-wrapper { flex-direction: column; gap: 30px; }
            #home { height: 60vh; } /* Make slider slightly smaller on mobile */
            .slide img { width: 100%; border-radius: 0; box-shadow: none; }
        }
    </style>
</head>
<body>

    <header id="main-header">
        <nav>
            <div class="logo">ZABKA MB SOLUTIONS</div>
            
            <div class="menu-toggle" id="mobile-menu">
                <i class="fa-solid fa-bars"></i>
            </div>

            <ul id="nav-list">
                <li><a href="#home">Home</a></li>
                <li><a href="#about">About Us</a></li>
                <li><a href="#services">Services</a></li>
                <li><a href="#why-choose">Why Choose Us</a></li>
                <li><a href="#contact">Contact Us</a></li>
            </ul>
        </nav>
    </header>

    <section id="home">
        <div class="slide active">
            <img src="Poster1.jpeg" alt="Payroll Management">
        </div>
        <div class="slide">
            <img src="Poster2jpeg.jpeg" alt="Training & Development">
        </div>
        <div class="slide">
            <img src="Poster3.jpeg" alt="Manpower Solutions">
        </div>
        <div class="slide">
            <img src="Poster4.jpeg" alt="Airtel CSP Services">
        </div>

        <div class="slider-dots">
            <span class="dot active" onclick="currentSlide(0)"></span>
            <span class="dot" onclick="currentSlide(1)"></span>
            <span class="dot" onclick="currentSlide(2)"></span>
            <span class="dot" onclick="currentSlide(3)"></span>
        </div>
    </section>

    <section id="about" style="background-color: var(--bg-white);">
        <div class="container">
            <h2>About Us</h2>
            <p class="section-subtitle">Leading Provider of Telecom & Manpower Solutions</p>
            
            <div style="max-width: 900px; margin: auto; font-size: 17px; line-height: 1.8; text-align: left;">
                <p style="margin-bottom: 20px;">
                    <strong>ZABKA MB SOLUTIONS PRIVATE LIMITED</strong> is your trusted partner for comprehensive Airtel CSP services and professional manpower solutions. As an authorized Airtel Customer Service Point, we provide complete telecom services including new connections, recharges, and billing solutions.
                </p>
                <p>
                    Our manpower division specializes in recruitment, contract staffing, and workforce management across various industries. With a commitment to excellence and customer satisfaction, we deliver reliable, efficient, and cost-effective solutions tailored to your business needs.
                </p>
            </div>

            <div class="about-features-container">
                <div class="about-feature-card">
                    <i class="fa-solid fa-certificate"></i>
                    <div><strong>Authorized Partner</strong><br><span style="color: var(--text-light); font-size: 14px;">Official Airtel CSP</span></div>
                </div>
                <div class="about-feature-card">
                    <i class="fa-solid fa-user-tie"></i>
                    <div><strong>Expert Team</strong><br><span style="color: var(--text-light); font-size: 14px;">Trained Professionals</span></div>
                </div>
                <div class="about-feature-card">
                    <i class="fa-solid fa-bolt"></i>
                    <div><strong>Quick Service</strong><br><span style="color: var(--text-light); font-size: 14px;">Fast Processing</span></div>
                </div>
                <div class="about-feature-card">
                    <i class="fa-solid fa-headset"></i>
                    <div><strong>24/7 Support</strong><br><span style="color: var(--text-light); font-size: 14px;">Always Available</span></div>
                </div>
            </div>
        </div>
    </section>

    <section id="services" style="background-color: var(--bg-body);">
        <div class="container">
            <h2>Our Services</h2>
            <p class="section-subtitle">Comprehensive Solutions for Your Business<br>From telecom services to manpower management, we have you covered.</p>

            <h3 class="service-category-title">Airtel CSP Services</h3>
            <div class="grid-container">
                <div class="card">
                    <i class="fa-solid fa-user-plus"></i>
                    <h3>New Connections</h3>
                    <p>Get new Airtel prepaid and postpaid connections with instant verification and quick activation.</p>
                </div>
                <div class="card">
                    <i class="fa-solid fa-indian-rupee-sign"></i>
                    <h3>Recharge & Bill Payment</h3>
                    <p>Secure, quick, and easy mobile recharge and bill payment services for all Airtel customers.</p>
                </div>
                <div class="card">
                    <i class="fa-solid fa-sim-card"></i>
                    <h3>SIM Services</h3>
                    <p>SIM activation, secure upgrades, replacements, and hassle-free MNP (Porting) services.</p>
                </div>
            </div>

            <h3 class="service-category-title">Manpower Solutions</h3>
            <div class="grid-container">
                <div class="card">
                    <i class="fa-solid fa-users-viewfinder"></i>
                    <h3>Recruitment Services</h3>
                    <p>End-to-end recruitment solutions designed to source both skilled and unskilled workforce needs.</p>
                </div>
                <div class="card">
                    <i class="fa-solid fa-file-contract"></i>
                    <h3>Contract Staffing</h3>
                    <p>Flexible, compliant contract-based workforce solutions tailored for short and long-term projects.</p>
                </div>
                <div class="card">
                    <i class="fa-solid fa-handshake"></i>
                    <h3>Permanent Placement</h3>
                    <p>Strategic recruitment helping you find and hire the right long-term talent for your organization.</p>
                </div>
                <div class="card">
                    <i class="fa-solid fa-industry"></i>
                    <h3>Industry Solutions</h3>
                    <p>Specialized manpower provisioning for IT, manufacturing, retail, and hospitality sectors.</p>
                </div>
                <div class="card">
                    <i class="fa-solid fa-file-invoice-dollar"></i>
                    <h3>Payroll Management</h3>
                    <p>Complete payroll processing, administrative management, and strict regulatory compliance services.</p>
                </div>
                <div class="card">
                    <i class="fa-solid fa-chalkboard-user"></i>
                    <h3>Training & Development</h3>
                    <p>Professional skill enhancement and corporate training programs to boost workforce productivity.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="why-choose" style="background-color: var(--bg-white);">
        <div class="container">
            <h2>Why Choose Us</h2>
            <p class="section-subtitle">Your Success is Our Priority<br>Experience the difference with our professional services and dedicated support.</p>
            
            <div class="grid-container">
                <div class="card center-align">
                    <i class="fa-solid fa-shield-halved"></i>
                    <h3>Authorized Partner</h3>
                    <p>Official Airtel CSP delivering certified services and 100% genuine products.</p>
                </div>
                <div class="card center-align">
                    <i class="fa-solid fa-users-gear"></i>
                    <h3>Expert Team</h3>
                    <p>Experienced industry professionals completely dedicated to customer satisfaction.</p>
                </div>
                <div class="card center-align">
                    <i class="fa-solid fa-stopwatch"></i>
                    <h3>Quick Service</h3>
                    <p>Optimized workflows ensuring fast processing and instant activation for all services.</p>
                </div>
                <div class="card center-align">
                    <i class="fa-solid fa-headset"></i>
                    <h3>Reliable Support</h3>
                    <p>Round-the-clock dedicated customer support for all your operational queries.</p>
                </div>
                <div class="card center-align">
                    <i class="fa-solid fa-chart-line"></i>
                    <h3>Competitive Pricing</h3>
                    <p>Best market rates and transparent pricing models with absolutely no hidden charges.</p>
                </div>
                <div class="card center-align">
                    <i class="fa-solid fa-network-wired"></i>
                    <h3>Wide Network</h3>
                    <p>Extensive operational reach across multiple locations for seamless service delivery.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="contact" style="background-color: var(--bg-body);">
        <div class="container">
            <h2>Contact Us</h2>
            <p class="section-subtitle">Have questions? We're here to help. Reach out to our team today.</p>
            
            <div class="contact-wrapper">
                <div class="contact-form-box">
                    <h3>Send us a Message</h3>
                    <p>Fill out the form below and our executive will get back to you shortly.</p>
                    
                    <form action="#" method="POST">
                        <div class="form-group">
                            <input type="text" class="form-control" placeholder="Full Name *" required>
                        </div>
                        <div class="form-group">
                            <input type="email" class="form-control" placeholder="Corporate Email *" required>
                        </div>
                        <div class="form-group">
                            <input type="tel" class="form-control" placeholder="Phone Number *" required>
                        </div>
                        <div class="form-group">
                            <select class="form-control">
                                <option value="" disabled selected>Select Service of Interest</option>
                                <option value="Airtel CSP">Airtel CSP Services</option>
                                <option value="Manpower">Manpower Solutions</option>
                                <option value="Both">Both Services</option>
                                <option value="Other">Other Corporate Inquiry</option>
                            </select>
                        </div>
                        <div class="form-group">
                            <textarea class="form-control" rows="5" placeholder="Your Message / Requirements *" required></textarea>
                        </div>
                        <button type="submit" class="btn btn-primary" style="width: 100%;">Submit Message</button>
                    </form>
                </div>

                <div class="contact-details-box">
                    <div class="info-card">
                        <i class="fa-solid fa-phone"></i>
                        <div>
                            <h4>Phone</h4>
                            <p><strong>Main Contact:</strong> +91 8587017507</p>
                            <p><strong>Alternate:</strong> +91 9667270256</p>
                        </div>
                    </div>
                    
                    <div class="info-card">
                        <i class="fa-solid fa-envelope"></i>
                        <div>
                            <h4>Email</h4>
                            <p>info@zabkambsolutions.in</p>
                        </div>
                    </div>

                    <div class="info-card">
                        <i class="fa-solid fa-location-dot"></i>
                        <div>
                            <h4>Location</h4>
                            <p>India</p>
                        </div>
                    </div>

                    <div class="info-card">
                        <i class="fa-solid fa-clock"></i>
                        <div>
                            <h4>Business Hours</h4>
                            <p><strong>Mon - Sat:</strong> 9:00 AM - 7:00 PM</p>
                            <p><strong>Sunday:</strong> 10:00 AM - 5:00 PM</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section class="cta-section" id="cta">
        <div class="container">
            <h2 class="white-text">Ready to Accelerate Your Business?</h2>
            <p style="font-size: 18px; margin-bottom: 35px; max-width: 600px; margin-left: auto; margin-right: auto;">Partner with us today to find the most efficient telecom and manpower solutions tailored to your operational needs.</p>
            <a href="#contact" class="btn">Get in Touch Now</a>
        </div>
    </section>

    <footer>
        <div class="footer-container">
            <div class="footer-box">
                <h3>ZABKA MB SOLUTIONS</h3>
                <p style="color: #94a3b8; line-height: 1.8; max-width: 300px;">Your trusted partner for comprehensive Airtel CSP services and professional manpower solutions.</p>
            </div>
            
            <div class="footer-box contact-info">
                <h3>Contact Details</h3>
                <p><i class="fa-solid fa-phone"></i> +91 8587017507</p>
                <p><i class="fa-solid fa-envelope"></i> info@zabkambsolutions.in</p>
                <p><i class="fa-solid fa-location-dot"></i> India</p>
            </div>
        </div>
        
        <div class="copyright">
            &copy; 2026 ZABKA MB SOLUTIONS PRIVATE LIMITED. All Rights Reserved.
        </div>
    </footer>

    <script>
        // --- Header Scroll Shadow ---
        window.addEventListener('scroll', function() {
            const header = document.getElementById('main-header');
            if (window.scrollY > 10) {
                header.style.padding = "10px 0";
                header.style.boxShadow = "0 4px 20px rgba(0,0,0,0.08)";
                header.style.background = "rgba(255, 255, 255, 0.98)";
            } else {
                header.style.padding = "0";
                header.style.boxShadow = "none";
                header.style.background = "rgba(255, 255, 255, 0.95)";
            }
        });

        // --- Hamburger Menu Logic ---
        const mobileMenu = document.getElementById('mobile-menu');
        const navList = document.getElementById('nav-list');
        const navLinks = document.querySelectorAll('#nav-list li a');
        const icon = mobileMenu.querySelector('i');

        mobileMenu.addEventListener('click', () => {
            navList.classList.toggle('active');
            if(navList.classList.contains('active')) {
                icon.classList.remove('fa-bars');
                icon.classList.add('fa-xmark');
            } else {
                icon.classList.remove('fa-xmark');
                icon.classList.add('fa-bars');
            }
        });

        navLinks.forEach(link => {
            link.addEventListener('click', () => {
                navList.classList.remove('active');
                icon.classList.remove('fa-xmark');
                icon.classList.add('fa-bars');
            });
        });

        // --- Image Slider Logic ---
        let currentSlideIndex = 0;
        const slides = document.querySelectorAll('.slide');
        const dots = document.querySelectorAll('.dot');
        const totalSlides = slides.length;

        function showSlide(index) {
            // Remove active class from all slides and dots
            slides.forEach(slide => slide.classList.remove('active'));
            dots.forEach(dot => dot.classList.remove('active'));

            // Set new active slide and dot
            currentSlideIndex = index;
            if (currentSlideIndex >= totalSlides) {
                currentSlideIndex = 0; // Loop back to first
            } else if (currentSlideIndex < 0) {
                currentSlideIndex = totalSlides - 1; // Loop to last
            }

            slides[currentSlideIndex].classList.add('active');
            dots[currentSlideIndex].classList.add('active');
        }

        function nextSlide() {
            showSlide(currentSlideIndex + 1);
        }

        // Allow clicking dots to change slide manually
        function currentSlide(index) {
            showSlide(index);
            resetTimer();
        }

        // Auto slide every 3.5 seconds
        let slideTimer = setInterval(nextSlide, 3500);

        function resetTimer() {
            clearInterval(slideTimer);
            slideTimer = setInterval(nextSlide, 3500);
        }
    </script>

</body>
</html>
