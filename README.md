# Unreal Engine Game Programmer Portfolio

A modern, responsive portfolio website designed specifically for Unreal Engine game programmers. Features a dark, cyberpunk-inspired theme with neon accents and smooth animations.

## 🎮 Features

### Design & Theme
- **Dark Cyberpunk Theme**: Modern dark design with neon green accents
- **Responsive Design**: Fully responsive across all devices
- **Smooth Animations**: CSS animations and JavaScript interactions
- **Game Development Focus**: Content specifically tailored for game programmers

### Sections
1. **Hero Section**: Eye-catching introduction with animated code window
2. **About Section**: Professional background and technical skills
3. **Projects Section**: Showcase of game development projects
4. **Plugins Section**: Marketplace plugins with ratings and pricing
5. **Contact Section**: Contact form and professional information

### Interactive Elements
- **Mobile Navigation**: Hamburger menu for mobile devices
- **Smooth Scrolling**: Navigation links with smooth scroll behavior
- **Hover Effects**: Interactive cards and buttons
- **Contact Form**: Functional contact form with validation
- **Loading Animation**: Professional loading screen
- **Typing Animation**: Animated text effects

## 🛠️ Technologies Used

- **HTML5**: Semantic markup
- **CSS3**: Modern styling with CSS Grid, Flexbox, and custom properties
- **JavaScript (ES6+)**: Interactive features and animations
- **Font Awesome**: Icons
- **Google Fonts**: Orbitron (for headings) and Roboto (for body text)

## 📁 File Structure

```
portfolio/
├── index.html          # Main HTML file
├── styles.css          # CSS styles
├── script.js           # JavaScript functionality
└── README.md           # This file
```

## 🚀 Getting Started

1. **Download/Clone** the files to your local machine
2. **Open** `index.html` in your web browser
3. **Customize** the content to match your personal information

## ✏️ Customization Guide

### Personal Information
Edit the following sections in `index.html`:

#### Hero Section
```html
<h1 class="hero-title">Your Name - Unreal Engine Game Programmer</h1>
<p class="hero-subtitle">Your tagline here</p>
```

#### Stats
```html
<div class="stat">
    <span class="stat-number">5+</span>
    <span class="stat-label">Years Experience</span>
</div>
```

#### About Section
```html
<p>Your personal description here...</p>
```

#### Contact Information
```html
<span>your.email@example.com</span>
<span>+1 (555) 123-4567</span>
<span>Your Location</span>
```

### Projects
Replace the project cards with your own projects:

```html
<div class="project-card">
    <div class="project-image">
        <img src="your-project-image.jpg" alt="Project Name">
    </div>
    <div class="project-content">
        <h3>Your Project Name</h3>
        <p>Project description...</p>
        <div class="project-tech">
            <span class="tech-tag">Unreal Engine 5</span>
            <span class="tech-tag">C++</span>
        </div>
    </div>
</div>
```

### Plugins
Update the plugin cards with your marketplace plugins:

```html
<div class="plugin-card">
    <div class="plugin-header">
        <div class="plugin-icon">
            <i class="fas fa-robot"></i>
        </div>
        <div class="plugin-info">
            <h3>Your Plugin Name</h3>
            <div class="plugin-rating">
                <i class="fas fa-star"></i>
                <span>(reviews)</span>
            </div>
        </div>
    </div>
    <p>Plugin description...</p>
    <div class="plugin-footer">
        <span class="plugin-price">$29.99</span>
        <a href="#" class="btn btn-small">View Plugin</a>
    </div>
</div>
```

### Colors & Theme
Customize the color scheme in `styles.css`:

```css
:root {
    --primary-color: #00ff88;      /* Main accent color */
    --secondary-color: #ff6b35;    /* Secondary accent */
    --accent-color: #4ecdc4;       /* Additional accent */
    --dark-bg: #0a0a0a;           /* Main background */
    --darker-bg: #050505;         /* Secondary background */
    --card-bg: #1a1a1a;           /* Card background */
    --text-primary: #ffffff;      /* Primary text */
    --text-secondary: #b0b0b0;    /* Secondary text */
}
```

## 🎨 Design Features

### Typography
- **Orbitron**: Used for headings (gaming/tech aesthetic)
- **Roboto**: Used for body text (clean and readable)

### Animations
- **Fade-in effects**: Elements animate in as you scroll
- **Hover effects**: Interactive elements respond to mouse hover
- **Typing animation**: Hero title types out on page load
- **Parallax scrolling**: Subtle parallax effect on hero section

### Responsive Breakpoints
- **Desktop**: 1200px and above
- **Tablet**: 768px - 1199px
- **Mobile**: Below 768px

## 📱 Mobile Features

- **Touch-friendly**: All interactive elements are optimized for touch
- **Responsive navigation**: Hamburger menu for mobile devices
- **Optimized layout**: Content reflows for smaller screens
- **Performance**: Optimized animations for mobile devices

## 🔧 Browser Support

- **Chrome**: Full support
- **Firefox**: Full support
- **Safari**: Full support
- **Edge**: Full support
- **Mobile browsers**: Full support

## 📧 Contact Form

The contact form includes:
- **Form validation**: Client-side validation for required fields
- **Email validation**: Checks for valid email format
- **Success/Error notifications**: User feedback for form submission
- **Responsive design**: Works on all device sizes

## 🚀 Deployment

### Local Development
1. Open `index.html` in your browser
2. All features work locally without a server

### Web Hosting
1. Upload all files to your web hosting service
2. Ensure all files are in the same directory
3. Access via your domain name

### GitHub Pages
1. Create a new repository
2. Upload all files
3. Enable GitHub Pages in repository settings
4. Your portfolio will be available at `username.github.io/repository-name`

## 📝 License

This portfolio template is free to use and modify for personal and commercial projects.

## 🤝 Contributing

Feel free to submit issues, feature requests, or pull requests to improve this portfolio template.

## 📞 Support

If you need help customizing this portfolio or have questions, feel free to reach out!

---

**Built with ❤️ for the Unreal Engine community** 