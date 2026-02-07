<!doctype html>
<html lang="en">
 <head>
  <meta charset="UTF-8">
  <title>Arsha Firnamarszepti | Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="description" content="Portfolio of Arsha Firnamarszepti – Visual Artist, Content Creator, and Animator">
  <style>
    * {
      box-sizing: border-box;
    }

    :root {
      --primary-color: #ff6b9d;
      --secondary-color: #c44569;
      --accent-color: #ffd700;
      --dark-bg: #0f1419;
      --light-text: #ffffff;
      --card-bg: #1a1f2e;
      --border-color: #2d3748;
    }

    body {
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      margin: 0;
      padding: 0;
      background: linear-gradient(135deg, #0f1419 0%, #1a1f2e 100%);
      color: #e0e0e0;
      line-height: 1.6;
      min-height: 100%;
    }

    /* Navigation */
    nav {
      position: fixed;
      top: 0;
      width: 100%;
      background: rgba(15, 20, 25, 0.95);
      backdrop-filter: blur(10px);
      padding: 1rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      z-index: 1000;
      border-bottom: 1px solid var(--border-color);
    }

    .nav-logo {
      font-weight: 700;
      font-size: 1.2rem;
      background: linear-gradient(135deg, #ff6b9d, #ffd700);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .nav-links {
      display: flex;
      gap: 2rem;
      list-style: none;
      margin: 0;
      padding: 0;
    }

    .nav-links a {
      color: #e0e0e0;
      text-decoration: none;
      font-size: 0.95rem;
      transition: color 0.3s ease;
      position: relative;
    }

    .nav-links a::after {
      content: '';
      position: absolute;
      bottom: -5px;
      left: 0;
      width: 0;
      height: 2px;
      background: linear-gradient(135deg, #ff6b9d, #ffd700);
      transition: width 0.3s ease;
    }

    .nav-links a:hover {
      color: #ff6b9d;
    }

    .nav-links a:hover::after {
      width: 100%;
    }

    @media (max-width: 768px) {
      .nav-links {
        display: none;
      }
    }

    /* Header */
    header {
      margin-top: 80px;
      padding: 80px 20px 60px;
      text-align: center;
      background: linear-gradient(135deg, rgba(255, 107, 157, 0.1) 0%, rgba(196, 69, 105, 0.1) 100%);
      border-bottom: 1px solid var(--border-color);
      position: relative;
      overflow: hidden;
    }

    header::before {
      content: '';
      position: absolute;
      top: -50%;
      right: -10%;
      width: 400px;
      height: 400px;
      background: radial-gradient(circle, rgba(255, 107, 157, 0.15) 0%, transparent 70%);
      border-radius: 50%;
      animation: float 6s ease-in-out infinite;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(-20px); }
    }

    header h1 {
      margin: 0;
      font-size: 3.5rem;
      background: linear-gradient(135deg, #ff6b9d, #ffd700, #ff6b9d);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      animation: fadeInDown 0.8s ease;
      position: relative;
      z-index: 1;
    }

    header p {
      margin-top: 15px;
      font-size: 1.3rem;
      color: #b0b0b0;
      animation: fadeInUp 0.8s ease 0.2s both;
    }

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

    /* Sections */
    section {
      max-width: 1000px;
      margin: 60px auto;
      padding: 0 20px;
      animation: fadeInUp 0.8s ease;
    }

    h2 {
      font-size: 2rem;
      margin-bottom: 30px;
      padding-bottom: 15px;
      border-bottom: 2px solid var(--primary-color);
      background: linear-gradient(90deg, #ff6b9d, #c44569);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      position: relative;
    }

    h2::after {
      content: '';
      position: absolute;
      bottom: -2px;
      left: 0;
      width: 100%;
      height: 2px;
      background: linear-gradient(90deg, #ff6b9d, #c44569, transparent);
    }

    /* Info Grid */
    .info-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      margin-bottom: 40px;
    }

    .info-box {
      background: var(--card-bg);
      padding: 25px;
      border-radius: 12px;
      border: 1px solid var(--border-color);
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
    }

    .info-box::before {
      content: '';
      position: absolute;
      top: 0;
      left: -100%;
      width: 100%;
      height: 100%;
      background: linear-gradient(90deg, transparent, rgba(255, 107, 157, 0.2), transparent);
      transition: left 0.5s ease;
    }

    .info-box:hover::before {
      left: 100%;
    }

    .info-box:hover {
      border-color: var(--primary-color);
      transform: translateY(-8px);
      box-shadow: 0 15px 40px rgba(255, 107, 157, 0.2);
    }

    .info-box strong {
      color: var(--primary-color);
      display: block;
      margin-bottom: 8px;
      font-size: 0.9rem;
      text-transform: uppercase;
      letter-spacing: 1px;
    }

    /* Lists */
    ul {
      padding-left: 0;
      list-style: none;
    }

    li {
      margin-bottom: 15px;
      padding-left: 30px;
      position: relative;
      color: #d0d0d0;
      transition: all 0.3s ease;
    }

    li::before {
      content: '▸';
      position: absolute;
      left: 0;
      color: var(--primary-color);
      font-size: 1.5rem;
      transition: all 0.3s ease;
    }

    li:hover {
      color: var(--primary-color);
      transform: translateX(5px);
    }

    li:hover::before {
      transform: scale(1.3);
    }

    /* Links */
    a {
      color: var(--primary-color);
      text-decoration: none;
      transition: all 0.3s ease;
      position: relative;
    }

    a::after {
      content: '';
      position: absolute;
      bottom: -2px;
      left: 0;
      width: 0;
      height: 2px;
      background: linear-gradient(90deg, var(--primary-color), var(--accent-color));
      transition: width 0.3s ease;
    }

    a:hover {
      color: var(--accent-color);
    }

    a:hover::after {
      width: 100%;
    }

    .external-link {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      padding: 10px 20px;
      background: linear-gradient(135deg, rgba(255, 107, 157, 0.1), rgba(196, 69, 105, 0.1));
      border: 1px solid var(--primary-color);
      border-radius: 6px;
      transition: all 0.3s ease;
    }

    .external-link:hover {
      background: linear-gradient(135deg, rgba(255, 107, 157, 0.2), rgba(196, 69, 105, 0.2));
      transform: translateX(5px);
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 40px 20px;
      background: rgba(15, 20, 25, 0.8);
      color: #888;
      font-size: 0.9rem;
      border-top: 1px solid var(--border-color);
      margin-top: 80px;
    }

    .footer-content {
      max-width: 1000px;
      margin: 0 auto;
    }

    .social-links {
      display: flex;
      justify-content: center;
      gap: 20px;
      margin-bottom: 20px;
    }

    .social-links a {
      width: 40px;
      height: 40px;
      display: flex;
      align-items: center;
      justify-content: center;
      border: 1px solid var(--primary-color);
      border-radius: 50%;
      transition: all 0.3s ease;
      color: var(--primary-color);
    }

    .social-links a:hover {
      background: var(--primary-color);
      color: var(--dark-bg);
      transform: translateY(-5px);
    }

    /* Scroll animations */
    .fade-in {
      opacity: 0;
      transform: translateY(30px);
      transition: all 0.6s ease;
    }

    .fade-in.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* Responsive */
    @media (max-width: 768px) {
      header h1 {
        font-size: 2.5rem;
      }

      h2 {
        font-size: 1.5rem;
      }

      .nav-links {
        gap: 1rem;
        font-size: 0.85rem;
      }

      section {
        margin: 40px auto;
      }
    }

    /* Loading animation */
    @keyframes pulse {
      0%, 100% {
        opacity: 1;
      }
      50% {
        opacity: 0.5;
      }
    }

    .pulse {
      animation: pulse 2s ease-in-out infinite;
    }
  </style>
  <style>@view-transition { navigation: auto; }</style>
  <script src="/_sdk/data_sdk.js" type="text/javascript"></script>
  <script src="/_sdk/element_sdk.js" type="text/javascript"></script>
  <script src="https://cdn.tailwindcss.com" type="text/javascript"></script>
 </head>
 <body>
  <nav>
   <div class="nav-logo">
    ✨ Arsha
   </div>
   <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#education">Education</a></li>
    <li><a href="#skills">Skills</a></li>
    <li><a href="#experience">Experience</a></li>
    <li><a href="#portfolio">Portfolio</a></li>
   </ul>
  </nav>
  <header>
   <h1>Arsha Firnamarszepti</h1>
   <p>✨ Visual Artist • Content Animator • Writer ✨</p>
  </header>
  <section id="about">
   <h2>Personal Information</h2>
   <div class="info-grid">
    <div class="info-box fade-in"><strong>📅 Date of Birth</strong> 12 July 2003
    </div>
    <div class="info-box fade-in"><strong>📱 Phone</strong> 05587213444
    </div>
    <div class="info-box fade-in"><strong>📍 Location</strong> Jawa Timur, Yogyakarta
    </div>
    <div class="info-box fade-in"><strong>📸 Instagram</strong> <a href="https://www.instagram.com/rshfirna?igsh=MW5oMW8yNmYycmxpcQ==" target="_blank" rel="noopener noreferrer"> @rshfirna </a>
    </div>
   </div>
  </section>
  <section id="education">
   <h2>Education</h2>
   <ul>
    <li>SD Muhammadiyah 7</li>
    <li>Al-Ihsan Islamic Boarding School (MTS)</li>
    <li>SMA KP Baleendah</li>
    <li>Institut Seni Indonesia Yogyakarta (ISI Yogyakarta)</li>
   </ul>
  </section>
  <section id="skills">
   <h2>Skills</h2>
   <ul>
    <li>Visual Graphic Design (Digital Drawing, Traditional Drawing, Poster, Infographics, Banner, Advertising)</li>
    <li>Content Animation</li>
    <li>Content Creation</li>
    <li>Writing</li>
   </ul>
  </section>
  <section id="experience">
   <h2>Experience &amp; Achievements</h2>
   <ul>
    <li>🏆 1st Winner – FLS2N (District Level)</li>
    <li>🏆 1st Winner – Calligraphy Competition (MTS Internal)</li>
    <li>🥈 2nd Winner – Calligraphy Competition (MTS Internal)</li>
    <li>🥉 3rd Winner – Calligraphy Competition (MTS Internal)</li>
    <li>👔 Former Head of Public Relations – OSIS</li>
    <li>🎨 Chief of Character Design – SEIIBU (Japanese Club)</li>
    <li>✨ Additional freelance and creative project experiences</li>
   </ul>
  </section>
  <section>
   <h2>Languages</h2>
   <ul>
    <li>🇮🇩 Indonesian (Native)</li>
    <li>🇬🇧 English (Second Language)</li>
    <li>🇯🇵 Japanese (Basic)</li>
    <li>🇸🇦 Arabic (Basic)</li>
   </ul>
  </section>
  <section id="portfolio">
   <h2>Portfolio</h2>
   <p style="font-size: 1.1rem; color: #d0d0d0;">Check out my full portfolio and amazing artworks:</p><a href="https://marszeportofolio.my.canva.site/speciality-in-narative-art" target="_blank" rel="noopener noreferrer" class="external-link"> 🎨 Visit Portfolio → marszeportofolio.my.canva.site </a>
  </section>
  <footer>
   <div class="footer-content">
    <div class="social-links"><a href="https://www.instagram.com/rshfirna?igsh=MW5oMW8yNmYycmxpcQ==" target="_blank" rel="noopener noreferrer" title="Instagram">📸</a> <a href="mailto:arsha@example.com" title="Email">✉️</a>
    </div>
    <p>© 2026 Arsha Firnamarszepti — All Rights Reserved</p>
    <p style="font-size: 0.8rem; margin-top: 10px;">Crafted with passion ✨</p>
   </div>
  </footer>
  <script>
  // Smooth scroll for navigation
  document.querySelectorAll('a[href^="#"]').forEach(anchor => {
    anchor.addEventListener('click', function (e) {
      e.preventDefault();
      const target = document.querySelector(this.getAttribute('href'));
      if (target) {
        target.scrollIntoView({ behavior: 'smooth', block: 'start' });
      }
    });
  });

  // Intersection Observer untuk animasi fade-in
  const observerOptions = {
    threshold: 0.1,
    rootMargin: '0px 0px -50px 0px'
  };

  const observer = new IntersectionObserver(function(entries) {
    entries.forEach(entry => {
      if (entry.isIntersecting) {
        entry.target.classList.add('visible');
        observer.unobserve(entry.target);
      }
    });
  }, observerOptions);

  document.querySelectorAll('.fade-in').forEach(el => {
    observer.observe(el);
  });

  // Active navigation link on scroll
  window.addEventListener('scroll', () => {
    let current = '';
    const sections = document.querySelectorAll('section');
    
    sections.forEach(section => {
      const sectionTop = section.offsetTop - 100;
      if (pageYOffset >= sectionTop) {
        current = section.getAttribute('id');
      }
    });

    document.querySelectorAll('.nav-links a').forEach(link => {
      link.classList.remove('active');
      if (link.getAttribute('href').slice(1) === current) {
        link.style.color = 'var(--primary-color)';
      } else {
        link.style.color = '#e0e0e0';
      }
    });
  });

  // Parallax effect on header
  window.addEventListener('scroll', () => {
    const header = document.querySelector('header');
    header.style.transform = translateY(${window.scrollY * 0.3}px);
  });
</script>
 <script>(function(){function c(){var b=a.contentDocument||a.contentWindow.document;if(b){var d=b.createElement('script');d.innerHTML="window.__CF$cv$params={r:'9c9f7cbd44c8fd9b',t:'MTc3MDQzMTY1Ni4wMDAwMDA='};var a=document.createElement('script');a.nonce='';a.src='/cdn-cgi/challenge-platform/scripts/jsd/main.js';document.getElementsByTagName('head')[0].appendChild(a);";b.getElementsByTagName('head')[0].appendChild(d)}}if(document.body){var a=document.createElement('iframe');a.height=1;a.width=1;a.style.position='absolute';a.style.top=0;a.style.left=0;a.style.border='none';a.style.visibility='hidden';document.body.appendChild(a);if('loading'!==document.readyState)c();else if(window.addEventListener)document.addEventListener('DOMContentLoaded',c);else{var e=document.onreadystatechange||function(){};document.onreadystatechange=function(b){e(b);'loading'!==document.readyState&&(document.onreadystatechange=e,c())}}}})();</script></body>
</html>
