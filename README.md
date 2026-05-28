<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Abdullah Tanveer - Full Stack Developer & AI Engineer</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
  <style>
    @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=JetBrains+Mono:wght@400;500&display=swap');

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --primary: #00d4ff;
      --secondary: #8b5cf6;
      --accent: #ec4899;
      --dark: #0f172a;
      --darker: #020617;
      --light: #f1f5f9;
      --text-primary: #ffffff;
      --text-secondary: #cbd5e1;
    }

    body {
      background: linear-gradient(135deg, var(--dark) 0%, #1a1f3a 50%, #16213e 100%);
      font-family: 'Poppins', sans-serif;
      color: var(--text-primary);
      overflow-x: hidden;
      min-height: 100vh;
    }

    .container {
      max-width: 1000px;
      margin: 0 auto;
      padding: 0 20px;
    }

    /* Animated Background Elements */
    .bg-gradient {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(45deg, rgba(0, 212, 255, 0.05) 0%, rgba(139, 92, 246, 0.05) 50%, rgba(236, 72, 153, 0.05) 100%);
      pointer-events: none;
      animation: float 6s ease-in-out infinite;
      z-index: 0;
    }

    @keyframes float {
      0%, 100% { transform: translateY(0px); }
      50% { transform: translateY(20px); }
    }

    .content {
      position: relative;
      z-index: 1;
    }

    /* Header */
    .header {
      text-align: center;
      padding: 60px 20px 40px;
      animation: slideInDown 0.8s ease-out;
    }

    @keyframes slideInDown {
      from {
        opacity: 0;
        transform: translateY(-30px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .header h1 {
      font-size: 56px;
      font-weight: 700;
      margin-bottom: 10px;
      background: linear-gradient(90deg, var(--primary), var(--secondary), var(--accent));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      animation: fadeInScale 1s ease-out;
    }

    @keyframes fadeInScale {
      from {
        opacity: 0;
        transform: scale(0.9);
      }
      to {
        opacity: 1;
        transform: scale(1);
      }
    }

    .header .tagline {
      font-size: 18px;
      color: var(--text-secondary);
      margin-bottom: 20px;
      font-weight: 300;
      letter-spacing: 1px;
      animation: slideInUp 0.8s ease-out 0.2s both;
    }

    @keyframes slideInUp {
      from {
        opacity: 0;
        transform: translateY(20px);
      }
      to {
        opacity: 1;
        transform: translateY(0);
      }
    }

    .badges-container {
      display: flex;
      gap: 12px;
      justify-content: center;
      flex-wrap: wrap;
      margin-top: 30px;
      animation: slideInUp 0.8s ease-out 0.4s both;
    }

    .badge {
      padding: 10px 18px;
      border: 2px solid;
      border-radius: 50px;
      font-size: 13px;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      cursor: pointer;
      transition: all 0.3s ease;
      position: relative;
      overflow: hidden;
    }

    .badge-1 {
      border-color: var(--primary);
      color: var(--primary);
    }

    .badge-1:hover {
      background: var(--primary);
      color: var(--dark);
      box-shadow: 0 0 20px rgba(0, 212, 255, 0.5);
      transform: translateY(-3px);
    }

    .badge-2 {
      border-color: var(--secondary);
      color: var(--secondary);
    }

    .badge-2:hover {
      background: var(--secondary);
      color: var(--text-primary);
      box-shadow: 0 0 20px rgba(139, 92, 246, 0.5);
      transform: translateY(-3px);
    }

    .badge-3 {
      border-color: var(--accent);
      color: var(--accent);
    }

    .badge-3:hover {
      background: var(--accent);
      color: var(--text-primary);
      box-shadow: 0 0 20px rgba(236, 72, 153, 0.5);
      transform: translateY(-3px);
    }

    /* Section Title */
    .section-title {
      font-size: 32px;
      font-weight: 700;
      margin: 60px 0 30px;
      position: relative;
      padding-bottom: 15px;
      animation: slideInLeft 0.8s ease-out;
    }

    @keyframes slideInLeft {
      from {
        opacity: 0;
        transform: translateX(-30px);
      }
      to {
        opacity: 1;
        transform: translateX(0);
      }
    }

    .section-title::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 0;
      height: 4px;
      background: linear-gradient(90deg, var(--primary), var(--secondary), var(--accent));
      animation: expandWidth 1s ease-out 0.3s forwards;
      border-radius: 2px;
    }

    @keyframes expandWidth {
      from { width: 0; }
      to { width: 60px; }
    }

    /* Projects Grid */
    .projects-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 24px;
      margin-bottom: 60px;
    }

    .project-card {
      background: linear-gradient(135deg, rgba(15, 23, 42, 0.8) 0%, rgba(30, 41, 59, 0.8) 100%);
      border: 2px solid rgba(0, 212, 255, 0.2);
      border-radius: 16px;
      padding: 24px;
      cursor: pointer;
      transition: all 0.4s cubic-bezier(0.175, 0.885, 0.32, 1.275);
      position: relative;
      overflow: hidden;
      backdrop-filter: blur(10px);
      animation: slideInUp 0.6s ease-out both;
    }

    .project-card:nth-child(1) { animation-delay: 0.1s; }
    .project-card:nth-child(2) { animation-delay: 0.2s; }
    .project-card:nth-child(3) { animation-delay: 0.3s; }
    .project-card:nth-child(4) { animation-delay: 0.4s; }

    .project-card::before {
      content: '';
      position: absolute;
      top: -50%;
      right: -50%;
      width: 200%;
      height: 200%;
      background: radial-gradient(circle, rgba(0, 212, 255, 0.1) 0%, transparent 70%);
      opacity: 0;
      transition: opacity 0.4s;
    }

    .project-card:hover::before {
      opacity: 1;
    }

    .project-card:hover {
      border-color: var(--primary);
      transform: translateY(-10px);
      box-shadow: 0 20px 40px rgba(0, 212, 255, 0.2), inset 0 1px 0 rgba(0, 212, 255, 0.1);
    }

    .project-icon {
      font-size: 32px;
      margin-bottom: 12px;
      animation: bounce 2s infinite;
    }

    .project-card:nth-child(2) .project-icon { animation-delay: 0.1s; }
    .project-card:nth-child(3) .project-icon { animation-delay: 0.2s; }
    .project-card:nth-child(4) .project-icon { animation-delay: 0.3s; }

    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-5px); }
    }

    .project-card h3 {
      font-size: 22px;
      font-weight: 600;
      margin-bottom: 8px;
      color: var(--primary);
    }

    .project-card .role {
      font-size: 12px;
      color: var(--accent);
      text-transform: uppercase;
      letter-spacing: 1px;
      margin-bottom: 12px;
      font-weight: 600;
    }

    .project-card p {
      font-size: 14px;
      color: var(--text-secondary);
      line-height: 1.6;
      margin-bottom: 16px;
    }

    .tech-stack {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin-top: 16px;
    }

    .tech-badge {
      background: rgba(0, 212, 255, 0.1);
      color: var(--primary);
      padding: 6px 12px;
      border-radius: 20px;
      font-size: 12px;
      font-weight: 500;
      border: 1px solid rgba(0, 212, 255, 0.3);
      transition: all 0.3s;
    }

    .tech-badge:hover {
      background: rgba(0, 212, 255, 0.2);
      border-color: var(--primary);
      transform: scale(1.05);
    }

    /* Skills Section */
    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
      gap: 20px;
      margin-bottom: 60px;
    }

    .skill-card {
      background: linear-gradient(135deg, rgba(15, 23, 42, 0.6) 0%, rgba(30, 41, 59, 0.6) 100%);
      border: 2px solid rgba(139, 92, 246, 0.2);
      border-radius: 12px;
      padding: 20px;
      transition: all 0.3s ease;
      animation: slideInUp 0.6s ease-out both;
      backdrop-filter: blur(10px);
    }

    .skill-card:nth-child(1) { animation-delay: 0.5s; }
    .skill-card:nth-child(2) { animation-delay: 0.6s; }
    .skill-card:nth-child(3) { animation-delay: 0.7s; }
    .skill-card:nth-child(4) { animation-delay: 0.8s; }
    .skill-card:nth-child(5) { animation-delay: 0.9s; }
    .skill-card:nth-child(6) { animation-delay: 1s; }

    .skill-card:hover {
      border-color: var(--secondary);
      transform: translateY(-5px);
      box-shadow: 0 15px 30px rgba(139, 92, 246, 0.2);
    }

    .skill-icon {
      font-size: 24px;
      margin-bottom: 10px;
    }

    .skill-card h4 {
      font-size: 16px;
      font-weight: 600;
      margin-bottom: 8px;
      color: var(--secondary);
    }

    .skill-card p {
      font-size: 13px;
      color: var(--text-secondary);
      line-height: 1.6;
    }

    /* Goals Section */
    .goals-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
      gap: 16px;
      margin-bottom: 60px;
    }

    .goal-item {
      background: linear-gradient(135deg, rgba(236, 72, 153, 0.1) 0%, rgba(139, 92, 246, 0.1) 100%);
      border: 2px solid rgba(236, 72, 153, 0.3);
      border-radius: 12px;
      padding: 20px;
      text-align: center;
      transition: all 0.3s ease;
      animation: slideInUp 0.6s ease-out both;
      position: relative;
      overflow: hidden;
    }

    .goal-item:nth-child(1) { animation-delay: 0.2s; }
    .goal-item:nth-child(2) { animation-delay: 0.3s; }
    .goal-item:nth-child(3) { animation-delay: 0.4s; }
    .goal-item:nth-child(4) { animation-delay: 0.5s; }
    .goal-item:nth-child(5) { animation-delay: 0.6s; }

    .goal-item::before {
      content: '';
      position: absolute;
      top: -50%;
      left: -50%;
      width: 200%;
      height: 200%;
      background: radial-gradient(circle, rgba(236, 72, 153, 0.2) 0%, transparent 70%);
      opacity: 0;
      transition: opacity 0.3s;
    }

    .goal-item:hover::before {
      opacity: 1;
    }

    .goal-item:hover {
      border-color: var(--accent);
      transform: translateY(-8px);
      box-shadow: 0 15px 35px rgba(236, 72, 153, 0.2);
    }

    .goal-icon {
      font-size: 28px;
      margin-bottom: 12px;
      animation: pulse 2s infinite;
    }

    @keyframes pulse {
      0%, 100% { transform: scale(1); }
      50% { transform: scale(1.1); }
    }

    .goal-item h4 {
      font-size: 15px;
      font-weight: 600;
      color: var(--accent);
      margin-bottom: 6px;
    }

    .goal-item p {
      font-size: 12px;
      color: var(--text-secondary);
    }

    /* CTA Section */
    .cta-section {
      text-align: center;
      padding: 60px 20px;
      background: linear-gradient(135deg, rgba(0, 212, 255, 0.05) 0%, rgba(139, 92, 246, 0.05) 100%);
      border-radius: 20px;
      border: 2px solid rgba(0, 212, 255, 0.1);
      margin-bottom: 40px;
      animation: slideInUp 0.8s ease-out;
    }

    .cta-section h2 {
      font-size: 28px;
      font-weight: 700;
      margin-bottom: 20px;
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
    }

    .cta-buttons {
      display: flex;
      gap: 12px;
      justify-content: center;
      flex-wrap: wrap;
      margin-top: 20px;
    }

    .cta-btn {
      padding: 14px 28px;
      border: 2px solid;
      border-radius: 50px;
      font-size: 14px;
      font-weight: 600;
      cursor: pointer;
      text-decoration: none;
      transition: all 0.3s ease;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      display: inline-flex;
      align-items: center;
      gap: 8px;
    }

    .cta-btn-primary {
      background: linear-gradient(135deg, var(--primary), var(--secondary));
      border-color: var(--primary);
      color: var(--dark);
    }

    .cta-btn-primary:hover {
      transform: translateY(-3px);
      box-shadow: 0 15px 35px rgba(0, 212, 255, 0.4);
    }

    .cta-btn-secondary {
      background: transparent;
      border-color: var(--accent);
      color: var(--accent);
    }

    .cta-btn-secondary:hover {
      background: rgba(236, 72, 153, 0.1);
      transform: translateY(-3px);
      box-shadow: 0 15px 35px rgba(236, 72, 153, 0.2);
    }

    /* Footer */
    .footer {
      text-align: center;
      padding: 40px 20px;
      border-top: 2px solid rgba(0, 212, 255, 0.1);
      color: var(--text-secondary);
      font-size: 13px;
      animation: fadeIn 1s ease-out 1s both;
    }

    @keyframes fadeIn {
      from { opacity: 0; }
      to { opacity: 1; }
    }

    .footer p {
      margin-bottom: 8px;
    }

    /* Responsive */
    @media (max-width: 768px) {
      .header h1 { font-size: 36px; }
      .header .tagline { font-size: 16px; }
      .section-title { font-size: 24px; }
      .projects-grid { grid-template-columns: 1fr; }
      .skills-grid { grid-template-columns: 1fr; }
      .goals-grid { grid-template-columns: repeat(2, 1fr); }
      .cta-buttons { flex-direction: column; }
      .cta-btn { width: 100%; justify-content: center; }
    }
  </style>
</head>
<body>
  <div class="bg-gradient"></div>

  <div class="content">
    <!-- Header -->
    <div class="header">
      <h1>Abdullah Tanveer</h1>
      <p class="tagline">Full Stack Developer • AI Engineer • SaaS Builder</p>
      <div class="badges-container">
        <div class="badge badge-1">MERN Stack</div>
        <div class="badge badge-2">AI Integration</div>
        <div class="badge badge-3">Flutter Dev</div>
      </div>
    </div>

    <div class="container">
      <!-- Featured Projects -->
      <h2 class="section-title">Featured Projects</h2>
      <div class="projects-grid">
        <div class="project-card">
          <div class="project-icon">🤖</div>
          <h3>StudyGenie AI</h3>
          <div class="role">AI • Education</div>
          <p>AI-powered study assistant enabling students to upload PDFs, chat with tutors, generate quizzes, and create personalized study plans.</p>
          <div class="tech-stack">
            <div class="tech-badge">Next.js</div>
            <div class="tech-badge">TypeScript</div>
            <div class="tech-badge">MongoDB</div>
            <div class="tech-badge">Groq API</div>
          </div>
        </div>

        <div class="project-card">
          <div class="project-icon">📊</div>
          <h3>Churn Prediction</h3>
          <div class="role">ML • Analytics</div>
          <p>Machine learning solution designed to predict customer churn, analyze retention patterns, and improve business decisions with AI insights.</p>
          <div class="tech-stack">
            <div class="tech-badge">Python</div>
            <div class="tech-badge">React</div>
            <div class="tech-badge">ML Models</div>
          </div>
        </div>

        <div class="project-card">
          <div class="project-icon">📱</div>
          <h3>Shamas Al Kananah</h3>
          <div class="role">Mobile • Commerce</div>
          <p>Premium e-commerce mobile app with real-time inventory, secure payments, and smooth checkout for hardware & electrical products.</p>
          <div class="tech-stack">
            <div class="tech-badge">Flutter</div>
            <div class="tech-badge">Firebase</div>
            <div class="tech-badge">Dart</div>
          </div>
        </div>

        <div class="project-card">
          <div class="project-icon">🚀</div>
          <h3>SaaS Vision 2026</h3>
          <div class="role">Innovation • Startup</div>
          <p>Building AI-driven SaaS products and intelligent automation systems. Target: Launch production SaaS products by end of 2026.</p>
          <div class="tech-stack">
            <div class="tech-badge">Full Stack</div>
            <div class="tech-badge">AI/ML</div>
            <div class="tech-badge">Scalable</div>
          </div>
        </div>
      </div>

      <!-- Technical Skills -->
      <h2 class="section-title">Technical Expertise</h2>
      <div class="skills-grid">
        <div class="skill-card">
          <div class="skill-icon">🎨</div>
          <h4>Frontend Development</h4>
          <p>React, Next.js, TypeScript, Tailwind CSS, HTML5, CSS3, JavaScript, Responsive Design</p>
        </div>
        <div class="skill-card">
          <div class="skill-icon">⚙️</div>
          <h4>Backend & Database</h4>
          <p>Node.js, Express, MongoDB, Firebase, PostgreSQL, RESTful APIs, GraphQL</p>
        </div>
        <div class="skill-card">
          <div class="skill-icon">📱</div>
          <h4>Mobile Development</h4>
          <p>Flutter, Dart, React Native, Cross-platform Development, Native Integration</p>
        </div>
        <div class="skill-card">
          <div class="skill-icon">🤖</div>
          <h4>AI & Machine Learning</h4>
          <p>Python, TensorFlow, PyTorch, Predictive Modeling, LLM Integration, ML Pipelines</p>
        </div>
        <div class="skill-card">
          <div class="skill-icon">🧰</div>
          <h4>Tools & Platforms</h4>
          <p>Git, GitHub, Docker, VS Code, Figma, Postman, AWS, Vercel, Firebase</p>
        </div>
        <div class="skill-card">
          <div class="skill-icon">🏗️</div>
          <h4>Architecture & Design</h4>
          <p>System Design, Scalable Architecture, SaaS Patterns, Clean Code, Best Practices</p>
        </div>
      </div>

      <!-- 2026 Goals -->
      <h2 class="section-title">2026 Objectives</h2>
      <div class="goals-grid">
        <div class="goal-item">
          <div class="goal-icon">🚀</div>
          <h4>Launch SaaS</h4>
          <p>Production-ready apps</p>
        </div>
        <div class="goal-item">
          <div class="goal-icon">🤖</div>
          <h4>AI Apps</h4>
          <p>Intelligent systems</p>
        </div>
        <div class="goal-item">
          <div class="goal-icon">💼</div>
          <h4>Top Tech Role</h4>
          <p>Career growth</p>
        </div>
        <div class="goal-item">
          <div class="goal-icon">🌍</div>
          <h4>Startup</h4>
          <p>Scale innovation</p>
        </div>
        <div class="goal-item">
          <div class="goal-icon">📱</div>
          <h4>Apps Published</h4>
          <p>App Store & Play</p>
        </div>
      </div>

      <!-- CTA Section -->
      <div class="cta-section">
        <h2>Let's Create Something Amazing</h2>
        <p style="color: var(--text-secondary); margin-bottom: 20px;">
          Open to collaborations on innovative projects, SaaS products, and AI-driven solutions.
        </p>
        <div class="cta-buttons">
          <a href="mailto:iamabdullahtanveer@gmail.com" class="cta-btn cta-btn-primary">✉️ Email Me</a>
          <a href="https://linkedin.com/in/abdullah-tanveer-570216338/" class="cta-btn cta-btn-secondary">💼 LinkedIn</a>
          <a href="https://github.com/abdullahtanveer" class="cta-btn cta-btn-secondary">🔗 GitHub</a>
        </div>
      </div>

      <!-- Footer -->
      <div class="footer">
        <p>© 2026 Abdullah Tanveer • Full Stack Developer & AI Engineer</p>
        <p>The best software is invisible — it simply works and improves lives.</p>
      </div>
    </div>
  </div>
</body>
</html>
