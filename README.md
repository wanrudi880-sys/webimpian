<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Karya Kreatif Digital - Jasa Pembuatan Website Profesional</title>
    
    <!-- Google Fonts (Poppins & Roboto) -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@600;700&family=Roboto:wght@400;500&display=swap" rel="stylesheet">

    <style>
        /* --- Reset & Global Styles --- */
        :root {
            --primary-color: #007BFF;
            --secondary-color: #343a40;
            --light-color: #f8f9fa;
            --text-color: #333;
            --font-heading: 'Poppins', sans-serif;
            --font-body: 'Roboto', sans-serif;
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
            font-family: var(--font-body);
            line-height: 1.6;
            color: var(--text-color);
            background-color: #fff;
        }

        .container {
            max-width: 1100px;
            margin: 0 auto;
            padding: 0 20px;
        }

        h1, h2, h3 {
            font-family: var(--font-heading);
            font-weight: 700;
            margin-bottom: 1rem;
        }

        h2 {
            font-size: 2.5rem;
            text-align: center;
            margin-bottom: 3rem;
        }

        section {
            padding: 80px 0;
        }

        section:nth-child(even) {
            background-color: var(--light-color);
        }

        /* --- Header & Navigasi --- */
        .navbar {
            background: #fff;
            padding: 1rem 0;
            position: fixed;
            width: 100%;
            top: 0;
            left: 0;
            z-index: 1000;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
            transition: background 0.3s ease;
        }

        .navbar .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .navbar .logo {
            font-family: var(--font-heading);
            font-size: 1.5rem;
            font-weight: 700;
            color: var(--primary-color);
            text-decoration: none;
        }

        .navbar .nav-menu {
            display: flex;
            list-style: none;
        }

        .navbar .nav-menu li {
            margin-left: 25px;
        }

        .navbar .nav-menu a {
            text-decoration: none;
            color: var(--secondary-color);
            font-weight: 500;
            transition: color 0.3s ease;
        }

        .navbar .nav-menu a:hover {
            color: var(--primary-color);
        }

        /* --- Hero Section --- */
        .hero {
            background: linear-gradient(rgba(0, 123, 255, 0.7), rgba(0, 123, 255, 0.7)), url('https://source.unsplash.com/random/1600x900?technology,website') no-repeat center center/cover;
            height: 100vh;
            color: #fff;
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: center;
            padding: 0 20px;
        }

        .hero-content h1 {
            font-size: 3.5rem;
            margin-bottom: 1rem;
        }

        .hero-content p {
            font-size: 1.2rem;
            max-width: 600px;
            margin: 0 auto 2rem auto;
        }

        .btn {
            display: inline-block;
            padding: 12px 30px;
            background: var(--primary-color);
            color: #fff;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 600;
            transition: background 0.3s ease, transform 0.2s ease;
        }

        .btn:hover {
            background: #0056b3;
            transform: translateY(-2px);
        }

        .btn-secondary {
            background: transparent;
            border: 2px solid #fff;
            margin-left: 10px;
        }

        .btn-secondary:hover {
            background: #fff;
            color: var(--primary-color);
        }

        /* --- Services Section --- */
        .services-grid {
            display: grid;
            grid-template-columns: repeat(3, 1fr);
            gap: 30px;
            text-align: center;
        }

        .service-item {
            background: #fff;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }

        .service-item:hover {
            transform: translateY(-10px);
            box-shadow: 0 10px 25px rgba(0,0,0,0.1);
        }

        .service-item .icon {
            font-size: 3rem;
            color: var(--primary-color);
            margin-bottom: 1rem;
        }

        /* --- Testimonials Section --- */
        .testimonials-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 30px;
        }

        .testimonial-item {
            background: #fff;
            padding: 30px;
            border-left: 5px solid var(--primary-color);
            border-radius: 5px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.08);
        }

        .testimonial-item p {
            font-style: italic;
            margin-bottom: 1rem;
        }

        .testimonial-item h4 {
            font-weight: 600;
            color: var(--secondary-color);
        }

        /* --- Contact Section --- */
        .contact .container {
            text-align: center;
        }

        .contact p {
            max-width: 700px;
            margin: 0 auto 2rem auto;
            font-size: 1.1rem;
        }

        /* --- Footer --- */
        .footer {
            background: var(--secondary-color);
            color: #fff;
            text-align: center;
            padding: 2rem 0;
        }

        .social-links a {
            color: #fff;
            font-size: 1.5rem;
            margin: 0 10px;
            text-decoration: none;
            transition: color 0.3s ease;
        }

        .social-links a:hover {
            color: var(--primary-color);
        }

        /* --- Responsive Design --- */
        @media (max-width: 768px) {
            h2 { font-size: 2rem; }
            .hero-content h1 { font-size: 2.5rem; }
            .services-grid, .testimonials-grid {
                grid-template-columns: 1fr;
            }
            .navbar .nav-menu {
                position: fixed;
                left: -100%;
                top: 70px;
                flex-direction: column;
                background-color: #fff;
                width: 100%;
                text-align: center;
                transition: 0.3s;
                box-shadow: 0 10px 27px rgba(0,0,0,0.05);
                padding: 20px 0;
            }
            .navbar .nav-menu.active {
                left: 0;
            }
            .navbar .nav-menu li {
                margin: 15px 0;
            }
            .hamburger {
                display: block;
                cursor: pointer;
            }
            .hamburger .bar {
                display: block;
                width: 25px;
                height: 3px;
                margin: 5px auto;
                transition: all 0.3s ease-in-out;
                background-color: var(--secondary-color);
            }
            .hamburger.active .bar:nth-child(2) {
                opacity: 0;
            }
            .hamburger.active .bar:nth-child(1) {
                transform: translateY(8px) rotate(45deg);
            }
            .hamburger.active .bar:nth-child(3) {
                transform: translateY(-8px) rotate(-45deg);
            }
        }
        
        @media (min-width: 769px) {
            .hamburger { display: none; }
        }

    </style>
</head>
<body>

    <!-- ==================== HEADER & NAVIGASI ==================== -->
    <header class="navbar">
        <div class="container">
            <a href="#" class="logo">KaryaKreatif</a>
            <ul class="nav-menu">
                <li><a href="#hero">Beranda</a></li>
                <li><a href="#services">Layanan</a></li>
                <li><a href="#testimonials">Testimoni</a></li>
                <li><a href="#contact">Kontak</a></li>
            </ul>
            <div class="hamburger">
                <span class="bar"></span>
                <span class="bar"></span>
                <span class="bar"></span>
            </div>
        </div>
    </header>

    <main>
        <!-- ==================== HERO SECTION ==================== -->
        <section id="hero" class="hero">
            <div class="hero-content">
                <h1>Wujudkan Website Impian Anda</h1>
                <p>Kami hadir untuk memberikan solusi digital terbaik dengan desain website yang modern, cepat, dan responsif untuk meningkatkan kehadiran online bisnis Anda.</p>
                <a href="#contact" class="btn">Konsultasi Gratis</a>
                <a href="#services" class="btn btn-secondary">Lihat Layanan</a>
            </div>
        </section>

        <!-- ==================== SERVICES SECTION ==================== -->
        <section id="services" class="services">
            <div class="container">
                <h2>Layanan Kami</h2>
                <div class="services-grid">
                    <div class="service-item">
                        <div class="icon">🚀</div>
                        <h3>Pembuatan Website</h3>
                        <p>Website perusahaan, toko online (e-commerce), atau profil pribadi yang profesional dan user-friendly.</p>
                    </div>
                    <div class="service-item">
                        <div class="icon">🎨</div>
                        <h3>Desain UI/UX</h3>
                        <p>Desain antarmuka yang menarik dan pengalaman pengguna yang intuitif untuk meningkatkan kepuasan pengunjung.</p>
                    </div>
                    <div class="service-item">
                        <div class="icon">📈</div>
                        <h3>Optimasi SEO</h3>
                        <p>Strategi SEO terbaik agar website Anda mudah ditemukan di halaman pertama mesin pencari seperti Google.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- ==================== TESTIMONIALS SECTION ==================== -->
        <section id="testimonials" class="testimonials">
            <div class="container">
                <h2>Apa Kata Klien Kami</h2>
                <div class="testimonials-grid">
                    <div class="testimonial-item">
                        <p>"Pelayanan yang sangat memuaskan! Website yang dibuat sesuai dengan keinginan kami dan prosesnya cepat. Terima kasih KaryaKreatif!"</p>
                        <h4>- Andi Pratama, CEO TokoKu</h4>
                    </div>
                    <div class="testimonial-item">
                        <p>"Desain yang modern dan SEO-friendly. Sejak menggunakan jasa mereka, trafik website kami naik drastis. Highly recommended!"</p>
                        <h4>- Siti Nurhaliza, Founder Klinik Sehat</h4>
                    </div>
                </div>
            </div>
        </section>

        <!-- ==================== CONTACT SECTION ==================== -->
        <section id="contact" class="contact">
            <div class="container">
                <h2>Siap Memulai Proyek Anda?</h2>
                <p>Hubungi kami sekarang untuk konsultasi gratis dan dapatkan penawaran terbaik untuk kebutuhan digital Anda.</p>
                <a href="mailto:info@karyakreatif.com" class="btn">Hubungi Kami via Email</a>
            </div>
        </section>
    </main>

    <!-- ==================== FOOTER ==================== -->
    <footer class="footer">
        <div class="container">
            <div class="social-links">
                <!-- Ganti # dengan link media sosial Anda -->
                <a href="#" target="_blank">f</a> <!-- Facebook -->
                <a href="#" target="_blank">t</a> <!-- Twitter -->
                <a href="#" target="_blank">i</a> <!-- Instagram -->
                <a href="#" target="_blank">in</a> <!-- LinkedIn -->
            </div>
            <p>&copy; 2024 Karya Kreatif Digital. All Rights Reserved.</p>
        </div>
    </footer>

    <script>
        // --- Hamburger Menu Toggle ---
        const hamburger = document.querySelector(".hamburger");
        const navMenu = document.querySelector(".nav-menu");

        hamburger.addEventListener("click", () => {
            hamburger.classList.toggle("active");
            navMenu.classList.toggle("active");
        });

        document.querySelectorAll(".nav-menu a").forEach(n => n.addEventListener("click", () => {
            hamburger.classList.remove("active");
            navMenu.classList.remove("active");
        }));

    </script>

</body>
</html>
