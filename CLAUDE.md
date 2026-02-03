# CLAUDE.md

## Project Overview

Static personal portfolio website for Noah Stanford, an accounting professional. Built with plain HTML and CSS — no frameworks, no build tools, no JavaScript. Designed for deployment on GitHub Pages.

## Repository Structure

```
/
├── index.html          # Entire website (HTML + embedded CSS, ~425 lines)
├── images.jpg          # Gallery image
├── images (1).jpg      # Gallery image
└── README.md           # Minimal project description
```

## Tech Stack

- **HTML5** with semantic elements (`<header>`, `<main>`, `<section>`, `<footer>`)
- **CSS3** embedded in `<style>` tag within `index.html` (no external stylesheets)
- **No JavaScript**, build tools, or dependencies

## Key Conventions

### HTML/CSS Patterns
- All styles live inside `index.html` in a single `<style>` block — there are no external CSS files
- Descriptive class names: `highlight-card`, `experience-item`, `education-item`, `gallery-item`, `skill-tag`
- Proper semantic HTML with heading hierarchy (h1 > h2 > h3)
- CSS reset at top of styles (`* { margin: 0; padding: 0; box-sizing: border-box; }`)

### Design System
- **Color palette**: Primary green `#527d5f`, dark green `#3d5a47`, backgrounds `#f7fafc` / `#f8faf9`, text `#2d3748` / `#5a6c7d`
- **Typography**: System font stack (`-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, ...`)
- **Spacing**: Consistent units of 30px, 40px, 60px
- **Responsive**: Single breakpoint at `max-width: 768px`
- **Interactions**: CSS transitions on hover states (cards lift, skill tags change color)

### Layout
- CSS Grid with `auto-fit` and `minmax()` for responsive card grids
- Flexbox for alignment within components
- Max container width of 1200px, centered

## Page Sections (in order)

1. **Header** — Name, title, contact info (phone, email, location)
2. **Highlights** — 5 cards with key qualifications
3. **Experience** — 3 work entries with bullet points
4. **Education** — 2 entries (university + high school)
5. **Skills** — 8 tags with hover effects
6. **Gallery** — 2 images in responsive grid
7. **Volunteer** — Missionary service
8. **Footer** — Copyright + "Built for GitHub Pages"

## Development Workflow

- No build step required — edit `index.html` directly and open in browser
- Deployment target is GitHub Pages (serves static files from the repo)
- No CI/CD pipelines, no testing frameworks
- No `.gitignore` — repo is small enough that defaults suffice

## Working With This Codebase

- When modifying styles, edit the `<style>` block inside `index.html`
- When adding content sections, follow the existing pattern: `<section>` with a class, an `<h2>` title, and content in card/item containers
- Image files sit in the repo root (note the space in `images (1).jpg` — quote paths when referencing)
- Keep the site self-contained: avoid adding external dependencies or build tooling unless explicitly requested
