# Copilot Instructions - TerraEx Website

## Project Overview
Single-page static website for TerraEx, an excavation and earthmoving company. Built with HTML/CSS only - no JavaScript framework or build system required. Content is in Spanish (es-ES).

## Architecture & Key Patterns

### File Organization
- **index.html**: Single HTML file containing all page sections and semantic structure
- **style.css**: All styling (642 lines) - uses CSS custom properties for theming
- No JS, no build process, no dependencies

### Design System
- **Color Palette** (in CSS `:root`):
  - Primary: `#f59e0b` (amber/orange) with hover state `#d97706`
  - Text: `#1a1a1a` (dark), `#4b5563` (light gray)
  - Background: `#f9fafb` (off-white), `#ffffff` (white)
- **Typography**: Manrope font family (300, 400, 600, 700, 800 weights) from Google Fonts
- **Border radius**: 8px standard
- **Container max-width**: 1200px

### HTML Structure Conventions
- All sections use semantic HTML5 (`<header>`, `<section>`, `<article>`)
- Classes follow BEM-lite pattern: descriptive names like `.hero-overlay`, `.stat-item`, `.project-card`
- External images from Unsplash (free placeholder service)
- Company logo loads from garciamonterde.com
- Language attribute: `<html lang="es">`

## Page Sections (in order)
1. **Navbar** - Fixed header with logo and navigation links (HTML incomplete - nav-links not yet implemented)
2. **Hero Section** - 90vh height with background image and call-to-action buttons
3. **About Section** - Two-column grid with stats and company info
4. **Services** - Simple unordered list of service offerings
5. **History/Projects** - Grid of project cards showcasing past work

## CSS Structure
- Global reset and variables at top
- Sections organized by comment blocks: `/* HEADER / NAVEGACIÓN */` style
- Responsive breakpoints for mobile (`:hover` states for desktops)
- Fixed navbar with z-index 1000

## Important Implementation Notes
- **External Resources**: All images are external URLs (no local assets folder needed yet)
- **Links**: Most CTA links use `href="#"` - need actual targets later (`#servicios` is anchored, others aren't)
- **Navbar Incomplete**: `.nav-links` exists in CSS but not HTML yet - add when implementing full navigation
- **Language**: Maintain Spanish content (headings, buttons, alt text)

## Common Tasks
- **Update colors**: Edit `:root` CSS variables (line ~5 in style.css)
- **Change typography**: Modify Manrope font weights in Google Fonts link or CSS font-weight declarations
- **Add sections**: Follow existing pattern: wrap in `.section-padding` container, use `.container` for max-width
- **Add project cards**: Duplicate `.project-card` structure within `.projects-grid`
- **Mobile optimization**: Media queries not yet extensive - consider adding for small screens

## Workflow Notes
- No npm/build required - open `index.html` directly in browser
- CSS changes take immediate effect on save
- Keep HTML and CSS in sync - class names should match styling
- Test in browser at multiple viewport sizes (hero section responsive at 90vh)
