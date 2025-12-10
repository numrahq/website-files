# Numra - AI Agents for Finance Operations

## Overview

Numra is a static landing page for an AI-powered finance operations platform. The project is a single-page marketing website built with vanilla HTML, CSS, and JavaScript, utilizing CDN-based dependencies for styling and icons. The site showcases AI agent capabilities for finance operations with animated visual elements and a modern glass-morphism design aesthetic.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture

**Technology Stack:**
- Pure HTML5 with no build system or framework
- Tailwind CSS (loaded via CDN) for utility-first styling
- Vanilla JavaScript for interactions and animations
- Iconify (loaded via CDN) for icon components

**Design Patterns:**
- Single-page application structure with smooth scroll navigation
- Glass-morphism UI design with translucent card components
- CSS keyframe animations for visual effects (orbiting elements, floating animations, marquee scrolling)
- Custom typography using Google Fonts (Inter for body text, JetBrains Mono for code/terminal elements)

**Key UI Components:**
- Glass cards with backdrop blur effects
- Terminal-style cursor animations
- Orbital and floating animations for hero sections
- Marquee animations for scrolling content rows
- Pie chart animations with SVG stroke manipulation

### File Structure

The project follows a minimal structure:
- `index.html` - Main landing page with all content and styles
- `assets/` - Directory containing client logo images for the trust bar
- `attached_assets/` - Directory containing source files and generated page variants

### Recent Changes (December 2024)

- Added trust bar section with 11 client logos in a smooth marquee slider
- Implemented CSS keyframe animation for seamless infinite scrolling
- Added accessibility improvements with aria-hidden on duplicate logos

### Styling Approach

Custom CSS is embedded within `<style>` tags in the HTML head, defining:
- Animation keyframes for complex visual effects
- Glass-morphism card styling with rgba backgrounds and backdrop-filter
- Custom scrollbar and summary element styling
- Responsive marquee row animations

## External Dependencies

### CDN-Loaded Resources

| Dependency | Purpose | Source |
|------------|---------|--------|
| Tailwind CSS | Utility-first CSS framework | cdn.tailwindcss.com |
| Iconify | Icon library | code.iconify.design |
| Google Fonts (Inter) | Primary body font | fonts.googleapis.com |
| Google Fonts (JetBrains Mono) | Monospace/terminal font | fonts.googleapis.com |

### No Backend Dependencies

This is a purely static site with no:
- Server-side processing
- Database connections
- API integrations
- Authentication systems
- Build tools or package managers

### Deployment Considerations

The site can be served from any static file host. No compilation or build step is required - files are ready to serve as-is.