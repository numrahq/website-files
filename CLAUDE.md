# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Numra is a static landing page for an AI-powered finance operations platform. This is a single-page marketing website built with **vanilla HTML, CSS, and JavaScript** - no build system, no framework, no compilation step required.

## Technology Stack

- **Pure HTML5** - All content and styles in `index.html`
- **Tailwind CSS** - Loaded via CDN for utility-first styling
- **Vanilla JavaScript** - For interactions and animations
- **Iconify** - Loaded via CDN for icons
- **Google Fonts** - Inter (body text) and JetBrains Mono (terminal/code elements)

## Key Architecture Patterns

### Design System
- **Glass-morphism UI** - Translucent cards using `rgba()` backgrounds with `backdrop-filter: blur()`
- **Custom animations** - CSS keyframes for orbiting elements, floating effects, marquee scrolling, and pie charts
- **Dark theme** - Background: `#0A0A0A`, primary text: slate-300, accents: indigo

### Animation Types
The site heavily uses CSS keyframe animations:
- `orbit` / `orbit-reverse` - Circular orbital motion
- `float` - Gentle up/down floating
- `marquee-left` / `marquee-right` - Infinite horizontal scrolling
- `logo-scroll` - Trust bar logo carousel (30s duration)
- `aura-chart-fill` - Animated pie chart SVG strokes
- `blink` - Terminal cursor effect

### File Structure
```
/
├── index.html           # Single-page site with embedded CSS/JS
├── assets/              # Client logos and team photos (JPEG/PNG)
├── attached_assets/     # Source files and page variants
└── replit.md           # Detailed project documentation
```

## Development Workflow

### Making Changes
1. Edit `index.html` directly - all HTML, CSS (`<style>` tags), and JS are embedded
2. Open in browser to preview (no build step needed)
3. Refresh to see changes

### Testing Locally
Simply open `index.html` in a browser. All dependencies load from CDN, so an internet connection is required for fonts, icons, and Tailwind.

### Deployment
This is a static site ready to deploy as-is to any static host (GitHub Pages, Netlify, Vercel, etc.). No build process required.

## Styling Approach

- **Tailwind utility classes** - Used directly in HTML for layout and responsive design
- **Custom CSS in `<style>` block** - For animations, glass-morphism effects, and component-specific styling
- **No CSS preprocessors** - Raw CSS only
- **Design tokens**:
  - Glass cards: `background: rgba(255, 255, 255, 0.03)` with `backdrop-filter: blur(10px)`
  - Borders: `rgba(255, 255, 255, 0.08)`
  - Selection: `bg-indigo-500/30`

## Important Considerations

### When Editing
- The HTML file is large (~89KB) - contains all content for the entire landing page
- Custom animations are defined in the `<style>` block at the top
- All sections use smooth scroll navigation (`scroll-smooth` class on `<html>`)
- Logo marquee duplicates logos for seamless infinite scroll (uses `aria-hidden` on duplicates)

### CDN Dependencies
All external resources load from CDN. If working offline:
- Tailwind CSS won't be available
- Icons won't render
- Fonts will fall back to system defaults

### Assets Directory
- `assets/` contains client logos (`trusted-logo-*.png`) and team member photos (JPEG files with names)
- Logos are used in the trust bar section with marquee animation
- Team photos appear to be for an about/team section

## Recent Changes (December 2024)

- Added trust bar section with 11 client logos in smooth marquee slider
- Implemented CSS keyframe animation for seamless infinite scrolling
- Accessibility improvements with `aria-hidden` on duplicate logos
