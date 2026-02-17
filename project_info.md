# Personal Portfolio Website - Project Info

## Overview
This is a personal portfolio website for Joe Lagasse, a Senior Firmware Engineer with 7+ years of experience in embedded systems, electro-optics, and soldier systems. The site showcases professional experience, technical skills, and project work in a clean, modern interface.

## Tech Stack
- **Pure HTML/CSS/JavaScript** - No frameworks or build tools
- **Static site** - Simple hosting, fast loading
- **Responsive design** - Mobile-first approach with breakpoints at 768px and 480px
- **Vanilla JS** - No dependencies, lightweight DOM manipulation

## Design Philosophy
**Dark Terminal Aesthetic:**
- Dark background (#09090b) with light text (#e4e4e7)
- Cyan accent color (#22d3ee) for interactive elements and highlights
- Monospace font (JetBrains Mono) for technical feel
- Terminal-inspired elements (prompts, cursor, window chrome)
- Smooth transitions and fade-in animations
- Clean, minimalist layout with consistent spacing

## Key Sections & Features

### 1. Hero Section
- Terminal window with animated cursor
- Quick snapshot: title, experience, core technologies
- Clean, impactful first impression

### 2. Company Carousel (NEW)
- **Purpose:** Showcase component manufacturers worked with (7 companies)
- **Companies:** STMicroelectronics, Microchip, Texas Instruments, Onsemi, IC-Haus, Excelitas, Monolithic Power Systems
- **Design:** Infinite auto-scroll ticker with hover-to-pause
- **Features:**
  - Bold title (2rem) and cyan subtitle
  - Grayscale logos that colorize on hover
  - 4 stat metrics below: Product Architectures, Component Integrations, Protocols, Years Experience
  - Fully responsive with adjusted scroll speed on mobile

### 3. About Me Section
- **Recent Update:** Completely rewritten for conciseness and impact
- **Tone:** Professional but personal, emphasizes problem-solving passion
- **Content:** Career journey from UNH IOL → Wilcox Industries → R&D
- **Key phrase:** "I thrive on unsolved problems"
- Includes headshot photo and links to UNH IOL and Wilcox Industries

### 4. Experience Section
- **Condensed with "Show More" functionality**
- Initially shows 3 key bullet points per position
- Expandable to full details via button toggle
- Two positions: Wilcox Industries (current) and UNH IOL

### 5. Skills Section
- **Condensed with "Show More" functionality**
- 4 skill categories: Expertise, Component Knowledge, Peripheral Knowledge, Languages/Software
- Initially shows top 5 items per category
- Expandable to full list (60+ total skills)
- Tag-based visual design with cyan accents

### 6. Projects Section
- Grid of project cards
- Each card has title, description, tech tags, and GitHub link
- Hover effects for interactivity

### 7. Education & Certifications
- Side-by-side cards for education and certifications
- University of New Hampshire - BS Computer Science
- Relevant certifications listed

### 8. Contact Section
- Email and LinkedIn links
- Centered, clean layout
- Call-to-action for collaboration

## Recent Improvements

### Carousel Enhancement (Latest)
- Increased title prominence from 0.9rem to 2rem
- Changed subtitle to cyan accent color
- Better visual hierarchy and spacing
- Added responsive mobile sizing

### About Me Rewrite
- Condensed from 4 long paragraphs to 4 punchy ones
- Stronger opening hook: "thrives on unsolved problems"
- More active voice and dynamic language
- Better reflects breadth: electro-optics, headborne platforms, testing fixtures
- Changed "headborne electro-optics" to "soldier systems"

### Skills & Experience Condensing
- Implemented collapsible sections with "Show More/Less" buttons
- Fixed toggle bug (was only targeting .hidden elements, now uses index-based logic)
- Top 5 skills visible initially, 3 experience bullets initially
- Smooth expand/collapse with proper state management

### Component Carousel Addition
- Created infinite scroll animation (30s loop, seamless with duplicated logos)
- Added SVG placeholder logos for 7 companies
- Grayscale filter with color-on-hover effect
- Stats section with 4 key metrics
- Changed title from "Trusted Component Partners" to "Component Experience"
- Updated stat from "15+ MCU Architectures" to "10+ Product Architectures"

## File Structure

```
z:\Apps\Personal_Website\
├── index.html                 # Main HTML file
├── css/
│   └── style.css             # All styles (700+ lines)
├── js/
│   └── main.js               # Interactive functionality
├── images/
│   ├── headshot.jpg          # Profile photo
│   └── logos/                # Company logos
│       ├── stm.svg
│       ├── microchip.svg
│       ├── ti.svg
│       ├── onsemi.svg
│       ├── ic-haus.svg
│       ├── excelitas.svg
│       ├── mps.svg
│       └── README.md         # Logo sourcing info
├── history.md                # Original bio content (source material)
├── Joseph_Lagasse_Resume_2025.docx  # Resume reference
└── project_info.md           # This file

```

## JavaScript Functionality

### Intersection Observer (Fade-in Animations)
- Elements with `.fade-in` class animate into view on scroll
- Smooth opacity and transform transitions
- Triggers once per element

### Show More/Less Toggles
- Handles both Skills and Experience sections
- Index-based hiding (first 5 for skills, first 3 for experience)
- Button text toggles between "Show More" and "Show Less"
- Targets all items regardless of current state (fixes initial bug)

### Carousel Auto-Scroll
- Pure CSS animation, no JS needed
- Infinite loop using duplicated logo set
- Pauses on hover (`:hover` with `animation-play-state: paused`)

## CSS Architecture

### Custom Properties (Variables)
- Color palette: bg-primary, bg-secondary, text-primary, text-secondary, accent, border
- Font families: font-mono (JetBrains Mono), font-sans (Inter)
- Consistent spacing and sizing

### Key Design Patterns
- Card-based layout with subtle borders and backgrounds
- Consistent padding: 24px on cards, 64px section spacing
- 0.3s transitions for smooth interactions
- Flex and grid layouts for responsive design
- Mobile-first media queries

## Current State

### ✅ Complete Features
- All core sections implemented and styled
- Responsive design working across devices
- Interactive elements (show/more, carousel, hover effects)
- Content fully updated and refined
- Accessibility considerations (semantic HTML, alt text, ARIA where needed)

### 📝 Content Status
- About Me: ✅ Rewritten and polished
- Experience: ✅ Condensed with key highlights
- Skills: ✅ Organized into categories with top items featured
- Projects: ✅ Showcase portfolio work
- Carousel: ✅ 7 companies featured with SVG placeholders

### 🎨 Design Status
- Terminal aesthetic: ✅ Consistent throughout
- Color scheme: ✅ Dark theme with cyan accents
- Typography: ✅ JetBrains Mono + Inter
- Spacing/layout: ✅ Clean and balanced
- Animations: ✅ Smooth and subtle

### 🔧 Technical Debt
- Logo SVGs are currently text-based placeholders - could replace with actual brand logos
- No analytics or tracking implemented
- No contact form (only email/LinkedIn links)
- Could add blog/writing section if desired

## Design Principles to Maintain

1. **Keep it simple** - No unnecessary complexity or over-engineering
2. **Terminal aesthetic** - Maintain dark theme, monospace font, cyan accents
3. **Performance first** - Static HTML, minimal JS, fast loading
4. **Mobile responsive** - Test all changes on mobile breakpoints
5. **Consistent spacing** - Use existing patterns (24px, 40px, 64px)
6. **Smooth interactions** - 0.3s transitions, subtle animations
7. **Content clarity** - Concise, impactful copy that showcases expertise

## Notes for Future Development

- If adding new sections, follow the existing `.section-title` pattern with section numbers
- For new interactive elements, use `.btn` or `.btn-outline` classes for consistency
- Maintain the fade-in animation pattern for new sections (add `.fade-in` class)
- Keep JavaScript vanilla - no frameworks needed for this simple site
- Test responsive design at 768px and 480px breakpoints
- Use the accent color (`--accent: #22d3ee`) sparingly for maximum impact

## Deployment
- Static site can be hosted on: GitHub Pages, Netlify, Vercel, or any web host
- No build step required - just upload files
- Ensure proper MIME types for .svg files

---

**Last Updated:** February 2026
**Status:** Active development, fully functional
**Next Steps:** Consider replacing SVG logo placeholders with actual brand logos, potential analytics integration
