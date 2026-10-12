<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Riya Fathima | Portfolio</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0b1120;
      --card-bg: rgba(30, 41, 59, 0.7);
      --text-main: #f8fafc;
      --text-muted: #94a3b8;
      --accent: #38bdf8;
      --accent-secondary: #818cf8;
      --border: #334155;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Poppins', sans-serif;
    }

    body {
      background-color: var(--bg);
      background-image: 
        radial-gradient(at 0% 0%, rgba(56, 189, 248, 0.12) 0px, transparent 50%),
        radial-gradient(at 100% 100%, rgba(129, 140, 248, 0.12) 0px, transparent 50%);
      background-attachment: fixed;
      color: var(--text-main);
      line-height: 1.6;
      padding-bottom: 50px;
      overflow-x: hidden;
    }

    /* Keyframe Animations */
    @keyframes fadeInUp {
      from {
        opacity: 0;
        transform: translateY(24px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    @keyframes floatBadge {
      0%, 100% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(-5px);
      }
    }

    @keyframes gradientShift {
      0% {
        background-position: 0% 50%;
      }
      50% {
        background-position: 100% 50%;
      }
      100% {
        background-position: 0% 50%;
      }
    }

    /* Navigation */
    nav {
      position: sticky;
      top: 0;
      background: rgba(11, 17, 32, 0.85);
      backdrop-filter: blur(12px);
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 1.5rem;
      border-bottom: 1px solid rgba(51, 65, 85, 0.7);
      z-index: 100;
      animation: fadeInUp 0.6s ease-out;
    }

    .logo {
      font-weight: 700;
      font-size: 1.25rem;
      color: var(--accent);
      letter-spacing: 0.5px;
    }

    .nav-links a {
      color: var(--text-muted);
      text-decoration: none;
      margin-left: 1rem;
      font-size: 0.85rem;
      transition: color 0.25s ease;
    }

    .nav-links a:hover {
      color: var(--accent);
    }

    /* Container */
    .container {
      max-width: 900px;
      margin: 0 auto;
      padding: 2rem 1.25rem;
    }

    /* Hero Section */
    .hero {
      text-align: center;
      padding: 2.5rem 0 3rem;
      animation: fadeInUp 0.8s ease-out;
    }

    .badge {
      display: inline-block;
      background: rgba(56, 189, 248, 0.12);
      color: var(--accent);
      padding: 0.35rem 0.9rem;
      border-radius: 20px;
      font-size: 0.8rem;
      font-weight: 600;
      margin-bottom: 1.2rem;
      border: 1px solid rgba(56, 189, 248, 0.4);
      animation: floatBadge 3.5s ease-in-out infinite;
      box-shadow: 0 0 15px rgba(56, 189, 248, 0.2);
    }

    .hero h1 {
      font-size: 2.3rem;
      line-height: 1.2;
      margin-bottom: 1rem;
    }

    .animated-name {
      background: linear-gradient(90deg, #38bdf8, #818cf8, #38bdf8);
      background-size: 200% auto;
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      animation: gradientShift 4s ease infinite;
      font-weight: 700;
    }

    .hero p {
      color: var(--text-muted);
      font-size: 1rem;
      max-width: 600px;
      margin: 0 auto 1.5rem;
    }

    .btn-group {
      display: flex;
      justify-content: center;
      gap: 0.75rem;
    }

    .btn {
      display: inline-block;
      padding: 0.65rem 1.3rem;
      border-radius: 8px;
      text-decoration: none;
      font-size: 0.9rem;
      font-weight: 600;
      transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
    }

    .btn-primary {
      background: var(--accent);
      color: #0b1120;
      box-shadow: 0 4px 14px rgba(56, 189, 248, 0.35);
    }

    .btn-primary:hover {
      transform: translateY(-2px);
      box-shadow: 0 6px 20px rgba(56, 189, 248, 0.55);
    }

    .btn-outline {
      border: 1px solid var(--border);
      color: var(--text-main);
      background: rgba(15, 23, 42, 0.6);
    }

    .btn-outline:hover {
      border-color: var(--accent);
      color: var(--accent);
      transform: translateY(-2px);
    }

    /* Sections */
    section {
      margin-top: 3.5rem;
      animation: fadeInUp 0.9s ease-out;
    }

    h2 {
      font-size: 1.5rem;
      margin-bottom: 1.2rem;
      position: relative;
      display: inline-block;
    }

    h2::after {
      content: '';
      position: absolute;
      left: 0;
      bottom: -6px;
      width: 45px;
      height: 3px;
      background: linear-gradient(90deg, var(--accent), var(--accent-secondary));
      border-radius: 2px;
    }

    /* Cards & Grids */
    .grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 1.2rem;
      margin-top: 1rem;
    }

    @media (min-width: 650px) {
      .grid {
        grid-template-columns: repeat(2, 1fr);
      }
    }

    .card {
      background: var(--card-bg);
      backdrop-filter: blur(8px);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 1.35rem;
      transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
      position: relative;
    }

    .card:hover {
      border-color: var(--accent);
      transform: translateY(-5px);
      box-shadow: 0 10px 25px -5px rgba(56, 189, 248, 0.2);
    }

    .card h3 {
      font-size: 1.15rem;
      margin-bottom: 0.5rem;
      color: #fff;
    }

    .card p {
      color: var(--text-muted);
      font-size: 0.85rem;
      margin-bottom: 1rem;
    }

    .tag-container {
      display: flex;
      flex-wrap: wrap;
      gap: 0.45rem;
    }

    .tag {
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid rgba(255, 255, 255, 0.1);
      color: var(--accent);
      font-size: 0.75rem;
      padding: 0.25rem 0.6rem;
      border-radius: 6px;
      transition: background 0.2s;
    }

    .tag:hover {
      background: rgba(56, 189, 248, 0.15);
    }

    /* Contact Card */
    .contact-card {
      background: var(--card-bg);
      backdrop-filter: blur(8px);
      border: 1px solid var(--border);
      border-radius: 14px;
      padding: 1.6rem;
      text-align: center;
      margin-top: 1rem;
      transition: all 0.3s ease;
    }

    .contact-card:hover {
      border-color: var(--accent-secondary);
      box-shadow: 0 10px 25px -5px rgba(129, 140, 248, 0.2);
    }

    .contact-card a {
      color: var(--accent);
      text-decoration: none;
      word-break: break-all;
    }

    footer {
      text-align: center;
      margin-top: 4rem;
      color: var(--text-muted);
      font-size: 0.8rem;
    }
  </style>
</head>
<body>

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
    <!-- Hero -->
    <header class="hero">
      <div class="badge">Available for Projects & Collaboration</div>
      <h1>Hi, I'm <span class="animated-name">Riya Fathima</span></h1>
      <p>Computer Science & Engineering student building automated embedded IoT systems, software tools, and digital experiences.</p>
      <div class="btn-group">
        <a href="#projects" class="btn btn-primary">View Projects</a>
        <a href="#contact" class="btn btn-outline">Get in Touch</a>
      </div>
    </header>

    <!-- About -->
    <section id="about">
      <h2>About Me</h2>
      <div class="card" style="margin-top: 1rem;">
        <p>
          I am a passionate Computer Science student exploring microcontroller prototyping, systems programming, and design. I love bridging physical hardware with clean software logic to solve practical everyday problems.
        </p>
      </div>
    </section>

    <!-- Skills -->
    <section id="skills">
      <h2>Technical Toolkit</h2>
      <div class="grid">
        <div class="card">
          <h3>Languages & Systems</h3>
          <p>Core programming fundamentals and system concepts.</p>
          <div class="tag-container">
            <span class="tag">C</span>
            <span class="tag">C++</span>
            <span class="tag">Operating Systems</span>
            <span class="tag">DSA</span>
          </div>
        </div>

        <div class="card">
          <h3>Hardware & Prototyping</h3>
          <p>Microcontrollers, electronics, and sensor integrations.</p>
          <div class="tag-container">
            <span class="tag">NodeMCU</span>
            <span class="tag">Arduino</span>
            <span class="tag">Relay Modules</span>
            <span class="tag">Sensors</span>
          </div>
        </div>

        <div class="card">
          <h3>Web & Design Tools</h3>
          <p>Building intuitive visual interfaces and graphics.</p>
          <div class="tag-container">
            <span class="tag">HTML5 / CSS3</span>
            <span class="tag">JavaScript</span>
            <span class="tag">Canva</span>
            <span class="tag">Git & GitHub</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Projects -->
    <section id="projects">
      <h2>Featured Projects</h2>
      <div class="grid">
        <div class="card">
          <h3>Smart Soil Moisture Irrigation System</h3>
          <p>An automated irrigation unit built with NodeMCU, FC-28 soil moisture sensors, and a relay module that delivers water automatically based on threshold moisture readings.</p>
          <div class="tag-container">
            <span class="tag">NodeMCU</span>
            <span class="tag">IoT</span>
            <span class="tag">Embedded C</span>
            <span class="tag">Relay Circuit</span>
          </div>
        </div>

        <div class="card">
          <h3>CPU Scheduling Simulator</h3>
          <p>An algorithmic implementation analyzing process execution times, turnaround metrics, and wait times using classic scheduling models like SJF and SRTF.</p>
          <div class="tag-container">
            <span class="tag">C</span>
            <span class="tag">Algorithms</span>
            <span class="tag">OS Concepts</span>
          </div>
        </div>

        <div class="card">
          <h3>Tech Summit Event Branding</h3>
          <p>Complete visual branding identity, typography systems, and promotional collateral design for national-level collegiate tech summit sessions.</p>
          <div class="tag-container">
            <span class="tag">Canva</span>
            <span class="tag">Visual Identity</span>
            <span class="tag">Typography</span>
          </div>
        </div>
      </div>
    </section>

    <!-- Contact -->
    <section id="contact">
      <h2>Let's Connect</h2>
      <div class="contact-card">
        <p style="margin-bottom: 0.5rem; color: #fff; font-weight: 600;">Have a project or opportunity in mind?</p>
        <p style="margin-bottom: 1rem;">Feel free to drop a message or view my code repositories.</p>
        <p>Email: <a href="mailto:your-email@example.com">your-email@example.com</a></p>
      </div>
    </section>

    <footer>
      <p>© 2026 Riya Fathima. Built and coded directly on mobile.</p>
    </footer>
  </div>

</body>
</html>
