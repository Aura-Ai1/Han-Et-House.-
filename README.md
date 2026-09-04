
<html lang="tr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HAN ET House | Tokat Steakhouse & Restoran</title>
  
  <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@500;700&family=Plus+Jakarta+Sans:wght@300;400;600&display=swap" rel="stylesheet">
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <link rel="stylesheet" href="https://unpkg.com/aos@2.3.1/dist/aos.css" />

  <style>
    :root {
      --gold: #d4af37;
      --gold-hover: #f3e5ab;
      --bg-dark: #0a0a0a;
      --card-bg: rgba(20, 20, 20, 0.75);
      --text-main: #f5f5f5;
      --text-muted: #a0a0a0;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    body {
      font-family: 'Plus Jakarta Sans', sans-serif;
      background-color: var(--bg-dark);
      color: var(--text-main);
      overflow-x: hidden;
    }

    /* Header & Navigation */
    header {
      position: fixed;
      top: 0;
      width: 100%;
      z-index: 1000;
      background: rgba(10, 10, 10, 0.85);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid rgba(212, 175, 55, 0.2);
      padding: 1.2rem 8%;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo {
      font-family: 'Cinzel', serif;
      font-size: 1.8rem;
      font-weight: 700;
      color: var(--gold);
      letter-spacing: 2px;
      text-decoration: none;
    }

    .nav-links {
      display: flex;
      gap: 2rem;
      list-style: none;
    }

    .nav-links a {
      color: var(--text-main);
      text-decoration: none;
      font-size: 0.95rem;
      transition: 0.3s;
    }

    .nav-links a:hover {
      color: var(--gold);
    }

    /* Hero Section */
    .hero {
      height: 100vh;
      background: linear-gradient(rgba(0,0,0,0.65), rgba(10,10,10,1)), 
                  url('https://images.unsplash.com/photo-1544025162-d76694265947?auto=format&fit=crop&w=1920&q=80') center/cover no-repeat;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 0 1rem;
    }

    .hero h1 {
      font-family: 'Cinzel', serif;
      font-size: 4rem;
      color: var(--gold);
      margin-bottom: 1rem;
      text-shadow: 0 4px 20px rgba(0,0,0,0.8);
    }

    .hero p {
      font-size: 1.2rem;
      max-width: 600px;
      margin-bottom: 2rem;
      color: var(--text-muted);
    }

    .badge {
      background: rgba(212, 175, 55, 0.15);
      border: 1px solid var(--gold);
      color: var(--gold);
      padding: 0.5rem 1.2rem;
      border-radius: 50px;
      font-size: 0.9rem;
      margin-bottom: 1.5rem;
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
    }

    /* Buttons */
    .btn {
      padding: 0.9rem 2rem;
      border-radius: 4px;
      text-decoration: none;
      font-weight: 600;
      transition: all 0.3s ease;
      display: inline-flex;
      align-items: center;
      gap: 0.6rem;
      cursor: pointer;
    }

    .btn-gold {
      background: var(--gold);
      color: #000;
    }

    .btn-gold:hover {
      background: var(--gold-hover);
      transform: translateY(-2px);
      box-shadow: 0 8px 20px rgba(212, 175, 55, 0.3);
    }

    .btn-outline {
      border: 1px solid var(--gold);
      color: var(--gold);
      margin-left: 1rem;
    }

    .btn-outline:hover {
      background: rgba(212, 175, 55, 0.1);
    }

    /* Menu & Gallery Section */
    .section {
      padding: 6rem 8%;
    }

    .section-title {
      text-align: center;
      margin-bottom: 4rem;
    }

    .section-title h2 {
      font-family: 'Cinzel', serif;
      font-size: 2.5rem;
      color: var(--gold);
    }

    .grid-container {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 2rem;
    }

    .card {
      background: var(--card-bg);
      border: 1px solid rgba(255,255,255,0.05);
      border-radius: 12px;
      overflow: hidden;
      transition: 0.4s ease;
    }

    .card:hover {
      transform: translateY(-8px);
      border-color: var(--gold);
      box-shadow: 0 10px 30px rgba(0,0,0,0.5);
    }

    .card-img {
      height: 220px;
      background-size: cover;
      background-position: center;
    }

    .card-body {
      padding: 1.5rem;
    }

    .card-body h3 {
      font-family: 'Cinzel', serif;
      margin-bottom: 0.5rem;
    }

    .price {
      color: var(--gold);
      font-weight: 600;
      font-size: 1.1rem;
      margin-top: 1rem;
      display: block;
    }

    /* Features List */
    .features {
      display: flex;
      justify-content: center;
      gap: 2rem;
      flex-wrap: wrap;
      margin-top: 3rem;
    }

    .feature-item {
      background: rgba(255,255,255,0.03);
      padding: 1rem 1.8rem;
      border-radius: 8px;
      border-left: 3px solid var(--gold);
      display: flex;
      align-items: center;
      gap: 0.8rem;
    }

    /* Contact & Location */
    .contact-container {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 3rem;
      align-items: center;
    }

    .info-box {
      background: var(--card-bg);
      padding: 2.5rem;
      border-radius: 12px;
      border: 1px solid rgba(212, 175, 55, 0.2);
    }

    .info-item {
      display: flex;
      align-items: flex-start;
      gap: 1rem;
      margin-bottom: 1.5rem;
    }

    .info-item i {
      color: var(--gold);
      font-size: 1.3rem;
      margin-top: 0.2rem;
    }

    /* Floating WhatsApp Button */
    .whatsapp-float {
      position: fixed;
      bottom: 2rem;
      right: 2rem;
      background: #25d366;
      color: white;
      width: 60px;
      height: 60px;
      border-radius: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 2rem;
      box-shadow: 0 5px 20px rgba(37, 211, 102, 0.4);
      z-index: 1000;
      text-decoration: none;
      transition: 0.3s;
    }

    .whatsapp-float:hover {
      transform: scale(1.1);
    }

    @media (max-width: 768px) {
      .hero h1 { font-size: 2.5rem; }
      .contact-container { grid-template-columns: 1fr; }
      .nav-links { display: none; }
    }
  </style>
</head>
<body>

  <header>
    <a href="#" class="logo">HAN ET HOUSE</a>
    <ul class="nav-links">
      <li><a href="#about">Hakkımızda</a></li>
      <li><a href="#menu">Öne Çıkanlar</a></li>
      <li><a href="#contact">İletişim & Konum</a></li>
    </ul>
  </header>

  <section class="hero">
    <div class="badge" data-aos="fade-down">
      <i class="fa-solid fa-star"></i> 4.6 Google Puanı (287+ Değerlendirme)
    </div>
    <h1 data-aos="fade-up">Kusursuz Lezzet, Unutulmaz Deneyim</h1>
    <p data-aos="fade-up" data-aos-delay="100">Tokat'ın kalbinde özel marinasyonlu kuzu lokum ve usta ellerden çıkan eşsiz steak lezzetleri.</p>
    <div data-aos="fade-up" data-aos-delay="200">
      <a href="https://wa.me/905462124888" target="_blank" class="btn btn-gold">
        <i class="fa-brands fa-whatsapp"></i> Rezerve Et
      </a>
      <a href="#menu" class="btn btn-outline">Menüyü İncele</a>
    </div>
  </section>

  <section id="about" class="section">
    <div class="features" data-aos="fade-up">
      <div class="feature-item"><i class="fa-solid fa-fire-flame-curved" style="color:var(--gold)"></i> Şömine Başında Keyif</div>
      <div class="feature-item"><i class="fa-solid fa-clock-rotate-left" style="color:var(--gold)"></i> İndirimli Saatler</div>
      <div class="feature-item"><i class="fa-solid fa-child" style="color:var(--gold)"></i> Özel Çocuk Menüsü</div>
    </div>
  </section>

  <section id="menu" class="section" style="background: rgba(0,0,0,0.5);">
    <div class="section-title" data-aos="fade-up">
      <h2>İmza Lezzetlerimiz</h2>
      <p style="color:var(--text-muted); margin-top:0.5rem;">Özenle seçilmiş ve dinlendirilmiş et çeşitleri</p>
    </div>

    <div class="grid-container">
      <div class="card" data-aos="fade-up">
        <div class="card-img" style="background-image: url('https://images.unsplash.com/photo-1558030006-450675393462?auto=format&fit=crop&w=800&q=80');"></div>
        <div class="card-body">
          <h3>Kuzu Lokum</h3>
          <p style="color:var(--text-muted); font-size:0.9rem;">Özel baharatlarla marine edilmiş, tereyağında pamuk gibi kuzu pirzola dilimleri.</p>
          <span class="price">₺600 - ₺800</span>
        </div>
      </div>

      <div class="card" data-aos="fade-up" data-aos-delay="100">
        <div class="card-img" style="background-image: url('https://images.unsplash.com/photo-1600891964092-4316c288032e?auto=format&fit=crop&w=800&q=80');"></div>
        <div class="card-body">
          <h3>T-Bone Steak</h3>
          <p style="color:var(--text-muted); font-size:0.9rem;">28 gün kuru dinlendirilmiş, döküm tavada mühürlenmiş premium kesim.</p>
          <span class="price">₺1.000 - ₺1.400</span>
        </div>
      </div>

      <div class="card" data-aos="fade-up" data-aos-delay="200">
        <div class="card-img" style="background-image: url('https://images.unsplash.com/photo-1544025162-d76694265947?auto=format&fit=crop&w=800&q=80');"></div>
        <div class="card-body">
          <h3>Özel Izgara Tabağı</h3>
          <p style="color:var(--text-muted); font-size:0.9rem;">Közlenmiş sebzeler ve özel sos eşliğinde servis edilen karışık steak tabağı.</p>
          <span class="price">₺800 - ₺1.200</span>
        </div>
      </div>
    </div>
  </section>

  <section id="contact" class="section">
    <div class="contact-container">
      <div class="info-box" data-aos="fade-right">
        <h2 style="font-family:'Cinzel', serif; color:var(--gold); margin-bottom:1.5rem;">Sizi Ağırlamaktan Mutluluk Duyarız</h2>
        
        <div class="info-item">
          <i class="fa-solid fa-location-dot"></i>
          <div>
            <strong>Adres:</strong>
            <p style="color:var(--text-muted);">Yeşilırmak, Sıtkı Ulaşoğlu 2. Sk., 60030 Tokat Merkez/Tokat</p>
          </div>
        </div>

        <div class="info-item">
          <i class="fa-solid fa-phone"></i>
          <div>
            <strong>Telefon:</strong>
            <p style="color:var(--text-muted);">(0356) 212 48 88</p>
          </div>
        </div>

        <div class="info-item">
          <i class="fa-solid fa-clock"></i>
          <div>
            <strong>Çalışma Saatleri:</strong>
            <p style="color:var(--text-muted);">Cumartesi: 09:00–00:00 | Pazar: 09:00–22:00</p>
            <p style="color:var(--text-muted);">Hafta İçi: 09:00–23:30</p>
          </div>
        </div>

        <div style="margin-top:2rem;">
          <a href="https://maps.google.com/?q=Yeşilırmak,Sıtkı+Ulaşoğlu+2.+Sk.,60030+Tokat+Merkez/Tokat" target="_blank" class="btn btn-gold">
            <i class="fa-solid fa-diamond-turn-right"></i> Yol Tarifi Al
          </a>
        </div>
      </div>

      <div style="border-radius:12px; overflow:hidden; border:1px solid rgba(212,175,55,0.2); height:100%; min-height:350px;" data-aos="fade-left">
        <iframe 
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3032.548873767087!2d36.545!3d40.316!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zNDDCsDE4JNTcuNiJOIDM2wrAzMic0Mi4wIkU!5e0!3m2!1str!2str!4v1620000000000!5m2!1str!2str" 
          width="100%" 
          height="100%" 
          style="border:0;" 
          allowfullscreen="" 
          loading="lazy">
        </iframe>
      </div>
    </div>
  </section>

  <a href="https://wa.me/905462124888" target="_blank" class="whatsapp-float">
    <i class="fa-brands fa-whatsapp"></i>
  </a>

  <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
  <script>
    // Animasyon Kütüphanesi Başlatma
    AOS.init({
      duration: 1000,
      once: true
    });
  </script>
</body>
</html>
