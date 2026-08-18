<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    background: linear-gradient(135deg, #0f172a 0%, #1e293b 100%);
    color: #e2e8f0;
    line-height: 1.6;
    min-height: 100vh;
  }

  .container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
  }

  /* Header Section */
  .header {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    padding: 80px 20px;
    text-align: center;
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
    clip-path: polygon(0 0, 100% 0, 100% 85%, 0 100%);
  }

  .header h1 {
    font-size: 4rem;
    font-weight: 700;
    margin-bottom: 10px;
    text-shadow: 0 2px 10px rgba(0, 0, 0, 0.3);
  }

  .header p {
    font-size: 1.3rem;
    opacity: 0.95;
    font-weight: 300;
    letter-spacing: 1px;
  }

  .role-badge {
    display: inline-block;
    background: rgba(255, 255, 255, 0.15);
    border: 1px solid rgba(255, 255, 255, 0.3);
    padding: 12px 30px;
    border-radius: 50px;
    margin-top: 20px;
    font-size: 0.95rem;
    backdrop-filter: blur(10px);
    font-weight: 500;
  }

  /* Main Content */
  .content {
    padding: 60px 20px;
  }

  /* Sections */
  .section {
    margin-bottom: 80px;
  }

  .section-title {
    font-size: 2.2rem;
    font-weight: 700;
    margin-bottom: 40px;
    padding-bottom: 20px;
    border-bottom: 2px solid #667eea;
    position: relative;
    display: inline-block;
  }

  .section-title::after {
    content: '';
    position: absolute;
    bottom: -2px;
    left: 0;
    height: 2px;
    width: 100%;
    background: linear-gradient(90deg, #667eea, #764ba2, transparent);
  }

  /* About Section */
  .about-content {
    background: rgba(30, 41, 59, 0.8);
    border-left: 4px solid #667eea;
    padding: 40px;
    border-radius: 8px;
    backdrop-filter: blur(10px);
    border: 1px solid rgba(255, 255, 255, 0.1);
  }

  .about-content h3 {
    font-size: 1.3rem;
    margin-top: 20px;
    margin-bottom: 12px;
    color: #667eea;
    font-weight: 600;
  }

  .about-content p {
    font-size: 1.05rem;
    line-height: 1.8;
    color: #cbd5e1;
    margin-bottom: 15px;
  }

  /* Tech Stack */
  .tech-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 40px;
    margin-top: 30px;
  }

  .tech-category {
    background: rgba(30, 41, 59, 0.8);
    border-radius: 8px;
    padding: 30px;
    border: 1px solid rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
    transition: all 0.3s ease;
  }

  .tech-category:hover {
    border-color: #667eea;
    box-shadow: 0 8px 32px rgba(102, 126, 234, 0.15);
    transform: translateY(-5px);
  }

  .tech-category h4 {
    font-size: 1.2rem;
    color: #667eea;
    margin-bottom: 20px;
    font-weight: 600;
  }

  .tech-list {
    display: flex;
    flex-wrap: wrap;
    gap: 12px;
  }

  .tech-badge {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    padding: 8px 16px;
    border-radius: 20px;
    font-size: 0.9rem;
    font-weight: 500;
    border: 1px solid rgba(255, 255, 255, 0.2);
  }

  /* Projects Section */
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
    gap: 30px;
    margin-top: 30px;
  }

  .project-card {
    background: rgba(30, 41, 59, 0.8);
    border-radius: 8px;
    padding: 30px;
    border: 1px solid rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
  }

  .project-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 4px;
    background: linear-gradient(90deg, #667eea, #764ba2);
  }

  .project-card:hover {
    border-color: #667eea;
    box-shadow: 0 12px 40px rgba(102, 126, 234, 0.2);
    transform: translateY(-8px);
  }

  .project-title {
    font-size: 1.3rem;
    font-weight: 700;
    margin-bottom: 12px;
    color: #f1f5f9;
  }

  .project-description {
    color: #cbd5e1;
    margin-bottom: 18px;
    font-size: 0.95rem;
    line-height: 1.6;
  }

  .project-tech {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
    margin-bottom: 18px;
  }

  .tech-tag {
    background: rgba(102, 126, 234, 0.15);
    color: #a5b4fc;
    padding: 6px 12px;
    border-radius: 4px;
    font-size: 0.85rem;
    border: 1px solid rgba(102, 126, 234, 0.3);
  }

  .project-link {
    display: inline-block;
    color: #667eea;
    text-decoration: none;
    font-weight: 600;
    font-size: 0.95rem;
    transition: all 0.3s ease;
    padding-bottom: 2px;
    border-bottom: 2px solid transparent;
  }

  .project-link:hover {
    color: #764ba2;
    border-bottom-color: #764ba2;
  }

  /* Skills Section */
  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 25px;
    margin-top: 30px;
  }

  .skill-item {
    background: rgba(30, 41, 59, 0.8);
    padding: 25px;
    border-radius: 8px;
    border: 1px solid rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
  }

  .skill-item h4 {
    color: #667eea;
    font-size: 1.1rem;
    margin-bottom: 15px;
    font-weight: 600;
  }

  .skill-item p {
    color: #cbd5e1;
    font-size: 0.95rem;
    line-height: 1.6;
  }

  /* Stats Section */
  .stats-container {
    background: rgba(30, 41, 59, 0.8);
    border-radius: 8px;
    padding: 40px;
    border: 1px solid rgba(255, 255, 255, 0.1);
    backdrop-filter: blur(10px);
    margin-top: 30px;
  }

  .stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 25px;
    text-align: center;
  }

  .stat-item {
    padding: 20px;
  }

  .stat-number {
    font-size: 2.5rem;
    font-weight: 700;
    color: #667eea;
    margin-bottom: 8px;
  }

  .stat-label {
    color: #cbd5e1;
    font-size: 0.95rem;
  }

  /* Contact Section */
  .contact-container {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    border-radius: 8px;
    padding: 50px;
    text-align: center;
    margin-top: 30px;
  }

  .contact-title {
    font-size: 2rem;
    font-weight: 700;
    margin-bottom: 30px;
  }

  .contact-links {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 20px;
    margin-bottom: 30px;
  }

  .contact-btn {
    background: rgba(255, 255, 255, 0.2);
    border: 1px solid rgba(255, 255, 255, 0.3);
    color: white;
    padding: 12px 30px;
    border-radius: 4px;
    text-decoration: none;
    font-weight: 600;
    transition: all 0.3s ease;
    backdrop-filter: blur(10px);
  }

  .contact-btn:hover {
    background: rgba(255, 255, 255, 0.3);
    border-color: rgba(255, 255, 255, 0.5);
  }

  .opportunities {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 15px;
    margin-top: 20px;
    justify-content: center;
  }

  .opp-item {
    background: rgba(255, 255, 255, 0.1);
    padding: 15px;
    border-radius: 4px;
    border: 1px solid rgba(255, 255, 255, 0.2);
    font-weight: 500;
  }

  /* Footer */
  .footer {
    text-align: center;
    padding: 40px 20px;
    border-top: 1px solid rgba(255, 255, 255, 0.1);
    color: #94a3b8;
    font-size: 0.95rem;
  }

  /* Responsive */
  @media (max-width: 768px) {
    .header h1 {
      font-size: 2.5rem;
    }

    .header p {
      font-size: 1.1rem;
    }

    .section-title {
      font-size: 1.8rem;
    }

    .projects-grid {
      grid-template-columns: 1fr;
    }

    .tech-grid {
      grid-template-columns: 1fr;
    }
  }

  /* Animations */
  @keyframes slideUp {
    from {
      opacity: 0;
      transform: translateY(20px);
    }
    to {
      opacity: 1;
      transform: translateY(0);
    }
  }

  .section {
    animation: slideUp 0.6s ease-out;
  }
</style>
</head>
<body>

<!-- Header -->
<div class="header">
  <div class="container">
    <h1>Noidea1001</h1>
    <p>Full-Stack Developer & Backend Specialist</p>
    <div class="role-badge">Building Production-Grade Enterprise Solutions</div>
  </div>
</div>

<!-- Main Content -->
<div class="container">
  <div class="content">

    <!-- About Section -->
    <div class="section">
      <h2 class="section-title">About</h2>
      <div class="about-content">
        <p>I am a full-stack developer with deep expertise in building scalable, production-grade applications. My focus is on clean architecture, database optimization, and enterprise-level system design. I specialize in backend development with a strong foundation in RESTful APIs and microservices architecture.</p>
        
        <h3>Current Focus</h3>
        <p>Enterprise applications, system architecture, and production-ready solutions</p>
        
        <h3>Specialization</h3>
        <p>API Design | Database Architecture | System Design | Backend Development</p>
        
        <h3>Philosophy</h3>
        <p>Write code that solves problems elegantly, scales effortlessly, and maintains clarity throughout the codebase.</p>
      </div>
    </div>

    <!-- Technology Stack -->
    <div class="section">
      <h2 class="section-title">Technology Stack</h2>
      <div class="tech-grid">
        <div class="tech-category">
          <h4>Languages</h4>
          <div class="tech-list">
            <span class="tech-badge">Python</span>
            <span class="tech-badge">C#</span>
            <span class="tech-badge">JavaScript</span>
            <span class="tech-badge">HTML5</span>
            <span class="tech-badge">CSS3</span>
          </div>
        </div>

        <div class="tech-category">
          <h4>Backend & Frameworks</h4>
          <div class="tech-list">
            <span class="tech-badge">.NET Core</span>
            <span class="tech-badge">ASP.NET</span>
            <span class="tech-badge">Django</span>
            <span class="tech-badge">Flask</span>
            <span class="tech-badge">REST APIs</span>
          </div>
        </div>

        <div class="tech-category">
          <h4>Databases & Tools</h4>
          <div class="tech-list">
            <span class="tech-badge">PostgreSQL</span>
            <span class="tech-badge">SQL Server</span>
            <span class="tech-badge">SQLite</span>
            <span class="tech-badge">Git</span>
            <span class="tech-badge">GitHub</span>
          </div>
        </div>
      </div>
    </div>

    <!-- Featured Projects -->
    <div class="section">
      <h2 class="section-title">Featured Projects</h2>
      <div class="projects-grid">
        
        <div class="project-card">
          <div class="project-title">Bank Account API</div>
          <div class="project-description">Secure banking system with comprehensive transaction processing and account management. Implements robust security protocols and RESTful architecture.</div>
          <div class="project-tech">
            <span class="tech-tag">Python</span>
            <span class="tech-tag">REST API</span>
            <span class="tech-tag">Database Design</span>
          </div>
          <a href="https://github.com/Noidea1001/Bank_account_api" class="project-link">View Repository →</a>
        </div>

        <div class="project-card">
          <div class="project-title">Travel Booking System</div>
          <div class="project-description">Full-featured travel platform with flight and hotel booking, itinerary management, and payment processing. Enterprise-level database architecture.</div>
          <div class="project-tech">
            <span class="tech-tag">Python</span>
            <span class="tech-tag">Database Architecture</span>
            <span class="tech-tag">APIs</span>
          </div>
          <a href="https://github.com/Noidea1001/Travel-booking-system" class="project-link">View Repository →</a>
        </div>

        <div class="project-card">
          <div class="project-title">University Management System</div>
          <div class="project-description">Enterprise-level system with Entity Framework Core. Manages student enrollment, courses, grades, and comprehensive reporting. Production-ready architecture.</div>
          <div class="project-tech">
            <span class="tech-tag">C#</span>
            <span class="tech-tag">.NET Core</span>
            <span class="tech-tag">Entity Framework</span>
          </div>
          <a href="https://github.com/Noidea1001/University-managment-EF-core" class="project-link">View Repository →</a>
        </div>

        <div class="project-card">
          <div class="project-title">Online Learning System</div>
          <div class="project-description">Django-powered e-learning platform with multilingual support, course management, and progress tracking. Scalable architecture with PostgreSQL backend.</div>
          <div class="project-tech">
            <span class="tech-tag">Django</span>
            <span class="tech-tag">PostgreSQL</span>
            <span class="tech-tag">Frontend</span>
          </div>
          <a href="https://github.com/Noidea1001/Online-learning-system" class="project-link">View Repository →</a>
        </div>

        <div class="project-card">
          <div class="project-title">Library Management System</div>
          <div class="project-description">Complete inventory management solution with member tracking and automated checkout system. Implements advanced database queries and business logic.</div>
          <div class="project-tech">
            <span class="tech-tag">HTML5</span>
            <span class="tech-tag">CSS3</span>
            <span class="tech-tag">Database</span>
          </div>
          <a href="https://github.com/Noidea1001/Library-System" class="project-link">View Repository →</a>
        </div>

        <div class="project-card">
          <div class="project-title">POS System</div>
          <div class="project-description">Professional point-of-sale interface for retail operations with transaction management, inventory tracking, and comprehensive reporting analytics.</div>
          <div class="project-tech">
            <span class="tech-tag">HTML5</span>
            <span class="tech-tag">CSS3</span>
            <span class="tech-tag">JavaScript</span>
          </div>
          <a href="https://github.com/Noidea1001/pos" class="project-link">View Repository →</a>
        </div>

        <div class="project-card">
          <div class="project-title">Student Attendance System</div>
          <div class="project-description">Automated attendance tracking with comprehensive report generation and advanced analytics. Demonstrates strong database architecture and backend development.</div>
          <div class="project-tech">
            <span class="tech-tag">Database Architecture</span>
            <span class="tech-tag">Python</span>
            <span class="tech-tag">Backend</span>
          </div>
          <a href="https://github.com/Noidea1001/Student-Attendance-Management-System" class="project-link">View Repository →</a>
        </div>

        <div class="project-card">
          <div class="project-title">Weather Application</div>
          <div class="project-description">Real-time weather application with location-based forecasts, interactive UI, and data visualization. Demonstrates frontend development expertise.</div>
          <div class="project-tech">
            <span class="tech-tag">Frontend</span>
            <span class="tech-tag">APIs</span>
            <span class="tech-tag">JavaScript</span>
          </div>
          <a href="https://github.com/Noidea1001/project-weather" class="project-link">View Repository →</a>
        </div>

      </div>
    </div>

    <!-- Core Competencies -->
    <div class="section">
      <h2 class="section-title">Core Competencies</h2>
      <div class="skills-grid">
        <div class="skill-item">
          <h4>Backend Architecture</h4>
          <p>RESTful APIs, SOLID Principles, Design Patterns, Microservices, Clean Code Architecture, API Gateway Patterns</p>
        </div>

        <div class="skill-item">
          <h4>Database Design</h4>
          <p>Normalization, Query Optimization, Entity Relationships, Schema Design, Performance Tuning, SQL Expertise</p>
        </div>

        <div class="skill-item">
          <h4>Backend Frameworks</h4>
          <p>ASP.NET Core, Entity Framework Core, Django, Flask, Express.js, API Development, Async Programming</p>
        </div>

        <div class="skill-item">
          <h4>Frontend Technologies</h4>
          <p>HTML5, CSS3, JavaScript, Bootstrap, Responsive Design, UI/UX Principles, Modern Web Standards</p>
        </div>

        <div class="skill-item">
          <h4>Development Practices</h4>
          <p>Git Workflow, Problem Solving, Code Reviews, Testing, Agile Methodology, Version Control, CI/CD</p>
        </div>

        <div class="skill-item">
          <h4>System Design</h4>
          <p>Scalability Planning, Performance Optimization, Security Implementation, Best Practices, Architecture Patterns</p>
        </div>
      </div>
    </div>

    <!-- Key Highlights -->
    <div class="section">
      <h2 class="section-title">Key Highlights</h2>
      <div class="stats-container">
        <div class="stats-grid">
          <div class="stat-item">
            <div class="stat-number">14+</div>
            <div class="stat-label">Projects Delivered</div>
          </div>
          <div class="stat-item">
            <div class="stat-number">5+</div>
            <div class="stat-label">Tech Stacks</div>
          </div>
          <div class="stat-item">
            <div class="stat-number">100%</div>
            <div class="stat-label">Code Quality Focus</div>
          </div>
          <div class="stat-item">
            <div class="stat-number">∞</div>
            <div class="stat-label">Learning Mindset</div>
          </div>
        </div>
      </div>
    </div>

    <!-- Current Work -->
    <div class="section">
      <h2 class="section-title">Currently Working On</h2>
      <div class="skills-grid">
        <div class="skill-item">
          <h4>Advanced API Architecture</h4>
          <p>Implementing microservices patterns and distributed system architectures for enhanced scalability and maintainability.</p>
        </div>

        <div class="skill-item">
          <h4>System Design Mastery</h4>
          <p>Deep diving into scalable architecture principles, design patterns, and enterprise-level best practices.</p>
        </div>

        <div class="skill-item">
          <h4>Enterprise Solutions</h4>
          <p>Building production-grade systems with robust architecture, security, and performance optimization.</p>
        </div>

        <div class="skill-item">
          <h4>Code Excellence</h4>
          <p>Continuous improvement through systematic refactoring and implementation of advanced coding patterns.</p>
        </div>

        <div class="skill-item">
          <h4>Performance Optimization</h4>
          <p>Database query optimization, caching strategies, and algorithmic efficiency improvements.</p>
        </div>

        <div class="skill-item">
          <h4>Full-Stack Integration</h4>
          <p>Seamless integration of frontend and backend systems with modern development practices.</p>
        </div>
      </div>
    </div>

    <!-- Contact Section -->
    <div class="section">
      <div class="contact-container">
        <div class="contact-title">Let's Work Together</div>
        <div class="contact-links">
          <a href="https://github.com/Noidea1001" class="contact-btn">GitHub Profile</a>
          <a href="mailto:your.email@example.com" class="contact-btn">Send Email</a>
          <a href="https://linkedin.com/in/your-profile" class="contact-btn">LinkedIn</a>
          <a href="https://yourportfolio.com" class="contact-btn">Portfolio</a>
        </div>
        
        <div style="margin-top: 40px;">
          <h3 style="font-size: 1.2rem; margin-bottom: 20px; font-weight: 600;">I'm Open To</h3>
          <div class="opportunities">
            <div class="opp-item">Full-Time Positions</div>
            <div class="opp-item">Contract Work</div>
            <div class="opp-item">Technical Collaborations</div>
            <div class="opp-item">Open Source Projects</div>
          </div>
        </div>
      </div>
    </div>

  </div>
</div>

<!-- Footer -->
<div class="footer">
  <p>Crafted with precision and attention to detail. Last updated August 2026.</p>
  <p style="margin-top: 10px;">Visit my GitHub repositories for complete project details and code samples.</p>
</div>

</body>
</html>