<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Riya Fathima | Portfolio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700;800&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #070d19;
      --card-bg: rgba(15, 23, 42, 0.75);
      --text-main: #f8fafc;
      --text-muted: #94a3b8;
      --accent: #38bdf8;
      --accent-secondary: #a855f7;
      --border: rgba(51, 65, 85, 0.6);
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background-color: var(--bg);
      color: var(--text-main);
      line-height: 1.6;
      padding-bottom: 60px;
      overflow-x: hidden;
      position: relative;
    }

    /* Animated Glowing Background Blobs */
    .blob {
      position: fixed;
      width: 280px;
      height: 280px;
      border-radius: 50%;
      filter: blur(80px);
      z-index: -1;
      opacity: 0.35;
      pointer-events: none;
      animation: floatBlobs 12s infinite alternate ease-in-out;
    }
    .blob-1 {
      top: -60px;
      left: -60px;
      background: #38bdf8;
    }
    .blob-2 {
      bottom: 20%;
      right: -80px;
      background: #a855f7;
      animation-delay: -6s;
    }

    @keyframes floatBlobs {
      0% { transform: translate(0, 0) scale(1); }
      50% { transform: translate(40px, 60px) scale(1.15); }
      100% { transform: translate(-30px, 30px) scale(0.9); }
    }

    /* Staggered Entry Animation */
    @keyframes slideUp {
      from {
        opacity: 0;
        transform: translateY(28px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    /* Gradient Text Animation */
    @keyframes gradientShift {
      0% { background-position: 0% 50%; }
      50% { background-position: 100% 50%; }
      100% { background-position: 0% 50%; }
    }

    /* Pulse Glow */
    @keyframes pulseRing {
      0% { box-shadow: 0 0 0 0 rgba(56, 189, 248, 0.5); }
      70% { box-shadow: 0 0 0 12px rgba(56, 189, 248, 0); }
      100% { box-shadow: 0 0 0 0 rgba(56, 189, 248, 0); }
    }

    /* Navbar */
    nav {
      position: sticky;
      top: 0;
      background: rgba(7, 13, 25, 0.85);
      backdrop-filter: blur(14px);
      -webkit-backdrop-filter: blur(14px);
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1.1rem 1.4rem;
      border-bottom: 1px solid var(--border);
      z-index: 100;
      animation: slideUp 0.6s ease-out;
    }

    .logo {
      font-weight: 800;
      font-size: 1.3rem;
      background: linear-gradient(135deg, var(--accent), var(--accent-secondary));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      letter-spacing: 1px;
    }

    .nav-links a {
      color: var(--text-muted);
      text-decoration: none;
      margin-left: 1.1rem;
      font-size: 0.85rem;
      font-weight: 500;
      transition: color 0.25s ease;
    }

    .nav-links a:hover {
      color: var(--accent);
    }

    /* Container */
    .container {
      max-width: 820px;
      margin: 0 auto;
      padding: 2rem 1.25rem;
    }

    /* Hero */
    .hero {
      text-align: center;
      padding: 3rem 0 3.5rem;
      animation: slideUp 0.8s ease-out backwards;
    }

    .status-badge {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      background: rgba(56, 189, 248, 0.1);
      border: 1px solid rgba(56, 189, 248, 0.35);
      padding: 0.4rem 1rem;
      border-radius: 999px;
      font-size: 0.78rem;
      font-weight: 600;
      color: var(--accent);
      margin-bottom: 1.4rem;
      animation: pulseRing 3s infinite;
    }

    .status-dot {
      width: 8px;
      height: 8px;
      background-color: #38bdf8;
      border-radius: 50%;
    }

    .hero h1 {
      font-size: 2.3rem;
      line-height: 1.25;
      font-weight: 700;
      margin-bottom: 1.1rem;
    }

    .animated-text {
      background: linear-gradient(90deg, #38bdf8, #a855f7, #ec4899, #38bdf8);
      background-size: 300% 300%;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: gradientShift 6s ease infinite;
      font-weight: 800;
    }

    .hero p {
      color: var(--text-muted);
      font-size: 0.95rem;
      max-width: 580px;
      margin: 0 auto 1.8rem;
    }

    .btn-group {
      display: flex;
      justify-content: center;
      gap: 0.85rem;
    }

    .btn {
      padding: 0.7rem 1.4rem;
      border-radius: 10px;
      text-decoration: none;
      font-size: 0.88rem;
      font-weight: 600;
      transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    }

    .btn-primary {
      background: linear-gradient(135deg, var(--accent), #2563eb);
      color: #fff;
      box-shadow: 0 6px 20px rgba(56, 189, 248, 0.35);
    }

    .btn-primary:active,
    .btn-primary:hover {
      transform: translateY(-3px) scale(1.02);
      box-shadow: 0 10px 28px rgba(56, 189, 248, 0.55);
    }

    .btn-outline {
      background: rgba(15, 23, 42, 0.6);
      border: 1px solid var(--border);
      color: var(--text-main);
    }

    .btn-outline:active,
    .btn-outline:hover {
      border-color: var(--accent);
      color: var(--accent);
      transform: translateY(-3px);
    }

    /* Sections */
    section {
      margin-top: 3.2rem;
      animation: slideUp 0.9s ease-out backwards;
    }

    h2 {
      font-size: 1.4rem;
      margin-bottom: 1.2rem;
      position: relative;
      display: inline-block;
    }

    h2::after {
      content: '';
      position: absolute;
      left: 0;
      bottom: -6px;
      width: 40px;
      height: 3px;
      background: linear-gradient(90deg, var(--accent), var(--accent-secondary));
      border-radius: 4px;
    }

    /* Cards */
    .grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 1.2rem;
    }

    @media (min-width: 640px) {
      .grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }

    .card {
      background: var(--card-bg);
      backdrop-filter: blur(12px);
      -webkit-backdrop-filter: blur(12px);
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 1.4rem;
      transition: all 0.35s cubic-bezier(0.4, 0, 0.2, 1);
      position: relative;
      overflow: hidden;
    }

    /* Subtle Card Top Highlight */
    .card::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      right: 0;
      height: 2px;
      background: linear-gradient(90deg, transparent, var(--accent), transparent);
      opacity: 0;
      transition: opacity 0.3s ease;
    }

    .card:active,
    .card:hover {
      transform: translateY(-6px);
      border-color: rgba(56, 189, 248, 0.45);
      box-shadow: 0 14px 30px -8px rgba(56, 189, 248, 0.22);
    }

    .card:hover::before {
      opacity: 1;
    }

    .card h3 {
      font-size: 1.15rem;
      margin-bottom: 0.5rem;
      color: #fff;
    }

    .card p {
      color: var(--text-muted);
      font-size: 0.85rem;
      margin-bottom: 1.1rem;
    }

    /* Tag Pills */
    .tags {
      display: flex;
      flex-wrap: wrap;
      gap: 0.45rem;
    }

    .tag {
      background: rgba(255, 255, 255, 0.04);
      border: 1px solid rgba(255, 255, 255, 0.1);
      color: var(--accent);
      font-size: 0.74rem;
      padding: 0.3rem 0.65rem;
      border-radius: 8px;
      transition: all 0.25s ease;
    }

    .card:hover .tag {
      border-color: rgba(56, 189, 248, 0.35);
      background: rgba(56, 189, 248, 0.08);
    }

    /* Contact Section */
    .contact-card {
      background: linear-gradient(145deg, rgba(15, 23, 42, 0.85), rgba(30, 41, 59, 0.5));
      border: 1px solid var(--border);
      border-radius: 16px;
      padding: 2rem 1.4rem;
      text-align: center;
      transition: all 0.3s ease;
    }

    .contact-card:hover {
      border-color: var(--accent-secondary);
      box-shadow: 0 12px 32px rgba(168, 85, 247, 0.2);
    }

    .contact-card a {
      color: var(--accent);
      text-decoration: none;
      font-weight: 600;
    }

    footer {
      text-align: center;
      margin-top: 4.5rem;
      color: var(--text-muted);
      font-size: 0.8rem;
    }
  </style>
</head>
<body>

  <!-- Background Animated Lights -->
  <div class="blob blob-1"></div>
  <div class="blob blob-2"></div>

  <!-- Navigation -->
  <nav>
    <div class="logo">RF.</div>
    <div class="nav-links">
      <a href="#about">About</a>
      <a href="#skills">Skills</a>
      <a href="#projects">Projects</a>
      <a href="#contact">Contact</a>
    </div>
  </nav>

  <div class="container">
    <!-- Hero Section -->
    <header class="hero">
      <div class="status-badge">
        <span class="status-dot"></span>
        Available for Projects & Collaboration
      </div>
      <h1>Hi, I'm <span class="animated-text">Riya Fathima</span></h1>
      <p>Computer Science & Engineering student building automated embedded IoT circuits, software tools, and digital user experiences.</p>
      <div class="btn-group">
        <a href="#projects" class="btn btn-primary">View Projects</a>
        <a href="#contact" class="btn btn-outline">Get in Touch</a>
      </div>
    </header>

    <!-- About Section -->
    <section id="about">
      <h2>About Me</h2>
      <div class="card">
        <p>
          I am a passionate Computer Science student exploring microcontroller prototyping, embedded electronics, and software systems. I enjoy creating practical solutions that bridge physical hardware sensors with responsive, clean logic.
        </p>
      </div>
    </section>

    <!-- Technical Skills -->
    <section id="skills">
      <h2>Technical Toolkit</h2>
      <div class="grid">
        <div class="card">
          <h3>Languages & Systems</h3>
          <p>Core programming fundamentals and algorithmic logic.</p>
          <div class="tags">
            <span class="tag">C</span>
            <span class="tag">C++</span>
            <span class="tag">DSA</span>
            <span class="tag">Operating Systems</span>
          </div>
        </div>

        <div class="card">
          <h3>Hardware & IoT</h3>
          <p>Sensor integration and microcontroller circuits.</p>
          <div class="tags">
            <span class="tag">NodeMCU</span>
            <span class="tag">Arduino</span>
            <span class="tag">FC-28 Soil Sensor</span>
            <span class="tag">Relays</span>
          </div>
        </div>

        <div class="card">
          <h3>Web & Creative</h3>
          <p>Interface structuring and visual graphic workflows.</p>
          <div class="tags">
            <span class="tag">HTML5 / CSS3</span>
            <span class="tag">JavaScript</span>
            <span class="tag">Git & GitHub</span>
            <span class="tag">Canva UI Design</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Projects -->
    <section id="projects">
      <h2>Featured Projects</h2>
      <div class="grid">
        <div class="card">
          <h3>Smart Soil Irrigation System</h3>
          <p>An automated irrigation circuit using NodeMCU and FC-28 soil moisture sensors to trigger pump relays based on real-time soil thresholds.</p>
          <div class="tags">
            <span class="tag">NodeMCU</span>
            <span class="tag">IoT</span>
            <span class="tag">Embedded C</span>
            <span class="tag">Automation</span>
          </div>
        </div>

        <div class="card">
          <h3>CPU Scheduling Simulator</h3>
          <p>Algorithm implementations analyzing process turnaround and waiting metrics under SJF and SRTF scheduling architectures.</p>
          <div class="tags">
            <span class="tag">C</span>
            <span class="tag">Algorithms</span>
            <span class="tag">Operating Systems</span>
          </div>
        </div>

        <div class="card">
          <h3>Tech Summit Event Collateral</h3>
          <p>Visual branding identity, typography systems, and graphic promotional materials for collegiate tech events.</p>
          <div class="tags">
            <span class="tag">Canva</span>
            <span class="tag">Graphic Design</span>
            <span class="tag">Branding</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section id="contact">
      <h2>Let's Connect</h2>
      <div class="contact-card">
        <p style="color: #fff; font-weight: 600; font-size: 1.05rem; margin-bottom: 0.4rem;">Interested in collaborating or reviewing my work?</p>
        <p style="margin-bottom: 1.1rem;">Feel free to reach out directly via email or check my GitHub repositories.</p>
        <p>Email: <a href="mailto:riyafathima@example.com">riyafathima@example.com</a></p>
      </div>
    </section>

    <footer>
      <p>© 2026 Riya Fathima. Built & published live on GitHub Pages.</p>
    </footer>
  </div>

</body>
</html>
