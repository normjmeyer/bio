# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static HTML personal resume/bio website for Norman Meyer, a Full Stack Software Engineer. The site is a single-page resume with no build process or dependencies.

## Architecture

- **Single-page static site**: `index.html` contains the entire resume content using semantic HTML5 elements
- **Styling**:
  - `application.css` contains custom CSS with modern features:
    - CSS custom properties (variables) for colors, spacing, and layout
    - CSS nesting syntax (not requiring a preprocessor)
    - `rem` units for accessibility (scales with user's browser font size)
- **Assets**: LinkedIn logo image stored in `assets/images/`

## File Structure

```
index.html          # Main resume page with semantic HTML sections
application.css     # Custom styles with layout and typography
assets/
  images/
    linkedin_logo.jpeg
```

## Content Sections

The resume is organized using semantic HTML5 elements in `index.html`:
1. `<header>` - Resume header with name and title
2. `<main>` - Main content wrapper containing:
   - `<section>` - Professional summary
   - `<section>` - Professional Experience
   - `<section>` - Technical Skills
   - `<section>` - Education (with expandable `<details>` elements for course certificates)

## Styling Architecture

The CSS uses modern best practices:
- **CSS Custom Properties (Variables)** defined in `:root`:
  - `--bg-section`, `--bg-main` for colors
  - `--spacing-xs`, `--spacing-sm`, `--spacing-md`, `--spacing-lg` for consistent spacing
  - `--max-content-width` for layout
- **Rem units** throughout for accessibility (allows scaling with user's browser font size)
- **CSS nesting syntax** (not requiring a preprocessor)
- **Flexbox** for layout (header, job titles)
- **Responsive design** with max-width and margin auto centering
- **Adjacent sibling selectors** for section backgrounds (`h1 + div`, `h1 + section`)
- **Custom classes** for specific components (`.job_title`, `.skill_name`, `.main_section_heading`)

## Development

This is a static site with no build process. To view:
1. Open `index.html` directly in a browser
2. Or serve with any static server (e.g., `python -m http.server`)
