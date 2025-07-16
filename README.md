<!DOCTYPE html>
<html lang="pt-br">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <meta name="description" content="Agência MBR especializada em tráfego pago para Google, Facebook e Instagram." />
  <title>MBR | Agência de Tráfego Pago</title>

  <!-- Fonte Poppins e Font Awesome -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap" rel="stylesheet" />
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css" />
  <link rel="stylesheet" href="https://unpkg.com/aos@2.3.4/dist/aos.css" />

  <style>
    /* Reset e base */
    *, *::before, *::after {
      margin: 0; padding: 0; box-sizing: border-box;
    }
    body {
      font-family: 'Poppins', sans-serif;
      background: url('https://www.transparenttextures.com/patterns/dark-mosaic.png') repeat #111;
      color: #eee;
      min-height: 100vh;
      display: flex;
      flex-direction: column;
      scroll-behavior: smooth;
    }

    /* HEADER */
    header {
      background-color: #1a1a1a;
      padding: 20px 40px;
      box-shadow: 0 2px 10px rgba(0,0,0,0.7);
      position: sticky;
      top: 0;
      z-index: 100;
    }

    .logo-container {
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    svg.logo {
      width: 220px;
      height: 80px;
      user-select: none;
      cursor: default;
    }

    .logo-subtitle {
      margin-top: 6px;
      font-style: italic;
      color: #d4af37;
      font-weight: 600;
      letter-spacing: 1.1px;
      text-shadow: 0 0 6px #d4af37a1;
      user-select: none;
    }

    nav {
      margin-top: 15px;
      display: flex;
      justify-content: center;
      gap: 28px;
      flex-wrap: wrap;
    }

    nav a {
      color: #d4af37;
      font-weight: 600;
      text-decoration: none;
      font-size: 1.1rem;
      padding: 6px 12px;
      border-radius: 6px;
      transition: background-color 0.3s ease, color 0.3s ease;
      user-select: none;
    }

    nav a:hover, nav a:focus {
      background-color: #d4af37;
      color: #1a1a1a;
      outline: none;
    }

    /* HERO com fundo melhorado */
    .hero {
      position: relative;
      padding: 100px 20px 80px;
      text-align: center;
      background: 
        linear-gradient(135deg, rgba(212, 175, 55, 0.2) 0%, rgba(0, 0, 0, 0.85) 70%),
        url('https://images.unsplash.com/photo-1611078489935-cd4f0e94c2c6?auto=format&fit=crop&w=1400&q=80') center/cover no-repeat;
      color: white;
      overflow: hidden;
      flex-grow: 1;
      box-shadow: inset 0 0 150px 50px rgba(212, 175, 55, 0.4);
    }
    .hero::before {
      content: "";
      position: absolute;
      inset: 0;
      background: radial-gradient(circle at top right, rgba(212, 175, 55, 0.3), transparent 70%);
      z-index: 0;
      pointer-events: none;
    }
    .hero-content {
      position: relative;
      z-index: 1;
      max-width: 720px;
      margin: 0 auto;
    }
    .hero h1 {
      font-size: 3.5rem;
      font-weight: 700;
      margin-bottom: 20px;
      text-shadow: 0 0 10px #d4af37cc;
    }
    .hero p {
      font-size: 1.3rem;
      margin-bottom: 40px;
      line-height: 1.5;
      text-shadow: 0 0 6px #000;
    }
    .btn-cta {
      background-color: #d4af37;
      color: #1a1a1a;
      font-weight: 700;
      padding: 16px 40px;
      font-size: 1.2rem;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      text-decoration: none;
      box-shadow: 0 0 15px #d4af37bb;
      transition: background-color 0.3s ease, color 0.3s ease;
      user-select: none;
      display: inline-block;
    }
    .btn-cta:hover,
    .btn-cta:focus {
      background-color: #b39327;
      color: #fff;
      outline: none;
      box-shadow: 0 0 20px #b3932799;
    }

    /* SECTIONS */
    section {
      max-width: 960px;
      margin: 60px auto;
      padding: 0 20px;
      text-align: center;
    }
    section h2 {
      font-size: 2.5rem;
      color: #d4af37;
      margin-bottom: 24px;
      text-shadow: 0 0 8px #d4af37aa;
      user-select: none;
    }
    section p {
      font-size: 1.15rem;
      color: #ccc;
      max-width: 700px;
      margin: 0 auto;
      line-height: 1.6;
    }

    /* FORM */
    form {
      max-width: 600px;
      margin: 0 auto;
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
    input, textarea {
      background-color: #222;
      color: #eee;
      border: 1.5px solid #444;
      border-radius: 8px;
      padding: 14px 18px;
      font-size: 1rem;
      font-family: inherit;
      transition: border-color 0.3s ease;
      resize: vertical;
      user-select: text;
    }
    input:focus, textarea:focus {
      outline: none;
      border-color: #d4af37;
      box-shadow: 0 0 8px #d4af37bb;
    }
    button[type="submit"] {
      background-color: #d4af37;
      color: #1a1a1a;
      font-weight: 700;
      font-size: 1.2rem;
      border: none;
      border-radius: 30px;
      padding: 14px 0;
      cursor: pointer;
      box-shadow: 0 0 12px #d4af37bb;
      transition: background-color 0.3s ease;
      user-select: none;
    }
    button[type="submit"]:hover,
    button[type="submit"]:focus {
      background-color: #b39327;
      color: #fff;
      outline: none;
      box-shadow: 0 0 15px #b3932799;
    }

    /* FOOTER */
    footer {
      background-color: #111;
      color: #777;
      text-align: center;
      padding: 25px 10px;
      font-size: 0.9rem;
      user-select: none;
    }

    /* WHATSAPP FLUTUANTE */
    .whatsapp-float {
      position: fixed;
      bottom: 20px;
      right: 20px;
      background-color: #25d366;
      color: white;
      width: 60px;
      height: 60px;
      border-radius: 50%;
      box-shadow: 0 0 12px #25d366cc;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 32px;
      z-index: 9999;
      transition: background-color 0.3s ease;
      user-select: none;
    }
    .whatsapp-float:hover,
    .whatsapp-float:focus {
      background-color: #1ebe57;
      outline: none;
      box-shadow: 0 0 18px #1ebe5799;
      cursor: pointer;
    }

    /* RESPONSIVIDADE */
    @media (max-width: 768px) {
      .hero h1 {
        font-size: 2.5rem;
      }
      nav a {
        font-size: 1rem;
      }
      section h2 {
        font-size: 2rem;
      }
    }
    @media (max-width: 480px) {
      header {
        padding: 15px 20px;
      }
      nav {
        gap: 15px;
      }
      .hero {
        padding: 80px 15px 60px;
      }
      .hero h1 {
        font-size: 1.8rem;
      }
      .btn-cta {
        padding: 14px 28px;
        font-size: 1rem;
      }
    }
  </style>
</head>
<body>

  <header role="banner">
    <div class="logo-container" aria-label="Logo da Agência MBR de Tráfego Pago">
      <svg class="logo" viewBox="0 0 220 80" role="img" aria-labelledby="logoTitle logoDesc" xmlns="http://www.w3.org/2000/svg" >
        <title id="logoTitle">Logo MBR</title>
        <desc id="logoDesc">Logo dourada 3D com sombra e brilho</desc>
        <defs>
          <linearGradient id="gold3D" x1="0" y1="0" x2="0" y2="1">
            <stop offset="0%" stop-color="#fff8c6" />
            <stop offset="30%" stop-color="#ffd700" />
            <stop offset="70%" stop-color="#d4af37" />
            <stop offset="100%" stop-color="#a67c00" />
          </linearGradient>
          <filter id="logoShadow" x="-20%" y="-20%" width="140%" height="140%">
            <feDropShadow dx="3" dy="3" stdDeviation="3" flood-color="#000" flood-opacity="0.5" />
          </filter>
          <filter id="logoGlow">
            <feDropShadow dx="0" dy="0" stdDeviation="3" flood-color="#fff9ae" flood-opacity="0.8"/>
          </filter>
        </defs>
        <text x="50%" y="60%" text-anchor="middle"
              font-family="Poppins, Segoe UI, sans-serif"
              font-size="64"
              font-weight="700"
              fill="url(#gold3D)"
              filter="url(#logoShadow)">
          MBR
        </text>
        <text x="50%" y="60%" text-anchor="middle"
              font-family="Poppins, Segoe UI, sans-serif"
              font-size="64"
              font-weight="700"
              fill="none"
              stroke="#fff"
              stroke-width="0.5"
              filter="url(#logoGlow)"
              opacity="0.4">
          MBR
        </text>
      </svg>
      <span class="logo-subtitle">Agência de Tráfego Pago</span>
    </div>

    <nav role="navigation" aria-label="Menu principal">
      <a href="#servicos" tabindex="0">Serviços</a>
      <a href="#sobre" tabindex="0">Sobre</a>
      <a href="#contato" tabindex="0">Contato</a>
    </nav>
  </header>

  <main role="main">
    <section class="hero" aria-label="Apresentação principal da agência" data-aos="fade-in">
      <div class="hero-content">
        <h1>Impulsione suas vendas com tráfego pago</h1>
        <p>Especialistas em campanhas no Google, Facebook e Instagram para atrair clientes e aumentar suas conversões.</p>
        <a href="https://wa.me/47991701067" target="_blank" rel="noopener" class="btn-cta" aria-label="Fale conosco no WhatsApp">Fale no WhatsApp</a>
      </div>
    </section>

    <section id="servicos" aria-labelledby="servicosTitle" data-aos="fade-up">
      <h2 id="servicosTitle"><i class="fas fa-bullhorn" aria-hidden="true"></i> Nossos Serviços</h2>
      <p>Gestão completa de tráfego pago com campanhas otimizadas no Google Ads, Facebook Ads e Instagram. Estratégias inteligentes e personalizadas para gerar leads e aumentar suas vendas.</p>
    </section>

    <section id="sobre" aria-labelledby="sobreTitle" data-aos="fade-up">
      <h2 id="sobreTitle"><i class="fas fa-chart-line" aria-hidden="true"></i> Sobre a MBR</h2>
      <p>Somos uma agência de performance digital focada em resultados reais. Utilizamos inteligência de dados, criatividade e análise para impulsionar negócios com tráfego pago.</p>
    </section>

    <section id="contato" aria-labelledby="contatoTitle" data-aos="fade-up">
      <h2 id="contatoTitle"><i class="fas fa-envelope" aria-hidden="true"></i> Fale Conosco</h2>
      <form action="https://formsubmit.co/SEUEMAIL@DOMINIO.COM" method="POST" aria-label="Formulário de contato">
        <input type="hidden" name="_captcha" value="false" />
        <input type="hidden" name="_next" value="obrigado.html" />
        <input type="text" name="nome" placeholder="Seu nome" required aria-required="true" />
        <input type="email" name="email" placeholder="Seu e-mail" required aria-required="true" />
        <textarea name="mensagem" rows="5" placeholder="Sua mensagem" required aria-required="true"></textarea>
        <button type="submit">Enviar Mensagem</button>
      </form>
    </section>
  </main>

  <footer role="contentinfo">
    &copy; 2025 MBR Agência de Tráfego Pago. Todos os direitos reservados.
  </footer>

  <!-- Botão flutuante WhatsApp -->
  <a href="https://wa.me/47991701067" class="whatsapp-float" target="_blank" rel="noopener" aria-label="WhatsApp da MBR Agência">
    <i class="fab fa-whatsapp" aria-hidden="true"></i>
  </a>

  <!-- Scripts -->
  <script src="https://unpkg.com/aos@2.3.4/dist/aos.js"></script>
  <script>
    AOS.init({
      duration: 800,
      once: true,
      easing: 'ease-in-out',
    });
  </script>
</body>
</html>
