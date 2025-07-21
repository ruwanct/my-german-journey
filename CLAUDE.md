# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview
This is a static HTML/CSS website for a German A2 language learning journey. The project tracks weekly German grammar lessons with detailed content and quick summary pages for each week.

## Architecture & Structure

### Site Structure
- **Main landing page**: `index.html` - Weekly progress overview with 10-week curriculum
- **Week content**: Each week has a dedicated folder (e.g., `week01/`, `week02/`) containing:
  - `index.html` - Full detailed lesson
  - `summary.html` - Quick reference notes
- **Shared styles**: `css/styles.css` - Comprehensive CSS framework for all pages

### Key Design Patterns

#### Navigation System
- **Sticky navbar**: Present on all pages with breadcrumb navigation
- **Navigation buttons**: Home, lesson/summary toggle, and week navigation
- **Theme-based coloring**: Each week uses CSS custom properties for consistent theming

#### Content Styling Framework
The CSS includes a robust system of semantic classes:

**Content Blocks**:
- `.rule-box` - Important grammar rules (yellow background)
- `.structure-box` - Sentence patterns (monospace font)
- `.example-box` - Examples and practice (blue accent)
- `.success-box` - Correct answers and tips (green)
- `.warning-box` - Common mistakes (yellow warning)
- `.memory-box` - Mnemonics and memory aids

**Highlight System**:
- `.highlight-primary` (blue) - Main focus words
- `.highlight-secondary` (green) - Supporting words  
- `.highlight-accent` (orange) - Special cases
- `.highlight-warning` (red) - Mistakes to avoid
- `.highlight-success` (green) - Correct examples

**Layout Components**:
- `.two-column-grid`, `.three-column-grid`, `.auto-grid` - Responsive grids
- `.content-table` - Styled data tables with hover effects
- `.bottom-nav` - Page navigation with themed buttons

#### Week Theming
- Uses CSS custom properties (`--primary-color`) for week-specific colors
- Classes like `.week01-theme`, `.week02-theme` set the primary color
- Summary pages use `.summary-page` class for gradient backgrounds

## Development Guidelines

### Adding New Week Content
1. Create folder `week##/` with `index.html` and `summary.html`
2. Use appropriate week theme class (`.week##-theme`)
3. Follow existing navigation structure with breadcrumbs
4. Use semantic CSS classes for consistent styling
5. Update main `index.html` progress tracking

### Content Styling
- Use the established highlight system for semantic meaning
- Employ content blocks (rule-box, example-box, etc.) for clear information hierarchy
- Tables should use `.content-table` class
- Responsive grids available for layout organization

### CSS Architecture
- Single CSS file approach with clear section organization
- Uses CSS custom properties for theming
- Mobile-first responsive design with `@media (max-width: 768px)`
- Print styles included for content export

### File Organization
- Keep all lesson content in respective week folders
- Shared assets in `css/` directory
- No build process - direct HTML/CSS development
- 404.html exists for error handling

## Deployment
This site is deployed on **GitHub Pages** and automatically serves from the repository. Any changes pushed to the main branch will be reflected on the live site.

## No Build Process
This is a static site with no package.json, build tools, or preprocessing. Direct HTML/CSS editing with browser refresh for development.