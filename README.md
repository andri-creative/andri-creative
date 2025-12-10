### 👋 Hi there, I'm Andri Anto!

<style>
  /* ===== CSS VARIABLES & THEME ===== */
  :root {
    /* Color Palette */
    --primary: #fb4362;
    --primary-dark: #d32f4e;
    --primary-light: #ff7b93;
    --secondary: #2d3748;
    --secondary-light: #4a5568;
    --accent: #4299e1;
    --accent-dark: #2b6cb0;
    --success: #48bb78;
    --warning: #ed8936;
    --danger: #f56565;
    
    /* Background Colors */
    --bg-primary: #ffffff;
    --bg-secondary: #f7fafc;
    --bg-tertiary: #edf2f7;
    --bg-dark: #1a202c;
    
    /* Text Colors */
    --text-primary: #2d3748;
    --text-secondary: #4a5568;
    --text-light: #718096;
    --text-inverse: #ffffff;
    
    /* Borders & Shadows */
    --border-radius: 12px;
    --border-radius-sm: 8px;
    --border-color: #e2e8f0;
    --shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.12);
    --shadow-md: 0 4px 6px rgba(0, 0, 0, 0.1);
    --shadow-lg: 0 10px 15px rgba(0, 0, 0, 0.1);
    --shadow-xl: 0 20px 25px rgba(0, 0, 0, 0.15);
    
    /* Spacing */
    --spacing-xs: 0.25rem;
    --spacing-sm: 0.5rem;
    --spacing-md: 1rem;
    --spacing-lg: 1.5rem;
    --spacing-xl: 2rem;
    --spacing-2xl: 3rem;
    
    /* Transitions */
    --transition-fast: 150ms ease-in-out;
    --transition-normal: 300ms ease-in-out;
    --transition-slow: 500ms ease-in-out;
    
    /* Typography */
    --font-sans: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue', sans-serif;
    --font-mono: 'SFMono-Regular', 'Consolas', 'Liberation Mono', 'Menlo', monospace;
    --font-heading: var(--font-sans);
    --font-body: var(--font-sans);
  }

  /* Dark Mode Support */
  @media (prefers-color-scheme: dark) {
    :root {
      --bg-primary: #1a202c;
      --bg-secondary: #2d3748;
      --bg-tertiary: #4a5568;
      --text-primary: #f7fafc;
      --text-secondary: #e2e8f0;
      --text-light: #a0aec0;
      --border-color: #4a5568;
      --shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.5);
      --shadow-md: 0 4px 6px rgba(0, 0, 0, 0.4);
      --shadow-lg: 0 10px 15px rgba(0, 0, 0, 0.4);
    }
  }

  /* ===== RESET & BASE STYLES ===== */
  .readme-container {
    font-family: var(--font-body);
    line-height: 1.7;
    color: var(--text-primary);
    background: var(--bg-primary);
    max-width: 900px;
    margin: 0 auto;
    padding: var(--spacing-xl);
    box-sizing: border-box;
  }

  .readme-container * {
    box-sizing: border-box;
  }

  .readme-container h1,
  .readme-container h2,
  .readme-container h3,
  .readme-container h4 {
    font-family: var(--font-heading);
    font-weight: 700;
    line-height: 1.3;
    margin-top: 0;
    color: var(--text-primary);
  }

  .readme-container h1 {
    font-size: 2.5rem;
    margin-bottom: var(--spacing-lg);
    background: linear-gradient(135deg, var(--primary), var(--accent));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .readme-container h2 {
    font-size: 1.8rem;
    margin-bottom: var(--spacing-md);
    padding-bottom: var(--spacing-xs);
    border-bottom: 3px solid var(--primary);
    display: inline-block;
  }

  .readme-container h3 {
    font-size: 1.4rem;
    margin-bottom: var(--spacing-md);
    display: flex;
    align-items: center;
    gap: var(--spacing-sm);
  }

  .readme-container h3 img {
    width: 24px;
    height: 24px;
  }

  .readme-container p {
    margin-bottom: var(--spacing-md);
    color: var(--text-secondary);
  }

  .readme-container a {
    color: var(--accent);
    text-decoration: none;
    transition: color var(--transition-fast);
    border-bottom: 1px dashed transparent;
  }

  .readme-container a:hover {
    color: var(--accent-dark);
    border-bottom-color: var(--accent);
  }

  .readme-container ul,
  .readme-container ol {
    padding-left: var(--spacing-xl);
    margin-bottom: var(--spacing-lg);
  }

  .readme-container li {
    margin-bottom: var(--spacing-sm);
    color: var(--text-secondary);
  }

  /* ===== HEADER SECTION ===== */
  .readme-header {
    text-align: center;
    padding: var(--spacing-2xl) 0;
    margin-bottom: var(--spacing-2xl);
    position: relative;
    overflow: hidden;
  }

  .readme-header::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    height: 4px;
    background: linear-gradient(90deg, var(--primary), var(--accent), var(--success));
    z-index: 1;
  }

  .readme-header::after {
    content: '';
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    width: 300px;
    height: 300px;
    background: radial-gradient(circle, var(--primary-light) 0%, transparent 70%);
    opacity: 0.1;
    z-index: 0;
  }

  .profile-gif {
    width: 120px;
    height: 120px;
    border-radius: 50%;
    border: 4px solid var(--primary);
    padding: 4px;
    background: var(--bg-primary);
    box-shadow: var(--shadow-lg);
    position: relative;
    z-index: 2;
    transition: transform var(--transition-normal), box-shadow var(--transition-normal);
    margin: var(--spacing-lg) auto;
  }

  .profile-gif:hover {
    transform: scale(1.05);
    box-shadow: var(--shadow-xl);
  }

  .view-counter {
    display: inline-flex;
    align-items: center;
    gap: var(--spacing-sm);
    background: var(--bg-secondary);
    padding: var(--spacing-sm) var(--spacing-md);
    border-radius: var(--border-radius-sm);
    font-size: 0.9rem;
    color: var(--text-light);
    margin: var(--spacing-md) 0;
  }

  /* ===== ABOUT SECTION ===== */
  .about-section {
    background: var(--bg-secondary);
    padding: var(--spacing-xl);
    border-radius: var(--border-radius);
    margin-bottom: var(--spacing-2xl);
    box-shadow: var(--shadow-md);
    border-left: 6px solid var(--primary);
    position: relative;
    overflow: hidden;
  }

  .about-section::after {
    content: '💻';
    position: absolute;
    top: -20px;
    right: -20px;
    font-size: 8rem;
    opacity: 0.05;
    transform: rotate(15deg);
    pointer-events: none;
  }

  .about-points {
    list-style: none;
    padding-left: 0;
    margin: var(--spacing-lg) 0;
  }

  .about-points li {
    position: relative;
    padding-left: var(--spacing-xl);
    margin-bottom: var(--spacing-md);
  }

  .about-points li::before {
    content: '→';
    position: absolute;
    left: 0;
    color: var(--primary);
    font-weight: bold;
  }

  .social-links {
    display: flex;
    gap: var(--spacing-md);
    flex-wrap: wrap;
    margin-top: var(--spacing-xl);
  }

  .social-link {
    display: inline-flex;
    align-items: center;
    gap: var(--spacing-sm);
    padding: var(--spacing-sm) var(--spacing-md);
    background: linear-gradient(135deg, var(--primary), var(--primary-dark));
    color: var(--text-inverse);
    border-radius: var(--border-radius-sm);
    font-weight: 500;
    transition: all var(--transition-normal);
    box-shadow: var(--shadow-sm);
  }

  .social-link:hover {
    transform: translateY(-2px);
    box-shadow: var(--shadow-md);
    color: var(--text-inverse);
    background: linear-gradient(135deg, var(--primary-dark), var(--primary));
  }

  /* ===== SKILLS SECTION ===== */
  .skills-section {
    margin: var(--spacing-2xl) 0;
  }

  .skills-categories {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: var(--spacing-xl);
    margin-top: var(--spacing-xl);
  }

  .skills-category {
    background: var(--bg-primary);
    padding: var(--spacing-xl);
    border-radius: var(--border-radius);
    box-shadow: var(--shadow-md);
    border: 1px solid var(--border-color);
    transition: transform var(--transition-normal), box-shadow var(--transition-normal);
  }

  .skills-category:hover {
    transform: translateY(-4px);
    box-shadow: var(--shadow-lg);
  }

  .skills-category h4 {
    font-size: 1.2rem;
    margin-bottom: var(--spacing-lg);
    color: var(--secondary);
    display: flex;
    align-items: center;
    gap: var(--spacing-sm);
  }

  .skills-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(80px, 1fr));
    gap: var(--spacing-md);
  }

  .skill-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    padding: var(--spacing-md);
    background: var(--bg-secondary);
    border-radius: var(--border-radius-sm);
    transition: all var(--transition-fast);
    text-align: center;
    position: relative;
  }

  .skill-item:hover {
    background: var(--bg-tertiary);
    transform: scale(1.05);
  }

  .skill-item::after {
    content: attr(title);
    position: absolute;
    bottom: -30px;
    left: 50%;
    transform: translateX(-50%);
    background: var(--secondary);
    color: var(--text-inverse);
    padding: var(--spacing-xs) var(--spacing-sm);
    border-radius: 4px;
    font-size: 0.75rem;
    opacity: 0;
    transition: opacity var(--transition-fast);
    white-space: nowrap;
    z-index: 10;
  }

  .skill-item:hover::after {
    opacity: 1;
  }

  .skill-icon {
    width: 40px;
    height: 40px;
    margin-bottom: var(--spacing-sm);
  }

  .skill-name {
    font-size: 0.8rem;
    color: var(--text-light);
    margin-top: var(--spacing-xs);
  }

  /* ===== STATS SECTION ===== */
  .stats-section {
    margin: var(--spacing-2xl) 0;
  }

  .stats-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: var(--spacing-xl);
    margin-top: var(--spacing-xl);
  }

  .stat-card {
    background: linear-gradient(135deg, var(--bg-secondary), var(--bg-primary));
    padding: var(--spacing-xl);
    border-radius: var(--border-radius);
    box-shadow: var(--shadow-md);
    text-align: center;
    border: 1px solid var(--border-color);
    transition: all var(--transition-normal);
    position: relative;
    overflow: hidden;
  }

  .stat-card:hover {
    transform: translateY(-4px);
    box-shadow: var(--shadow-lg);
  }

  .stat-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 4px;
    background: linear-gradient(90deg, var(--primary), var(--accent));
  }

  .stat-title {
    font-size: 0.9rem;
    color: var(--text-light);
    text-transform: uppercase;
    letter-spacing: 1px;
    margin-bottom: var(--spacing-md);
  }

  .stat-content {
    font-size: 1.5rem;
    font-weight: 700;
    color: var(--text-primary);
    margin-bottom: var(--spacing-sm);
  }

  /* ===== SUPPORT SECTION ===== */
  .support-section {
    background: linear-gradient(135deg, var(--primary), var(--accent));
    padding: var(--spacing-2xl);
    border-radius: var(--border-radius);
    margin: var(--spacing-2xl) 0;
    text-align: center;
    color: var(--text-inverse);
    position: relative;
    overflow: hidden;
  }

  .support-section::before {
    content: '';
    position: absolute;
    top: -50%;
    left: -50%;
    width: 200%;
    height: 200%;
    background: radial-gradient(circle, rgba(255,255,255,0.1) 1px, transparent 1px);
    background-size: 20px 20px;
    animation: float 20s linear infinite;
    z-index: 0;
  }

  @keyframes float {
    0% { transform: rotate(0deg); }
    100% { transform: rotate(360deg); }
  }

  .support-content {
    position: relative;
    z-index: 1;
  }

  .support-title {
    font-size: 1.8rem;
    margin-bottom: var(--spacing-md);
    color: var(--text-inverse);
  }

  .support-subtitle {
    font-size: 1rem;
    opacity: 0.9;
    margin-bottom: var(--spacing-xl);
  }

  .support-buttons {
    display: flex;
    justify-content: center;
    gap: var(--spacing-md);
    flex-wrap: wrap;
  }

  .support-button {
    display: inline-flex;
    align-items: center;
    gap: var(--spacing-sm);
    padding: var(--spacing-md) var(--spacing-xl);
    background: rgba(255, 255, 255, 0.15);
    color: var(--text-inverse);
    border: 2px solid rgba(255, 255, 255, 0.3);
    border-radius: var(--border-radius-sm);
    font-weight: 600;
    transition: all var(--transition-normal);
    backdrop-filter: blur(10px);
  }

  .support-button:hover {
    background: rgba(255, 255, 255, 0.25);
    transform: translateY(-3px);
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
  }

  /* ===== BLOG SECTION ===== */
  .blog-section {
    background: var(--bg-secondary);
    padding: var(--spacing-xl);
    border-radius: var(--border-radius);
    margin: var(--spacing-2xl) 0;
  }

  .blog-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: var(--spacing-lg);
    margin-top: var(--spacing-lg);
  }

  .blog-card {
    background: var(--bg-primary);
    border-radius: var(--border-radius-sm);
    overflow: hidden;
    box-shadow: var(--shadow-md);
    transition: all var(--transition-normal);
    border: 1px solid var(--border-color);
  }

  .blog-card:hover {
    transform: translateY(-4px);
    box-shadow: var(--shadow-lg);
  }

  .blog-image {
    height: 160px;
    background: linear-gradient(135deg, var(--primary-light), var(--accent));
    display: flex;
    align-items: center;
    justify-content: center;
    color: var(--text-inverse);
    font-size: 2rem;
  }

  .blog-content {
    padding: var(--spacing-lg);
  }

  .blog-title {
    font-size: 1.1rem;
    margin-bottom: var(--spacing-sm);
    color: var(--text-primary);
  }

  .blog-excerpt {
    font-size: 0.9rem;
    color: var(--text-light);
    margin-bottom: var(--spacing-md);
  }

  .blog-meta {
    display: flex;
    justify-content: space-between;
    font-size: 0.8rem;
    color: var(--text-light);
  }

  /* ===== ACTIVITY GRAPH ===== */
  .activity-section {
    margin: var(--spacing-2xl) 0;
  }

  .activity-graph {
    background: var(--bg-primary);
    padding: var(--spacing-xl);
    border-radius: var(--border-radius);
    box-shadow: var(--shadow-md);
    border: 1px solid var(--border-color);
  }

  /* ===== FOOTER ===== */
  .readme-footer {
    text-align: center;
    padding: var(--spacing-xl) 0;
    margin-top: var(--spacing-2xl);
    border-top: 1px solid var(--border-color);
    color: var(--text-light);
    font-size: 0.9rem;
  }

  .footer-links {
    display: flex;
    justify-content: center;
    gap: var(--spacing-lg);
    margin-top: var(--spacing-md);
    flex-wrap: wrap;
  }

  /* ===== ANIMATIONS ===== */
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

  @keyframes pulse {
    0%, 100% { opacity: 1; }
    50% { opacity: 0.7; }
  }

  @keyframes slideIn {
    from {
      transform: translateX(-20px);
      opacity: 0;
    }
    to {
      transform: translateX(0);
      opacity: 1;
    }
  }

  .animate-fade-in {
    animation: fadeInUp 0.6s ease-out;
  }

  .animate-pulse {
    animation: pulse 2s infinite;
  }

  .animate-slide-in {
    animation: slideIn 0.5s ease-out;
  }

  /* ===== RESPONSIVE DESIGN ===== */
  @media (max-width: 768px) {
    .readme-container {
      padding: var(--spacing-md);
    }
    
    .readme-container h1 {
      font-size: 2rem;
    }
    
    .readme-container h2 {
      font-size: 1.5rem;
    }
    
    .readme-container h3 {
      font-size: 1.2rem;
    }
    
    .skills-categories {
      grid-template-columns: 1fr;
    }
    
    .skills-grid {
      grid-template-columns: repeat(auto-fill, minmax(70px, 1fr));
    }
    
    .stats-grid {
      grid-template-columns: 1fr;
    }
    
    .support-section {
      padding: var(--spacing-xl);
    }
    
    .support-buttons {
      flex-direction: column;
      align-items: center;
    }
    
    .blog-grid {
      grid-template-columns: 1fr;
    }
    
    .social-links {
      flex-direction: column;
    }
  }

  @media (max-width: 480px) {
    .readme-header {
      padding: var(--spacing-xl) 0;
    }
    
    .profile-gif {
      width: 100px;
      height: 100px;
    }
    
    .about-section,
    .skills-category,
    .stat-card,
    .blog-card {
      padding: var(--spacing-lg);
    }
    
    .skills-grid {
      grid-template-columns: repeat(3, 1fr);
    }
    
    .footer-links {
      flex-direction: column;
      gap: var(--spacing-sm);
    }
  }

  /* ===== UTILITY CLASSES ===== */
  .text-center {
    text-align: center;
  }

  .text-gradient {
    background: linear-gradient(135deg, var(--primary), var(--accent));
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
  }

  .badge {
    display: inline-block;
    padding: var(--spacing-xs) var(--spacing-sm);
    background: var(--bg-tertiary);
    color: var(--text-secondary);
    border-radius: var(--border-radius-sm);
    font-size: 0.8rem;
    font-weight: 500;
    margin-right: var(--spacing-xs);
    margin-bottom: var(--spacing-xs);
  }

  .badge-primary {
    background: linear-gradient(135deg, var(--primary), var(--primary-dark));
    color: var(--text-inverse);
  }

  .badge-secondary {
    background: var(--accent);
    color: var(--text-inverse);
  }

  .badge-success {
    background: var(--success);
    color: var(--text-inverse);
  }

  .card {
    background: var(--bg-primary);
    border-radius: var(--border-radius);
    padding: var(--spacing-xl);
    box-shadow: var(--shadow-md);
    border: 1px solid var(--border-color);
    transition: all var(--transition-normal);
  }

  .card:hover {
    transform: translateY(-2px);
    box-shadow: var(--shadow-lg);
  }

  .grid {
    display: grid;
    gap: var(--spacing-lg);
  }

  .grid-2 {
    grid-template-columns: repeat(2, 1fr);
  }

  .grid-3 {
    grid-template-columns: repeat(3, 1fr);
  }

  .grid-4 {
    grid-template-columns: repeat(4, 1fr);
  }

  .flex {
    display: flex;
  }

  .flex-center {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .flex-between {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  .mb-1 { margin-bottom: var(--spacing-xs); }
  .mb-2 { margin-bottom: var(--spacing-sm); }
  .mb-3 { margin-bottom: var(--spacing-md); }
  .mb-4 { margin-bottom: var(--spacing-lg); }
  .mb-5 { margin-bottom: var(--spacing-xl); }

  .mt-1 { margin-top: var(--spacing-xs); }
  .mt-2 { margin-top: var(--spacing-sm); }
  .mt-3 { margin-top: var(--spacing-md); }
  .mt-4 { margin-top: var(--spacing-lg); }
  .mt-5 { margin-top: var(--spacing-xl); }

  .p-1 { padding: var(--spacing-xs); }
  .p-2 { padding: var(--spacing-sm); }
  .p-3 { padding: var(--spacing-md); }
  .p-4 { padding: var(--spacing-lg); }
  .p-5 { padding: var(--spacing-xl); }
</style>

<div class="readme-container">
  <!-- Header Section -->
  <header class="readme-header animate-fade-in">
    <div class="view-counter">
      <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
        <path d="M1 12s4-8 11-8 11 8 11 8-4 8-11 8-11-8-11-8z"></path>
        <circle cx="12" cy="12" r="3"></circle>
      </svg>
      Profile Views
    </div>
    
    <h1>👋 Hi there, I'm Andri Anto!</h1>
    
    <img src="https://media.giphy.com/media/M9gbBd9nbDrOTu1Mqx/giphy.gif" 
         alt="Developer GIF" 
         class="profile-gif">
    
    <p class="text-gradient" style="font-size: 1.2rem; font-weight: 500;">
      Full Stack Developer from Indonesia
    </p>
  </header>

  <!-- About Section -->
  <section class="about-section animate-slide-in">
    <h2>👩‍💻 About Me</h2>
    <p>I am a passionate Full Stack Developer with experience in building modern web applications. I enjoy solving complex problems and creating efficient, scalable solutions.</p>
    
    <ul class="about-points">
      <li>🔭 Currently working as a Software Engineer, contributing to both frontend and backend development</li>
      <li>🌱 Exploring Technical Content Writing and sharing knowledge through blog posts</li>
      <li>💡 Enjoy solving problems on coding platforms and participating in tech communities</li>
      <li>⚡ In my free time, I solve problems on GeeksforGeeks and read tech articles</li>
      <li>🎯 Focused on creating clean, maintainable code with best practices</li>
    </ul>
    
    <div class="social-links">
      <a href="https://www.linkedin.com/in/andri-anto-072982330" class="social-link">
        <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
          <path d="M20.447 20.452h-3.554v-5.569c0-1.328-.027-3.037-1.852-3.037-1.853 0-2.136 1.445-2.136 2.939v5.667H9.351V9h3.414v1.561h.046c.477-.9 1.637-1.85 3.37-1.85 3.601 0 4.267 2.37 4.267 5.455v6.286zM5.337 7.433c-1.144 0-2.063-.926-2.063-2.065 0-1.138.92-2.063 2.063-2.063 1.14 0 2.064.925 2.064 2.063 0 1.139-.925 2.065-2.064 2.065zm1.782 13.019H3.555V9h3.564v11.452zM22.225 0H1.771C.792 0 0 .774 0 1.729v20.542C0 23.227.792 24 1.771 24h20.451C23.2 24 24 23.227 24 22.271V1.729C24 .774 23.2 0 22.222 0h.003z"/>
        </svg>
        LinkedIn
      </a>
    </div>
  </section>

  <!-- Skills Section -->
  <section class="skills-section">
    <h2 class="text-center">🛠️ Tech Stack & Tools</h2>
    
    <div class="skills-categories">
      <div class="skills-category">
        <h4>📱 Frontend</h4>
        <div class="skills-grid">
          <div class="skill-item" title="React">
            <img src="https://github.com/devicons/devicon/blob/master/icons/react/react-original.svg" alt="React" class="skill-icon">
            <span class="skill-name">React</span>
          </div>
          <div class="skill-item" title="HTML5">
            <img src="https://github.com/devicons/devicon/blob/master/icons/html5/html5-original.svg" alt="HTML5" class="skill-icon">
            <span class="skill-name">HTML5</span>
          </div>
          <div class="skill-item" title="CSS3">
            <img src="https://github.com/devicons/devicon/blob/master/icons/css3/css3-plain-wordmark.svg" alt="CSS3" class="skill-icon">
            <span class="skill-name">CSS3</span>
          </div>
          <div class="skill-item" title="JavaScript">
            <img src="https://github.com/devicons/devicon/blob/master/icons/javascript/javascript-original.svg" alt="JavaScript" class="skill-icon">
            <span class="skill-name">JS</span>
          </div>
        </div>
      </div>
      
      <div class="skills-category">
        <h4>⚙️ Backend</h4>
        <div class="skills-grid">
          <div class="skill-item" title="Node.js">
            <img src="https://github.com/devicons/devicon/blob/master/icons/nodejs/nodejs-original-wordmark.svg" alt="Node.js" class="skill-icon">
            <span class="skill-name">Node.js</span>
          </div>
          <div class="skill-item" title="Spring">
            <img src="https://www.andri.biz.id/skills/he/3.png" alt="Spring" class="skill-icon">
            <span class="skill-name">Spring</span>
          </div>
          <div class="skill-item" title="Java">
            <img src="https://www.andri.biz.id/skills/he/3.png" alt="Java" class="skill-icon">
            <span class="skill-name">Java</span>
          </div>
          <div class="skill-item" title="MySQL">
            <img src="https://github.com/devicons/devicon/blob/master/icons/mysql/mysql-original-wordmark.svg" alt="MySQL" class="skill-icon">
            <span class="skill-name">MySQL</span>
          </div>
        </div>
      </div>
    </div>
    
    <div class="skills-category mt-4">
      <h4>🔧 Tools & Others</h4>
      <div class="skills-grid">
        <div class="skill-item" title="Git">
          <img src="https://github.com/devicons/devicon/blob/master/icons/git/git-original-wordmark.svg" alt="Git" class="skill-icon">
          <span class="skill-name">Git</span>
        </div>
        <div class="skill-item" title="AWS">
          <img src="https://github.com/devicons/devicon/blob/master/icons/amazonwebservices/amazonwebservices-plain-wordmark.svg" alt="AWS" class="skill-icon">
          <span class="skill-name">AWS</span>
        </div>
        <div class="skill-item" title="Firebase">
          <img src="https://github.com/devicons/devicon/blob/master/icons/firebase/firebase-plain-wordmark.svg" alt="Firebase" class="skill-icon">
          <span class="skill-name">Firebase</span>
        </div>
        <div class="skill-item" title="Postman">
          <img src="https://www.vectorlogo.zone/logos/getpostman/getpostman-icon.svg" alt="Postman" class="skill-icon">
          <span class="skill-name">Postman</span>
        </div>
      </div>
    </div>
  </section>

  <!-- Stats Section -->
  <section class="stats-section">
    <h2 class="text-center">📊 GitHub Statistics</h2>
    
    <div class="stats-grid">
      <div class="stat-card animate-fade-in">
        <div class="stat-title">GitHub Streak</div>
        <div class="stat-content">
          <img src="https://nirzak-streak-stats.vercel.app/?user=andri-creative&theme=dark&hide_border=false&theme=dark&background=000000" 
               alt="GitHub Streak" 
               style="width: 100%; height: auto;">
        </div>
      </div>
      
      <div class="stat-card animate-fade-in" style="animation-delay: 0.2s">
        <div class="stat-title">Most Used Languages</div>
        <div class="stat-content">
          <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=andri-creative&layout=compact&theme=vision-friendly-dark" 
               alt="Top Languages" 
               style="width: 100%; height: auto;">
        </div>
      </div>
    </div>
  </section>

  <!-- Support Section -->
  <section class="support-section animate-slide-in">
    <div class="support-content">
      <h3 class="support-title">☕ Support My Work</h3>
      <p class="support-subtitle">If you find my projects useful, consider supporting my work</p>
      
      <div class="support-buttons">
        <a href="https://ko-fi.com/dricode" class="support-button">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
            <path d="M23.881 8.948c-.773-4.085-4.859-4.593-4.859-4.593H.723c-.604 0-.679.798-.679.798s-.082 7.324-.022 11.822c.164 2.424 2.586 2.672 2.586 2.672s8.267-.023 11.966-.049c2.438-.426 2.683-2.566 2.658-3.734 4.352.24 7.422-2.831 6.649-6.916zm-11.062 3.511c-1.246 1.453-4.011 3.976-4.011 3.976s-.121.119-.31.023c-.076-.057-.108-.09-.108-.09-.443-.441-3.368-3.049-4.034-3.954-.709-.965-1.041-2.7-.091-3.71.951-1.01 3.005-1.086 4.363.407 0 0 1.565-1.782 3.468-.963 1.904.82 1.832 3.011.723 4.311zm6.173.478c-.928.116-1.682.028-1.682.028V7.284h1.77s1.971.551 1.971 2.638c0 1.913-.985 2.667-2.059 3.015z"/>
          </svg>
          Buy me a coffee
        </a>
        
        <a href="https://www.patreon.com/dricode" class="support-button">
          <svg width="20" height="20" viewBox="0 0 24 24" fill="currentColor">
            <path d="M0 .5v23h23V.5H0z"/>
          </svg>
          Become a Patron
        </a>
      </div>
    </div>
  </section>

  <!-- Activity Graph -->
  <section class="activity-section">
    <h2 class="text-center">📈 Contribution Graph</h2>
    <div class="activity-graph">
      <img src="https://github-readme-activity-graph.vercel.app/graph?username=andri-creative&theme=github-compact&radius=16" 
           alt="GitHub Activity Graph" 
           style="width: 100%; height: auto;">
    </div>
  </section>

  <!-- Footer -->
  <footer class="readme-footer">
    <p>Made with ❤️ by Andri Anto</p>
    <div class="footer-links">
      <a href="https://github.com/andri-creative" style="color: var(--text-light);">GitHub</a>
      <span>•</span>
      <a href="https://www.linkedin.com/in/andri-anto-072982330" style="color: var(--text-light);">LinkedIn</a>
      <span>•</span>
      <a href="mailto:your-email@example.com" style="color: var(--text-light);">Email</a>
    </div>
    <p class="mt-3" style="font-size: 0.8rem; opacity: 0.7;">
      Last updated: <span id="current-date"></span>
    </p>
  </footer>
</div>

<script>
  // Add current date to footer
  document.getElementById('current-date').textContent = new Date().toLocaleDateString('en-US', {
    year: 'numeric',
    month: 'long',
    day: 'numeric'
  });
  
  // Add hover effects for skills
  document.querySelectorAll('.skill-item').forEach(item => {
    item.addEventListener('mouseenter', function() {
      this.style.transform = 'scale(1.05)';
    });
    item.addEventListener('mouseleave', function() {
      this.style.transform = 'scale(1)';
    });
  });
</script>

---
### 🛠 &nbsp;Languages and Tools :

<p align="center">
  <img src="https://www.andri.biz.id/skills/he/3.png" title="Java" alt="Java" width="50" height="50"/>&nbsp;
  <img src="https://www.andri.biz.id/skills/he/3.png" title="React" alt="React" width="50" height="50"/>&nbsp;
  <img src="https://www.andri.biz.id/skills/he/3.png" title="Spring" alt="Spring" width="50" height="50"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/materialui/materialui-original.svg" title="Material UI" alt="Material UI" width="50" height="50"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/flutter/flutter-original.svg" title="Flutter" alt="Flutter" width="50" height="50"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/redux/redux-original.svg" title="Redux" alt="Redux " width="50" height="50"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/css3/css3-plain-wordmark.svg" title="CSS3" alt="CSS" width="50" height="50"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/html5/html5-original.svg" title="HTML5" alt="HTML" width="50" height="50"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/javascript/javascript-original.svg" title="JavaScript" alt="JavaScript" width="50" height="50"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/firebase/firebase-plain-wordmark.svg" title="Firebase" alt="Firebase" width="50" height="50"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/gatsby/gatsby-original.svg" title="Gatsby" alt="Gatsby" width="50" height="50"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/mysql/mysql-original-wordmark.svg" title="MySQL" alt="MySQL" width="50" height="50"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/nodejs/nodejs-original-wordmark.svg" title="NodeJS" alt="NodeJS" width="50" height="50"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/amazonwebservices/amazonwebservices-plain-wordmark.svg" title="AWS" alt="AWS" width="50" height="50"/>&nbsp;
  <img src="https://www.vectorlogo.zone/logos/getpostman/getpostman-icon.svg" title="Postman" alt="Postman" width="50" height="50"/>&nbsp;
  <img src="https://github.com/devicons/devicon/blob/master/icons/git/git-original-wordmark.svg" title="Git" alt="Git" width="50" height="50"/>&nbsp;
</p>

---

### ✍️ Blog Posts : 
- [How to Create REST APIs with Java and Spring Boot](https://www.twilio.com/blog/create-rest-apis-java-spring-boot)
- [How to Implement Memoization in React to Improve Performance](https://www.sitepoint.com/implement-memoization-in-react-to-improve-performance/)
- [How to Create an Impressive GitHub Profile README](https://www.sitepoint.com/github-profile-readme/)

<p align="center">
  <img src="https://komarev.com/ghpvc/?username=andri-creative&style=flat-square&color=blue" alt="Profile Views">
</p>
