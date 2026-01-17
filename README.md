/* Reset and Base Styles */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  --primary-color: #0891b2; /* Changed from #00ff88 to cyan-blue */
  --secondary-color: #06b6d4; /* Updated to complement cyan */
  --accent-color: #22d3ee; /* Lighter cyan for accents */
  --dark-bg: #0a0a0a;
  --darker-bg: #050505;
  --card-bg: #1a1a1a;
  --text-primary: #ffffff;
  --text-secondary: #b0b0b0;
  --text-muted: #666666;
  --border-color: #333333;
  --gradient-primary: linear-gradient(135deg, #0891b2 0%, #22d3ee 100%); /* Updated gradient */
  --gradient-secondary: linear-gradient(135deg, #06b6d4 0%, #0891b2 100%); /* Updated secondary gradient */
  --shadow-glow: 0 0 20px rgba(8, 145, 178, 0.3); /* Updated glow to cyan */
  --shadow-card: 0 8px 32px rgba(0, 0, 0, 0.3);
}

body {
  font-family: 'Roboto', sans-serif;
  background: var(--dark-bg);
  color: var(--text-primary);
  line-height: 1.6;
  overflow-x: hidden;
}

.container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
}

/* Typography */
h1, h2, h3, h4, h5, h6 {
  font-family: 'Orbitron', monospace;
  font-weight: 700;
}

.section-title {
  font-size: 2.5rem;
  text-align: center;
  margin-bottom: 3rem;
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
  position: relative;
}

.section-title::after {
  content: '';
  position: absolute;
  bottom: -10px;
  left: 50%;
  transform: translateX(-50%);
  width: 80px;
  height: 3px;
  background: var(--gradient-primary);
  border-radius: 2px;
}

/* Navigation */
.navbar {
  position: fixed;
  top: 0;
  width: 100%;
  background: rgba(10, 10, 10, 0.95);
  backdrop-filter: blur(10px);
  z-index: 1000;
  padding: 1rem 0;
  transition: all 0.3s ease;
}

.nav-container {
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.nav-logo {
  display: flex;
  align-items: center;
  gap: 10px;
  font-family: 'Orbitron', monospace;
  font-size: 1.5rem;
  font-weight: 700;
  color: var(--primary-color);
}

.nav-logo i {
  font-size: 1.8rem;
}

.nav-menu {
  display: flex;
  list-style: none;
  gap: 2rem;
}

.nav-link {
  color: var(--text-primary);
  text-decoration: none;
  font-weight: 500;
  transition: all 0.3s ease;
  position: relative;
}

.nav-link:hover {
  color: var(--primary-color);
}

.nav-link::after {
  content: '';
  position: absolute;
  bottom: -5px;
  left: 0;
  width: 0;
  height: 2px;
  background: var(--gradient-primary);
  transition: width 0.3s ease;
}

.nav-link:hover::after {
  width: 100%;
}

.hamburger {
  display: none;
  flex-direction: column;
  cursor: pointer;
}

.bar {
  width: 25px;
  height: 3px;
  background: var(--text-primary);
  margin: 3px 0;
  transition: 0.3s;
}

/* Hero Section */
.hero {
  min-height: 100vh;
  display: flex;
  align-items: center;
  background: linear-gradient(135deg, var(--darker-bg) 0%, var(--dark-bg) 100%);
  position: relative;
  overflow: hidden;
}

.hero::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: url('data:image/svg+xml,');
  opacity: 0.3;
}

.hero-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 20px;
  position: relative;
  z-index: 2;
}

.hero-title {
  font-size: 3.5rem;
  margin-bottom: 1rem;
  background: var(--gradient-primary);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  background-clip: text;
}

.hero-subtitle {
  font-size: 1.2rem;
  color: var(--text-secondary);
  margin-bottom: 2rem;
}

.hero-stats {
  display: flex;
  gap: 2rem;
  margin-bottom: 2rem;
}

.stat {
  text-align: center;
}

.stat-number {
  display: block;
  font-size: 2rem;
  font-weight: 700;
  color: var(--primary-color);
  font-family: 'Orbitron', monospace;
}

.stat-label {
  font-size: 0.9rem;
  color: var(--text-secondary);
}

.hero-buttons {
  display: flex;
  gap: 1rem;
}

.btn {
  padding: 12px 24px;
  border: none;
  border-radius: 5px;
  text-decoration: none;
  font-weight: 600;
  transition: all 0.3s ease;
  cursor: pointer;
  display: inline-block;
  text-align: center;
}

.btn-primary {
  background: var(--gradient-primary);
  color: var(--dark-bg);
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-glow);
}

.btn-secondary {
  background: transparent;
  color: var(--primary-color);
  border: 2px solid var(--primary-color);
}

.btn-secondary:hover {
  background: var(--primary-color);
  color: var(--dark-bg);
  transform: translateY(-2px);
}

.btn-small {
  padding: 8px 16px;
  font-size: 0.9rem;
}

/* Enhanced Code Window with IDE-like styling */
.code-window {
  background: var(--card-bg);
  border-radius: 10px;
  overflow: hidden;
  box-shadow: var(--shadow-card);
  border: 1px solid var(--border-color);
  position: relative;
}

.code-window::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 2px;
  background: var(--gradient-primary);
}

.window-header {
  background: var(--darker-bg);
  padding: 10px 15px;
  display: flex;
  align-items: center;
  gap: 10px;
  border-bottom: 1px solid var(--border-color);
}

.window-buttons {
  display: flex;
  gap: 8px;
}

.btn-red, .btn-yellow, .btn-green {
  width: 12px;
  height: 12px;
  border-radius: 50%;
}

.btn-red { background: #ff5f56; }
.btn-yellow { background: #ffbd2e; }
.btn-green { background: #27ca3f; }

.window-title {
  color: var(--text-secondary);
  font-size: 0.9rem;
  margin-left: 10px;
}

.code-content {
  padding: 20px;
  background: #1e1e1e; /* VS Code dark background */
  position: relative;
}

.code-content pre {
  margin: 0;
  font-family: 'Fira Code', 'Consolas', 'Monaco', 'Courier New', monospace;
  font-size: 0.9rem;
  line-height: 1.5;
  overflow-x: auto;
}

/* Line numbers */
.code-content::before {
  content: '1\a2\a3\a4\a5\a6\a7\a8\a9\a10\a11\a12\a13\a14';
  position: absolute;
  left: 0;
  top: 20px;
  padding: 0 10px;
  color: #6e7681;
  font-family: 'Fira Code', 'Consolas', 'Monaco', 'Courier New', monospace;
  font-size: 0.9rem;
  line-height: 1.5;
  white-space: pre;
  border-right: 1px solid var(--border-color);
  width: 40px;
  text-align: right;
}

.code-content code {
  color: #d4d4d4; /* Default text color */
  margin-left: 50px;
  display: block;
}

/* IDE-like Syntax Highlighting */
.code-content .keyword {
  color: #569cd6; /* Blue for keywords */
  font-weight: 600;
}

.code-content .class-name {
  color: #4ec9b0; /* Teal for class names */
  font-weight: 500;
}

.code-content .function {
  color: #dcdcaa; /* Yellow for functions */
  font-weight: 500;
}

.code-content .comment {
  color: #6a9955; /* Green for comments */
  font-style: italic;
}

.code-content .string {
  color: #ce9178; /* Orange for strings */
}

.code-content .number {
  color: #b5cea8; /* Light green for numbers */
}

.code-content .operator {
  color: #d4d4d4; /* White for operators */
}

.code-content .macro {
  color: #c586c0; /* Purple for macros */
  font-weight: 600;
}

.code-content .type {
  color: #4fc1ff; /* Light blue for types */
}

.code-content .punctuation {
  color: #d4d4d4; /* White for punctuation */
}

.code-content .namespace {
  color: #4ec9b0; /* Teal for namespaces */
}

.code-content .access-modifier {
  color: #569cd6; /* Blue for access modifiers */
  font-weight: 600;
}

/* Code content scrollbar styling */
.code-content::-webkit-scrollbar {
  width: 8px;
  height: 8px;
}

.code-content::-webkit-scrollbar-track {
  background: var(--darker-bg);
}

.code-content::-webkit-scrollbar-thumb {
  background: var(--primary-color);
  border-radius: 4px;
}

.code-content::-webkit-scrollbar-thumb:hover {
  background: var(--accent-color);
}

.scroll-indicator {
  position: absolute;
  bottom: 30px;
  left: 50%;
  transform: translateX(-50%);
  color: var(--primary-color);
  font-size: 1.5rem;
  animation: bounce 2s infinite;
}

@keyframes bounce {
  0%, 20%, 50%, 80%, 100% { transform: translateX(-50%) translateY(0); }
  40% { transform: translateX(-50%) translateY(-10px); }
  60% { transform: translateX(-50%) translateY(-5px); }
}

/* About Section */
.about {
  padding: 100px 0;
  background: var(--darker-bg);
}

.about-content {
  display: grid;
  grid-template-columns: 2fr 1fr;
  gap: 4rem;
  align-items: start;
}

.about-text p {
  margin-bottom: 1.5rem;
  color: var(--text-secondary);
  font-size: 1.1rem;
}

.skills h3 {
  margin-bottom: 1rem;
  color: var(--primary-color);
}

.skill-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 10px;
}

.skill-tag {
  background: var(--card-bg);
  color: var(--primary-color);
  padding: 8px 16px;
  border-radius: 20px;
  font-size: 0.9rem;
  border: 1px solid var(--border-color);
  transition: all 0.3s ease;
}

.skill-tag:hover {
  background: var(--primary-color);
  color: var(--dark-bg);
  transform: translateY(-2px);
}

.profile-card {
  background: var(--card-bg);
  padding: 2rem;
  border-radius: 15px;
  text-align: center;
  box-shadow: var(--shadow-card);
  border: 1px solid var(--border-color);
}

.profile-avatar {
  width: 80px;
  height: 80px;
  background: var(--gradient-primary);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 0 auto 1rem;
  font-size: 2rem;
  color: var(--dark-bg);
}

.profile-card h3 {
  margin-bottom: 0.5rem;
  color: var(--primary-color);
}

.profile-card p {
  color: var(--text-secondary);
  margin-bottom: 1rem;
}

.social-links {
  display: flex;
  justify-content: center;
  gap: 1rem;
}

.social-link {
  width: 40px;
  height: 40px;
  background: var(--card-bg);
  border: 1px solid var(--border-color);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--text-secondary);
  transition: all 0.3s ease;
}

.social-link:hover {
  background: var(--primary-color);
  color: var(--dark-bg);
  transform: translateY(-2px);
}

/* Projects Section */
.projects {
  padding: 100px 0;
}

.projects-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.project-card {
  background: var(--card-bg);
  border-radius: 15px;
  overflow: hidden;
  box-shadow: var(--shadow-card);
  border: 1px solid var(--border-color);
  transition: all 0.3s ease;
}

.project-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 20px 40px rgba(0, 0, 0, 0.4);
}

.project-image {
  position: relative;
  overflow: hidden;
}

.project-image img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  transition: transform 0.3s ease;
}

.project-card:hover .project-image img {
  transform: scale(1.1);
}

.project-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: rgba(0, 0, 0, 0.8);
  display: flex;
  align-items: center;
  justify-content: center;
  opacity: 0;
  transition: opacity 0.3s ease;
}

.project-card:hover .project-overlay {
  opacity: 1;
}

.project-links {
  display: flex;
  gap: 1rem;
}

.project-link {
  width: 50px;
  height: 50px;
  background: var(--primary-color);
  color: var(--dark-bg);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  text-decoration: none;
  transition: all 0.3s ease;
}

.project-link:hover {
  transform: scale(1.1);
  box-shadow: var(--shadow-glow);
}

.project-content {
  padding: 1.5rem;
}

.project-content h3 {
  margin-bottom: 1rem;
  color: var(--primary-color);
}

.project-content p {
  color: var(--text-secondary);
  margin-bottom: 1rem;
}

.project-tech {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
}

.tech-tag {
  background: var(--darker-bg);
  color: var(--accent-color);
  padding: 4px 12px;
  border-radius: 15px;
  font-size: 0.8rem;
  border: 1px solid var(--border-color);
}

/* Plugins Section */
.plugins {
  padding: 100px 0;
  background: var(--darker-bg);
}

.plugins-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
}

.plugin-card {
  background: var(--card-bg);
  border-radius: 15px;
  padding: 1.5rem;
  box-shadow: var(--shadow-card);
  border: 1px solid var(--border-color);
  transition: all 0.3s ease;
}

.plugin-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.4);
}

.plugin-header {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1rem;
}

.plugin-icon {
  width: 50px;
  height: 50px;
  background: var(--gradient-primary);
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 1.5rem;
  color: var(--dark-bg);
}

.plugin-info h3 {
  color: var(--primary-color);
  margin-bottom: 0.5rem;
}

.plugin-rating {
  display: flex;
  align-items: center;
  gap: 5px;
}

.plugin-rating i {
  color: #ffd700;
  font-size: 0.9rem;
}

.plugin-rating span {
  color: var(--text-secondary);
  font-size: 0.8rem;
}

.plugin-card p {
  color: var(--text-secondary);
  margin-bottom: 1rem;
}

.plugin-features {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-bottom: 1rem;
}

.feature-tag {
  background: var(--darker-bg);
  color: var(--secondary-color);
  padding: 4px 12px;
  border-radius: 15px;
  font-size: 0.8rem;
  border: 1px solid var(--border-color);
}

.plugin-footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.plugin-price {
  font-size: 1.2rem;
  font-weight: 700;
  color: var(--primary-color);
  font-family: 'Orbitron', monospace;
}

/* Contact Section */
.contact {
  padding: 100px 0;
}

.contact-content {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
}

.contact-info h3 {
  color: var(--primary-color);
  margin-bottom: 1rem;
}

.contact-info p {
  color: var(--text-secondary);
  margin-bottom: 2rem;
}

.contact-details {
  margin-bottom: 2rem;
}

.contact-item {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1rem;
}

.contact-item i {
  color: var(--primary-color);
  width: 20px;
}

.social-links-large {
  display: flex;
  gap: 1rem;
}

.social-link-large {
  width: 50px;
  height: 50px;
  background: var(--card-bg);
  border: 1px solid var(--border-color);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--text-secondary);
  font-size: 1.2rem;
  transition: all 0.3s ease;
}

.social-link-large:hover {
  background: var(--primary-color);
  color: var(--dark-bg);
  transform: translateY(-2px);
}

.contact-form {
  background: var(--card-bg);
  padding: 2rem;
  border-radius: 15px;
  box-shadow: var(--shadow-card);
  border: 1px solid var(--border-color);
}

.form-group {
  margin-bottom: 1.5rem;
}

.form-group input,
.form-group textarea {
  width: 100%;
  padding: 12px;
  background: var(--darker-bg);
  border: 1px solid var(--border-color);
  border-radius: 5px;
  color: var(--text-primary);
  font-family: inherit;
  transition: all 0.3s ease;
}

.form-group input:focus,
.form-group textarea:focus {
  outline: none;
  border-color: var(--primary-color);
  box-shadow: 0 0 0 2px rgba(0, 255, 136, 0.2);
}

.form-group textarea {
  resize: vertical;
  min-height: 120px;
}

/* Footer */
.footer {
  background: var(--darker-bg);
  padding: 3rem 0 1rem;
  border-top: 1px solid var(--border-color);
}

.footer-content {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 2rem;
  margin-bottom: 2rem;
}

.footer-section h3,
.footer-section h4 {
  color: var(--primary-color);
  margin-bottom: 1rem;
}

.footer-section p {
  color: var(--text-secondary);
}

.footer-section ul {
  list-style: none;
}

.footer-section ul li {
  margin-bottom: 0.5rem;
}

.footer-section ul li a {
  color: var(--text-secondary);
  text-decoration: none;
  transition: color 0.3s ease;
}

.footer-section ul li a:hover {
  color: var(--primary-color);
}

.footer-social {
  display: flex;
  gap: 1rem;
}

.footer-social a {
  width: 40px;
  height: 40px;
  background: var(--card-bg);
  border: 1px solid var(--border-color);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  color: var(--text-secondary);
  transition: all 0.3s ease;
}

.footer-social a:hover {
  background: var(--primary-color);
  color: var(--dark-bg);
  transform: translateY(-2px);
}

.footer-bottom {
  text-align: center;
  padding-top: 2rem;
  border-top: 1px solid var(--border-color);
  color: var(--text-muted);
}

/* Responsive Design */
@media (max-width: 768px) {
  .hamburger {
    display: flex;
  }

  .nav-menu {
    position: fixed;
    left: -100%;
    top: 70px;
    flex-direction: column;
    background-color: var(--darker-bg);
    width: 100%;
    text-align: center;
    transition: 0.3s;
    box-shadow: 0 10px 27px rgba(0, 0, 0, 0.05);
    padding: 2rem 0;
  }

  .nav-menu.active {
    left: 0;
  }

  .hero-content {
    grid-template-columns: 1fr;
    text-align: center;
    gap: 2rem;
  }

  .hero-title {
    font-size: 2.5rem;
  }

  .hero-stats {
    justify-content: center;
  }

  .about-content {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .contact-content {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .projects-grid,
  .plugins-grid {
    grid-template-columns: 1fr;
  }

  .section-title {
    font-size: 2rem;
  }
}

@media (max-width: 480px) {
  .hero-title {
    font-size: 2rem;
  }

  .hero-stats {
    flex-direction: column;
    gap: 1rem;
  }

  .hero-buttons {
    flex-direction: column;
    align-items: center;
  }

  .btn {
    width: 100%;
    max-width: 200px;
  }
}

/* Smooth Scrolling */
html {
  scroll-behavior: smooth;
}

/* Loading Animation */
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

.fade-in-up {
  animation: fadeInUp 0.6s ease-out;
}

/* Custom Scrollbar */
::-webkit-scrollbar {
  width: 8px;
}

::-webkit-scrollbar-track {
  background: var(--darker-bg);
}

::-webkit-scrollbar-thumb {
  background: var(--primary-color);
  border-radius: 4px;
}

::-webkit-scrollbar-thumb:hover {
  background: var(--accent-color);
}
