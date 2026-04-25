# Nassos Kranidiotis – Personal Website

A modern, responsive single-page portfolio website hosted on GitHub Pages at [nassoskranidiotis.com](https://nassoskranidiotis.com).

## 🚀 Overview

This is a static website with **no build step** and **no package manager**—just HTML, CSS, and JavaScript. All dependencies are loaded from CDNs. Perfect for fast deployment and easy maintenance.

## 📁 Project Structure

```
.
├── index.html              # Main single-page application
├── style.css               # Custom styles (layered on Bootstrap 5)
├── script.js               # JavaScript utilities (back-to-top, AOS init)
├── CNAME                   # Custom domain configuration
├── assets/
│   ├── vb1.mp4            # Video background
│   ├── video-poster.webp  # Video fallback poster
│   ├── founder.webp       # Profile image
│   ├── scienceart-bg.webp # Science & Art section background
│   ├── logotext.png       # Navbar logo
│   ├── companyname.png    # Home section logo
│   ├── xpert.webp         # Xpert app preview
│   ├── tutorials.webp     # Tutorials preview
│   ├── books.webp         # Books preview
│   ├── blog.webp          # Blog preview
│   ├── poetry.webp        # Poetry preview
│   ├── it.webp            # IT section preview
│   ├── gallery.webp       # Gallery preview
│   ├── favicon.ico        # Site favicon
│   └── logo.png           # Logo variant
└── gi/
    └── index.html         # Redirect page to Glycemic Index app
```

## 🎨 Key Features

- **Single-page application** — Smooth anchor-link navigation between sections
- **Video background** — Full-screen video with optimized fallback poster
- **Responsive design** — Mobile-first approach using Bootstrap 5
- **Smooth scrolling** — CSS scroll behavior + smooth margins
- **Parallax effects** — Fixed background images with overlays
- **Scroll animations** — AOS (Animate On Scroll) library
- **Dark theme** — Optimized for visual appeal and readability

## 🔧 Technology Stack

### Frontend Framework & Styling
- **Bootstrap 5.3.3** (CSS + JS bundle) — Responsive grid and components
- **Bootstrap Icons 1.10.5** — Icon library
- **Custom CSS** — Enhanced styles and theme customization

### JavaScript Library
- **AOS 2.3.4** — Scroll-triggered animations

### Architecture
- Vanilla HTML, CSS, and JavaScript (no frameworks)
- All dependencies loaded from CDN (jsDelivr, Unpkg)
- No build process, no package manager required

## 📄 Page Sections

The site is structured as a single-page application with anchor-linked sections:

1. **#home** — Hero section with branding and age display
2. **#profile** — Professional background and biography
3. **#projects** — Showcase of featured projects (Xpert, Tutorials, Books, etc.)
4. **#scienceart** — Science and artistic interests section
5. **#followme** — Social links and contact information

## 🏃 Local Development

### Quick Start
Open `index.html` directly in your browser, or serve it locally:

```bash
# Using Python built-in server
python3 -m http.server 8080

# Then visit: http://localhost:8080
```

### Browser Testing
- Test on multiple devices (desktop, tablet, mobile)
- Check the video background plays smoothly
- Verify smooth scrolling and animations
- Test navbar responsiveness

## 🚀 Deployment

Push to the `main` branch — **GitHub Pages deploys automatically**.

### DNS & Domain Configuration
The custom domain is configured via:
- **CNAME file** — Points to GitHub Pages
- **DNS A records** — Points to GitHub's infrastructure
- See `notes.txt` for DNS setup details

## 🎯 Architecture Notes

### Video Background
- `position: fixed; z-index: -1` ensures all sections scroll over it
- Includes a poster image for faster initial load
- Uses `preload="none"` for optimization

### Science & Art Section
- Parallax-style fixed background image (`scienceart-bg.webp`)
- Dark overlay applied via `::before` pseudo-element
- Creates depth while maintaining readability

### AOS (Animate On Scroll)
- Initialized in `script.js` (runs last, overrides inline initialization)
- Adds fade/slide animations as elements enter viewport
- Improves visual hierarchy during scrolling

## 📝 Editing Guide

### Updating Content
1. Edit `index.html` to modify section content
2. Update `style.css` for custom styling
3. Add logic to `script.js` for interactive features
4. Push to deploy

### Adding New Assets
1. Optimize images (`.webp` format preferred)
2. Optimize videos (consider compression)
3. Place in `assets/` folder
4. Reference in HTML

### Customization Tips
- **Colors** — Modify CSS custom properties or directly in `style.css`
- **Typography** — Adjust font families and sizes in `style.css`
- **Animations** — Configure AOS options or add custom CSS animations
- **Navbar** — Update links in `index.html` navbar section

## 🔐 Meta Tags & SEO

- Open Graph tags for social media sharing
- Meta description for search engine snippets
- Structured author and keyword metadata
- Responsive viewport configuration

## 📋 Requirements

None! This is a static site with CDN dependencies. No installation needed.

## 📄 License

This project is the personal website of Nassos Kranidiotis.

## 📧 Contact

For inquiries, visit [nassoskranidiotis.com](https://nassoskranidiotis.com) or follow the contact links in the "Follow Me" section.
