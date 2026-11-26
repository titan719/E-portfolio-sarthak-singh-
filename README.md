# Sarthak Singh — AI/ML Portfolio

A cinematic, dark-mode portfolio website blending Apple's premium structure with SpaceX's bold typography. Built as a single self-contained HTML file for easy GitHub Pages deployment.

## 🌐 Live Demo

Deploy to GitHub Pages: `https://<your-username>.github.io/<repo-name>/`

## 📁 Project Structure

```
portfolio/
├── index.html          # Main portfolio (self-contained)
├── assets/
│   ├── ultrasonic_radar.mp4      # Project 1 video
│   ├── arduino_basics.mp4        # Project 2 video
│   └── potentiometer.mp4         # Project 3 video
└── README.md
```

## 🚀 Quick Deploy to GitHub Pages

### Option 1: GitHub Web Interface (Easiest)

1. **Create a new repository** on GitHub named `portfolio` (or any name)
2. **Upload files**:
   - Go to your repo → "Add file" → "Upload files"
   - Drag and drop the entire `portfolio/` folder contents
   - Commit changes
3. **Enable GitHub Pages**:
   - Settings → Pages → Source: "Deploy from a branch"
   - Branch: `main` / Folder: `/ (root)` → Save
4. **Your site is live** at `https://<username>.github.io/portfolio/`

### Option 2: Command Line

```bash
# In your portfolio folder
git init
git add .
git commit -m "Initial portfolio commit"
git branch -M main
git remote add origin https://github.com/<your-username>/portfolio.git
git push -u origin main

# Then enable Pages in GitHub Settings → Pages
```

## ✏️ Customization Guide

### Update Personal Info
Edit these sections in `index.html`:

**Hero Section** (lines ~200-215):
```html
<h1 class="hero__headline display-hero">Building Intelligent Systems</h1>
<p class="hero__subheadline body-text">
  Your custom tagline here...
</p>
```

**Contact Email** (line ~580):
```html
<a href="mailto:your.email@example.com" class="footer__email">
  your.email@example.com
</a>
```

**Social Links** — Add to footer contact section:
```html
<a href="https://github.com/yourusername" class="footer__email" target="_blank" rel="noopener">
  <svg>...</svg> GitHub
</a>
<a href="https://linkedin.com/in/yourusername" class="footer__email" target="_blank" rel="noopener">
  <svg>...</svg> LinkedIn
</a>
```

### Add/Modify Projects

Each project is an `<article class="project-card">` block. Duplicate and modify:

```html
<article class="project-card reveal reveal--delay-1" role="listitem">
  <div class="project-card__media">
    <video 
      class="project-card__video" 
      src="assets/your-video.mp4" 
      muted loop playsinline preload="metadata"
      aria-label="Project description"
    ></video>
    <div class="project-card__play" aria-hidden="true">
      <svg viewBox="0 0 24 24" fill="currentColor">
        <polygon points="5,3 19,12 5,21"/>
      </svg>
    </div>
  </div>
  <div class="project-card__content">
    <div class="project-card__meta">
      <span class="project-card__tag">Tag1</span>
      <span class="project-card__tag">Tag2</span>
    </div>
    <h3 class="project-card__title project-title">Project Title</h3>
    <p class="project-card__description body-text">
      Project description...
    </p>
    <div class="project-card__footer">
      <a href="#" class="project-card__link">
        View Details
        <svg viewBox="0 0 24 24" fill="none" stroke-width="2">
          <path d="M5 12h14M12 5l7 7-7 7"/>
        </svg>
      </a>
    </div>
  </div>
</article>
```

**Add project video**: Place `.mp4` file in `assets/` and update `src="assets/your-video.mp4"`

### Add Project Images (Instead of Videos)

Replace the `<video>` block with:
```html
<img 
  class="project-card__video" 
  src="assets/your-image.jpg" 
  alt="Project screenshot"
  loading="lazy"
>
```

## 🎨 Design System

### Color Palette
| Token | Value | Usage |
|-------|-------|-------|
| `--space-black` | `#000000` | Page background |
| `--spectral-white` | `#f0f0fa` | Primary text |
| `--spectral-white-80` | `rgba(240,240,250,0.8)` | Secondary text |
| `--spectral-white-60` | `rgba(240,240,250,0.6)` | Muted text |
| `--accent-blue` | `#0071e3` | CTAs, links, accents |
| `--ghost-bg` | `rgba(240,240,250,0.1)` | Ghost button bg |
| `--ghost-border` | `rgba(240,240,250,0.35)` | Ghost button border |

### Typography
- **Font**: Inter (via Google Fonts) with system fallbacks
- **Headlines**: Uppercase, tight line-height, positive letter-spacing (SpaceX style)
- **Body**: Sentence case, relaxed line-height (Apple style)
- **Scale**: Fluid clamping via `clamp()` for responsive sizing

### Spacing Scale
Base unit: 8px → `--space-xs` (4px) through `--space-5xl` (128px)

## ♿ Accessibility Features

- Semantic HTML5 structure
- ARIA labels and roles
- Focus-visible outlines
- `prefers-reduced-motion` support
- Alt text for media
- Keyboard navigable
- Sufficient contrast ratios (WCAG AA)

## 📱 Responsive Breakpoints

- Mobile: `< 480px` — Single column, stacked CTAs
- Tablet: `480–768px` — 2-column project grid
- Desktop: `768–1024px` — Full navigation, 2-col grid
- Large: `> 1024px` — 3-column project grid, max-width container

## 🔧 Performance

- Self-contained (no external CSS/JS files)
- Inter font preloaded
- Video `preload="metadata"` + lazy load via IntersectionObserver
- CSS custom properties for theming
- Minimal JS (~2KB gzipped)

## 📝 License

MIT — Feel free to use as a template for your own portfolio.

---

**Built with precision** • Sarthak Singh — BTech AI/ML Student