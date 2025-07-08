# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a Jekyll-based GitHub Pages website using the devAid theme, a responsive template designed for developers. The site serves as a personal portfolio/landing page for Alpharez.

## Common Build Commands

### Development
- **Local development**: `bundle exec jekyll serve`
- **Install dependencies**: `bundle install`
- **Build site**: `bundle exec jekyll build`

### Deployment
- **GitHub Pages**: Automatic deployment on push to master branch
- **Manual build**: `jekyll build` (outputs to `_site/`)

## Architecture Overview

### Jekyll Structure
- **Layouts**: `_layouts/` - Main templates (default.html, page.html, blog.html)
- **Includes**: `_includes/` - Reusable components (header, footer, navigation sections)
- **Posts**: `_posts/` - Blog posts in Markdown format
- **Pages**: Root-level `.html` and `.markdown` files

### Theme Architecture
Uses the devAid theme with a single-page application structure:
- **Main layout**: `_layouts/default.html` includes all page sections
- **Sectioned content**: Each section is a separate include file:
  - `promo.html` - Hero section
  - `about.html` - About section  
  - `features.html` - Features showcase
  - `docs.html` - Documentation section
  - `contact.html` - Contact form

### CSS/Styling
- **LESS compilation**: Source files in `public/less/` with theme variants
- **Compiled CSS**: Output in `public/css/` (styles.css, styles-2.css, etc.)
- **Theme system**: Multiple theme variants (default, theme-2, theme-3, theme-4)
- **Responsive design**: Bootstrap-based with custom responsive breakpoints

### Static Assets
- **JavaScript**: Custom scripts in `public/js/` with minification
- **Third-party libraries**: Bootstrap, jQuery, Font Awesome, Prism syntax highlighting
- **Images**: Profile images and theme assets in `public/images/`

## Configuration

### Site Settings (_config.yml)
- **Title**: Alpharez
- **Email**: steve.clement@alpharez.com
- **Theme**: minima (Jekyll default)
- **Plugins**: jekyll-feed

### Dependencies (Gemfile)
- **Jekyll**: ~> 4.2.0
- **Theme**: minima ~> 2.5
- **Plugins**: jekyll-feed ~> 0.12

## Development Notes

### Content Management
- Blog posts follow Jekyll naming convention: `YYYY-MM-DD-title.markdown`
- Pages use YAML front matter for metadata
- Navigation is generated from `site.widgets` configuration

### Custom Features
- Single-page scrolling navigation
- Theme switching capability (4 theme variants)
- Responsive mobile navigation
- Social media integration placeholders
- Contact form integration ready

### Known TODOs
Based on TODO.md, planned improvements include:
- SEO meta tags integration
- Jekyll SEO plugin integration
- Snipcart e-commerce integration
- Rich snippets implementation
- XML sitemap generation