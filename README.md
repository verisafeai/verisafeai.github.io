# VeriSafe Website

Welcome to the VeriSafe homepage repository. This is a static website built with **Jekyll** showcasing VeriSafe's mission to make autonomous systems verifiably safe.

## 🎯 About VeriSafe

VeriSafe develops formally verified, safe autonomous decision-making systems for safety-critical applications in robotics, autonomous vehicles, healthcare, and telecommunications. This website presents VeriSafe's vision, solution, market opportunity, and team.

## 📋 Website Structure

The website is a single-page application with the following sections:

1. **Navigation** — Sticky header with logo and section links
2. **Hero** — Main value proposition with brand messaging
3. **Vision** — Three core pillars: Safe, Controllable, Verifiable
4. **Problem** — Current challenges in autonomous system deployment
5. **Solution** — VeriSafe's approach and key differentiators
6. **Industries** — Target markets and use cases
7. **Market** — Growth opportunity and market size
8. **Partners** — Organizations and funding bodies
9. **Team** — Founding team with bios
10. **Call to Action** — Investment and partnership opportunities
11. **Footer** — Contact and legal links

## 🛠️ Tech Stack

- **Jekyll** — Static site generator
- **CSS (SCSS)** — Custom design system with VeriSafe color palette
- **HTML5** — Semantic markup
- **Responsive Design** — Mobile-first approach (optimized for 375px - 1200px+)

## 🎨 Design

- **Color Palette**: VeriSafe Blue (#0080BD), Verified Teal (#0D9488), Deep Navy (#0A2E3F)
- **Typography**: Inter and Montserrat from Google Fonts
- **Assets**: 30 images extracted from pitch deck (optimized)

## 📁 Project Layout

```
.
├── index.html                 # Homepage (all sections in one file)
├── _config.yml                # Jekyll configuration (site title, baseurl, etc.)
├── _layouts/
│   └── default.html           # Main layout template
├── _includes/
│   └── head.html              # HTML head (meta, fonts, CSS, favicon)
├── css/
│   └── verisafe.css           # Complete design system (1318 lines)
├── assets_extracted/          # Extracted images from pitch deck
│   ├── README.md              # Asset documentation
│   └── [30 image files]
├── _posts/                    # Blog posts (not used in homepage)
├── js/                        # JavaScript (from original theme)
├── img/                       # Legacy images (not used)
└── README.md                  # This file
```

## 🚀 Local Deployment

### Prerequisites

- **Ruby** (version 2.6.0 or higher)
  - Check: `ruby --version`
  - Install: https://www.ruby-lang.org/en/documentation/installation/

- **Bundler** (Ruby package manager)
  - Check: `bundle --version`
  - Install: `gem install bundler`

- **Jekyll** (will be installed via Bundler)

### Quick Start

1. **Navigate to the project directory:**
   ```bash
   cd /Users/joshua/Coding/2026_06_verisafeai.github.io
   ```

2. **Install dependencies:**
   ```bash
   bundle install
   ```
   This reads the `Gemfile` and installs all required Ruby gems (Jekyll, etc.)

3. **Build the site:**
   ```bash
   bundle exec jekyll build
   ```
   This generates the static site in the `_site/` directory.

4. **Serve locally:**
   ```bash
   bundle exec jekyll serve
   ```
   The site will be available at: **http://localhost:4000**

5. **View the website:**
   - Open your browser and visit: `http://localhost:4000`
   - The homepage (`index.html`) will load automatically
   - Press `Ctrl+C` (or `Cmd+C` on Mac) to stop the local server

### Development Workflow

**Auto-rebuild on file changes:**
```bash
bundle exec jekyll serve --livereload
```
This automatically rebuilds the site when you edit HTML, CSS, or config files. Refresh your browser to see changes.

**Build only (no server):**
```bash
bundle exec jekyll build
```
Output will be in `_site/` directory.

## ✏️ Editing Content

### Update Site Metadata
Edit `_config.yml`:
- `title: VeriSafe` — Site title
- `email: joshua.wendland@rub.de` — Contact email
- `description:` — Site description (appears in meta tags)
- `url:` and `baseurl:` — For GitHub Pages deployment

### Update Homepage Content
Edit `index.html` to change:
- Section titles and text
- Image file paths (in `src` attributes)
- Colors (via CSS classes in `_layouts/default.html`)
- Links and CTAs

### Update Styles
Edit `css/verisafe.css` to modify:
- Color palette (`:root` CSS variables)
- Typography and spacing
- Layout and responsive breakpoints
- Component styles (buttons, cards, sections)

### Update Navigation
Edit `_layouts/default.html`:
- Logo and navigation links
- Sticky navigation behavior
- Mobile menu functionality

## 📊 Performance Optimization

Current assets:
- **Logo**: 1.4 MB (consider resizing to 128×128px for web use)
- **Problem GIF**: 2.8 MB (consider converting to WebP or static PNG)
- **Team photos**: 130-190 KB (good for web)
- **Industry icons**: 27-35 KB each (optimized)
- **Partner logos**: Varying sizes (7-400 KB)

**Tips for optimization:**
- Use ImageOptim or similar tools to compress PNG/JPG files
- Convert large GIFs to WebP or MP4 for better compression
- Use `srcset` for responsive images on retina displays
- Minimize CSS by removing unused classes

## 🌐 Deployment to GitHub Pages

Once ready to publish:

1. **Ensure `_config.yml` is correct:**
   ```yaml
   url: https://verisafe.github.io
   baseurl: ""  # or "/project-name/" if using a project repo
   ```

2. **Push to GitHub:**
   ```bash
   git add .
   git commit -m "Update website content"
   git push origin main
   ```

3. **Enable GitHub Pages:**
   - Go to repository Settings → Pages
   - Select "Deploy from a branch"
   - Choose `main` branch
   - Save

4. **Access your live site:**
   - https://verisafe.github.io (or your custom domain)

## 🔧 Troubleshooting

**Jekyll not found:**
```bash
gem install jekyll bundler
```

**Port 4000 already in use:**
```bash
bundle exec jekyll serve --port 4001
```

**Cache issues:**
```bash
rm -rf _site/
bundle exec jekyll clean
bundle exec jekyll serve
```

**CSS not loading:**
- Make sure `css/verisafe.css` exists
- Check `_includes/head.html` for correct CSS path
- Clear browser cache (Ctrl+Shift+Delete)

**Images not showing:**
- Check image paths in `index.html` (relative to repo root)
- Verify files exist in `assets_extracted/` or correct path
- Ensure filenames match exactly (case-sensitive on Linux/Mac)

## 📝 MEMORY.md

See `MEMORY.md` for project history, design decisions, and color palette reference.

## 📧 Contact

For questions about VeriSafe:
- Email: joshua.wendland@rub.de
- Website: www.verisafe.github.io

---

**Last updated:** June 23, 2026  
**Built with:** Jekyll, custom CSS, VeriSafe brand assets
