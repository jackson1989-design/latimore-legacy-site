# CLAUDE.md - AI Assistant Guide for Latimore Life & Legacy Site

## Project Overview

Static HTML website for **Latimore Life & Legacy LLC**, an independent insurance agency based in Schuylkill Haven, Pennsylvania. Founded by Jackson Latimore, the agency serves families and small business owners in Schuylkill, Luzerne, and Northumberland counties with life insurance, annuities, and financial planning services.

## Tech Stack

- **Type:** Static HTML5 website (no framework, no build tools, no JavaScript)
- **Styling:** External CSS via `assets/css/style.css` (referenced but not yet created)
- **Hosting:** No backend; pure static files
- **Version Control:** Git

## Repository Structure

```
latimore-legacy-site/
├── CLAUDE.md          # This file - AI assistant guide
├── index.html         # Homepage / landing page
├── about.html         # About Jackson Latimore & company mission
├── services.html      # Service offerings (families & businesses)
└── education.html     # Education hub / resource center
```

### Pages Not Yet Created (referenced in navigation)

- `contact.html` - Contact form / CTA destination
- `why.html` - "Why Choose Us" page

### Assets Not Yet Created

- `assets/css/style.css` - Main stylesheet (linked by all pages)
- Downloadable resources referenced in `education.html` (checklists, worksheets, guides)
- Favicon, images, and media assets

## File Descriptions

| File | Purpose | Key Content |
|------|---------|-------------|
| `index.html` | Homepage | Hero section, service pillars preview (3 cards), testimonials, trusted partners list |
| `about.html` | About page | Jackson's background, credentials, company mission and values |
| `services.html` | Services page | 4 family service cards (IUL, Annuities, Term/Whole Life, Legacy Planning) + 3 business service cards (Key Person, Succession, Retirement Benefits) |
| `education.html` | Education hub | 4 educational topic cards, 3 downloadable resource placeholders |

## Code Conventions

### HTML Structure

- All pages use HTML5 doctype with `lang="en"` and viewport meta tag
- Each page includes an SEO-focused `<meta name="description">` tag
- Only `index.html` has a `<meta name="keywords">` tag; other pages omit it
- Semantic HTML5 elements: `<header>`, `<nav>`, `<section>`, `<footer>`
- Consistent header/nav/footer structure across all pages
- Active page indicated by `class="active"` on the corresponding `<nav>` link

### CSS Class Naming

Classes follow a descriptive, component-based pattern (not BEM, closer to Bootstrap conventions):

- Layout: `.hero`, `.hero-content`, `.services-grid`
- Components: `.service-card`, `.testimonial`, `.author`, `.logo`
- Interactive: `.btn-primary`, `.active`

Note: `about.html` and `education.html` sections use plain `<section>` tags without classes. The education page reuses `.services-grid` and `.service-card` for its topic cards.

### Navigation Menu (6 items)

```
Home | About | Services | Education | Why Choose Us | Contact
```

The nav appears in the same order on every page. Mark the current page with `class="active"`.

Note: `index.html` does NOT currently set `class="active"` on the Home link, while `about.html`, `services.html`, and `education.html` do mark their respective links. This is an inconsistency in the existing code.

### Footer Pattern

Every page footer contains:
1. Social media links (LinkedIn, Facebook) - URLs not yet configured
2. Licensing info: PA DOI License #1268820, NIPR #21638507
3. Copyright: 2026 Latimore Life & Legacy LLC

## Business Context for Content

- **Tone:** Professional, educational, consultative - never aggressive sales language
- **Audience:** Families and small business owners in post-industrial PA communities
- **Brand promise:** Breaking generational cycles of financial vulnerability; building lasting legacies
- **Carrier partners:** American General Life, North American Company, F&G, American Equity, Ethos Life
- **Differentiators:** First-generation professional, local community roots, transparency, education-first approach

## Development Workflow

### No Build Step

This is a static site. Files are served as-is. No compilation, bundling, or preprocessing is needed.

### Git Conventions

- Commit messages should be descriptive of what was created or changed
- The repo uses a simple linear history
- Branch naming: feature branches prefixed with `claude/`

### Adding New Pages

When creating a new HTML page:
1. Copy the `<head>` section from an existing page (doctype, charset, viewport, stylesheet link)
2. Update `<title>` and `<meta name="description">` for the new page
3. Include the full navigation menu; set `class="active"` on the correct link
4. Include the standard footer with social links, licensing, and copyright
5. Link the new page from navigation in ALL existing pages

### Modifying Existing Pages

- Maintain the existing semantic HTML structure
- Keep meta descriptions relevant and keyword-rich
- Preserve licensing information in footers - this is legally required
- Do not remove or alter carrier partner references without explicit instruction

## Known Issues / Incomplete Items

1. **No CSS exists yet** - `assets/css/style.css` is referenced everywhere but not created
2. **Missing pages** - `contact.html` and `why.html` are linked but don't exist
3. **Placeholder links** - Education "Read More" links and resource downloads point to `#`
4. **Social media URLs** - Footer social links point to generic `https://www.linkedin.com/` and `https://www.facebook.com/` (need real profile URLs)
5. **No images/favicon** - No visual assets exist in the repo
6. **No `.gitignore`** - Should be added if tooling or dependencies are introduced
7. **Stray text in services.html** - Line 1 contains `services.html` before the `<!DOCTYPE html>` declaration; this should be removed
8. **Missing active class on index.html** - Home nav link lacks `class="active"` unlike other pages
