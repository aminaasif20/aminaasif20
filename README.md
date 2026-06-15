<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
  <title>Amina Asif · Software Developer</title>
  <!-- Font Awesome 6 for sharp icons -->
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    body {
      background: #f8fafc;
      font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, sans-serif;
      color: #0f172a;
      line-height: 1.5;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      min-height: 100vh;
      padding: 2rem 1.5rem;
    }

    /* professional card-based layout */
    .profile-card {
      max-width: 880px;
      width: 100%;
      background: #ffffff;
      border-radius: 2.5rem;
      box-shadow: 0 25px 50px -12px rgba(0, 0, 0, 0.08);
      padding: 2.5rem 2.2rem;
      transition: all 0.2s ease;
      border: 1px solid #f1f5f9;
    }

    /* header identity */
    .header-section {
      display: flex;
      flex-wrap: wrap;
      align-items: center;
      justify-content: space-between;
      margin-bottom: 2.2rem;
    }

    .name-title h1 {
      font-size: 2.8rem;
      font-weight: 700;
      letter-spacing: -0.5px;
      background: linear-gradient(135deg, #0f172a 0%, #334155 80%);
      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
      background-clip: text;
      margin-bottom: 0.2rem;
    }

    .badge-group {
      display: flex;
      flex-wrap: wrap;
      gap: 0.65rem;
      margin-top: 0.25rem;
    }

    .badge {
      background: #f1f5f9;
      color: #1e293b;
      padding: 0.4rem 1rem;
      border-radius: 2rem;
      font-size: 0.9rem;
      font-weight: 500;
      display: flex;
      align-items: center;
      gap: 0.4rem;
      letter-spacing: -0.2px;
      border: 1px solid #e2e8f0;
    }

    .badge i {
      font-size: 0.9rem;
      color: #2563eb;
    }

    .contact-links {
      display: flex;
      gap: 0.9rem;
      align-items: center;
    }

    .contact-links a {
      background: #ffffff;
      border: 1px solid #e2e8f0;
      width: 44px;
      height: 44px;
      display: flex;
      align-items: center;
      justify-content: center;
      border-radius: 14px;
      color: #1e293b;
      font-size: 1.3rem;
      transition: all 0.2s;
      box-shadow: 0 1px 3px rgba(0,0,0,0.02);
      text-decoration: none;
    }

    .contact-links a:hover {
      background: #0f172a;
      color: white;
      border-color: #0f172a;
      transform: translateY(-2px);
      box-shadow: 0 10px 15px -5px rgba(15, 23, 42, 0.2);
    }

    .email-link {
      background: #f8fafc;
      border-radius: 2rem;
      padding: 0.5rem 1.4rem;
      font-weight: 500;
      font-size: 0.95rem;
      color: #1e293b;
      text-decoration: none;
      display: flex;
      align-items: center;
      gap: 0.5rem;
      border: 1px solid #e2e8f0;
      transition: 0.2s;
      white-space: nowrap;
    }

    .email-link i {
      color: #2563eb;
    }

    .email-link:hover {
      background: #ffffff;
      border-color: #94a3b8;
    }

    /* philosophy line */
    .quote-line {
      background: #f1f5f9;
      border-radius: 1.5rem;
      padding: 1rem 1.5rem;
      margin: 1.8rem 0 2rem 0;
      border-left: 4px solid #2563eb;
      font-style: normal;
      font-weight: 500;
      color: #1e293b;
      display: flex;
      align-items: center;
      gap: 0.8rem;
      font-size: 1.05rem;
      background: linear-gradient(to right, #f8fafc, #ffffff);
    }

    .quote-line i {
      font-size: 1.5rem;
      color: #2563eb;
      opacity: 0.9;
    }

    /* section headings */
    .section-title {
      font-size: 1.1rem;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.5px;
      color: #475569;
      margin: 2rem 0 1.2rem 0;
      display: flex;
      align-items: center;
      gap: 0.6rem;
      border-bottom: 1px solid #e9eef3;
      padding-bottom: 0.65rem;
    }

    .section-title i {
      color: #2563eb;
      font-size: 1.2rem;
    }

    /* about text */
    .about-text {
      color: #334155;
      font-size: 1.05rem;
      margin-bottom: 0.5rem;
      line-height: 1.7;
    }

    .highlight-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 1.2rem;
      margin-top: 1rem;
    }

    .highlight-item {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      background: #f8fafc;
      padding: 0.3rem 1.1rem;
      border-radius: 2rem;
      font-size: 0.9rem;
      font-weight: 500;
      color: #1e293b;
      border: 1px solid #e9eef3;
    }

    .highlight-item i {
      color: #2563eb;
    }

    /* tech grid */
    .tech-grid {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      align-items: center;
    }

    .tech-item {
      background: white;
      border: 1px solid #e2e8f0;
      border-radius: 1.2rem;
      padding: 0.6rem 1.2rem;
      display: flex;
      align-items: center;
      gap: 0.6rem;
      font-weight: 500;
      color: #1e293b;
      transition: 0.2s;
      box-shadow: 0 2px 6px rgba(0,0,0,0.02);
    }

    .tech-item i, .tech-item img {
      font-size: 1.4rem;
      width: 24px;
      text-align: center;
      color: #2563eb;
    }

    .tech-item span {
      font-size: 0.95rem;
    }

    .tech-item:hover {
      border-color: #2563eb;
      background: #f8faff;
      transform: translateY(-1px);
    }

    /* custom icons using fontawesome for tech (mapped to similar) */
    .footer-motto {
      margin-top: 2.5rem;
      text-align: center;
      font-weight: 500;
      color: #475569;
      font-size: 0.95rem;
      letter-spacing: 0.3px;
      border-top: 1px solid #e9eef3;
      padding-top: 1.8rem;
      display: flex;
      align-items: center;
      justify-content: center;
      gap: 0.5rem;
    }

    .footer-motto i {
      color: #2563eb;
    }

    /* responsiveness */
    @media (max-width: 600px) {
      .profile-card {
        padding: 1.8rem 1.2rem;
      }
      .header-section {
        flex-direction: column;
        align-items: flex-start;
        gap: 1.2rem;
      }
      .name-title h1 {
        font-size: 2.2rem;
      }
      .contact-links {
        flex-wrap: wrap;
      }
    }
  </style>
</head>
<body>
  <div class="profile-card">
    
    <!-- Header with name, badges, and contact -->
    <div class="header-section">
      <div class="name-title">
        <h1>Amina Asif</h1>
        <div class="badge-group">
          <div class="badge"><i class="fas fa-code"></i> Software Developer</div>
          <div class="badge"><i class="fas fa-layer-group"></i> Full-Stack Enthusiast</div>
          <div class="badge"><i class="fas fa-bolt"></i> Quick Learner</div>
        </div>
      </div>
      <div class="contact-links">
        <a href="https://linkedin.com/in/by-amina-asif" target="_blank" aria-label="LinkedIn Profile" title="LinkedIn">
          <i class="fab fa-linkedin-in"></i>
        </a>
        <a href="https://kaggle.com/aminakagg1e" target="_blank" aria-label="Kaggle Profile" title="Kaggle">
          <i class="fab fa-kaggle"></i>
        </a>
        <a href="mailto:aminaasif245@gmail.com" class="email-link">
          <i class="far fa-envelope"></i> aminaasif245@gmail.com
        </a>
      </div>
    </div>

    <!-- Philosophy / quote -->
    <div class="quote-line">
      <i class="fas fa-quote-right"></i>
      <span>Execution is more powerful than intention.</span>
    </div>

    <!-- About section -->
    <div>
      <div class="section-title">
        <i class="fas fa-user-astronaut"></i> About Me
      </div>
      <p class="about-text">
        Passionate software developer from Pakistan with a strong drive to build impactful digital solutions. 
        I believe in learning by doing — whenever I grasp a new concept or envision an idea, I move quickly from thought to execution.
      </p>
      <div class="highlight-grid">
        <div class="highlight-item">
          <i class="fas fa-seedling"></i> Expanding expertise in full‑stack web & Flutter
        </div>
        <div class="highlight-item">
          <i class="fas fa-rocket"></i> Code. Build. Iterate. Improve.
        </div>
      </div>
    </div>

    <!-- Technologies & Tools -->
    <div>
      <div class="section-title">
        <i class="fas fa-toolbox"></i> Technologies & Tools
      </div>
      <div class="tech-grid">
        <!-- Android -->
        <div class="tech-item">
          <i class="fab fa-android"></i>
          <span>Android</span>
        </div>
        <!-- C++ -->
        <div class="tech-item">
          <i class="fas fa-code"></i>
          <span>C++</span>
        </div>
        <!-- C# -->
        <div class="tech-item">
          <i class="fas fa-hashtag"></i>
          <span>C#</span>
        </div>
        <!-- HTML5 -->
        <div class="tech-item">
          <i class="fab fa-html5"></i>
          <span>HTML5</span>
        </div>
        <!-- JavaScript -->
        <div class="tech-item">
          <i class="fab fa-js"></i>
          <span>JavaScript</span>
        </div>
        <!-- MySQL -->
        <div class="tech-item">
          <i class="fas fa-database"></i>
          <span>MySQL</span>
        </div>
        <!-- Node.js -->
        <div class="tech-item">
          <i class="fab fa-node-js"></i>
          <span>Node.js</span>
        </div>
        <!-- React -->
        <div class="tech-item">
          <i class="fab fa-react"></i>
          <span>React</span>
        </div>
        <!-- Additional Flutter (mentioned in about) -->
        <div class="tech-item">
          <i class="fas fa-mobile-alt"></i>
          <span>Flutter</span>
        </div>
      </div>
      <p style="margin-top: 0.8rem; font-size: 0.85rem; color: #64748b; display: flex; align-items: center; gap: 0.3rem;">
        <i class="fas fa-circle" style="font-size: 0.4rem; color: #2563eb;"></i> 
        Currently focusing on full‑stack development & Flutter
      </p>
    </div>

    <!-- Footer motto -->
    <div class="footer-motto">
      <i class="fas fa-terminal"></i> Code. Build. Iterate. Improve.
    </div>
  </div>
</body>
</html>
