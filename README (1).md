# AI Engineer Portfolio v4 — Premium Cinematic Edition

Ultra-premium dark portfolio with Tesla AI / OpenAI-grade aesthetics. Single HTML file, zero dependencies, free to deploy anywhere.

---

## Quick Start (3 Ways)

### Option 1: Direct Open
Double-click `index.html` in your browser. Everything works offline.

### Option 2: Python Server
```bash
cd portfolio
python3 -m http.server 8000
# Open http://localhost:8000
```

### Option 3: Node Server
```bash
npx serve portfolio
# Open http://localhost:3000
```

---

## What's Inside

| Feature | Details |
|---|---|
| **Design** | Tesla AI / OpenAI inspired dark cinematic theme |
| **3D Effects** | 5-layer parallax star field, volumetric nebulae, perspective grid floor, mouse-reactive depth layer |
| **Hero** | Isometric 3D coding workstation — monitor with live typing code, person silhouette, orbital rings with depth particles, hologram cards with scanlines, perspective grid floor, floating code glyphs |
| **About** | Advanced neural network canvas (60 nodes with gradient connections, data pulses, layered glow) |
| **Skills** | 3 glass cards with gradient border reveal, animated skill bars with glowing endpoints |
| **Projects** | 5 featured projects with alternating layout, particle network canvas backgrounds, ghost numbering |
| **Timeline** | Left-aligned vertical with gradient line, glowing dots with radial pulse on hover |
| **Certs** | Glass cards with top-light border reveal and radial hover glow |
| **Interests** | 4 cards with bottom-glow, icon scale animation |
| **Contact** | Split layout — info + glass form with glow-focus inputs |
| **Footer** | "Thank You" with multi-color gradient text, rising particle canvas |
| **Admin** | Full CRUD dashboard (Ctrl+Shift+A) |
| **Animations** | Blur-to-focus reveal system, scroll-triggered counters, staggered delays, smooth cursor orb |
| **Typography** | Clash Display + Cabinet Grotesk + JetBrains Mono |
| **Responsive** | Full mobile support with hamburger nav overlay |

---

## File Structure

```
portfolio/
  index.html      ← Everything (HTML + CSS + JS) in one file
  README.md       ← This file
```

---

## Customization Guide

### 1. Personal Info
Search and replace in `index.html`:

```
"Your Name Here"  → Your actual name
"you@email.com"   → Your email
"github.com"      → Your GitHub URL
"linkedin.com"    → Your LinkedIn URL
"twitter.com"     → Your Twitter/X URL
```

### 2. About Section
Find the `<section id="about">` block and edit:
- Heading text in `<h3>`
- Both `<p>` paragraphs
- Tags in `.ab-tags`
- Metric counts: change `data-count="15"`, `data-count="5"`, `data-count="3"`

### 3. Skills
Find the `<section id="skills">` block. Each skill bar looks like:
```html
<div class="sk-r">
  <span class="sk-n">Python</span>
  <div class="sk-tr"><div class="sk-f c1" data-w="95"></div></div>
  <span class="sk-p">95%</span>
</div>
```
Change the skill name, `data-w` value (0-100), and percentage text.

### 4. Projects (Data Object)
Find `const D={projects:[...]}` in the `<script>` tag. Each project:
```javascript
{
  id: 1,
  title: "Your Project Title",
  desc: "Project description here.",
  tags: ["Python", "React", "Docker"],
  demo: "https://demo-url.com",
  github: "https://github.com/you/repo",
  featured: true    // shows on main page
}
```

### 5. Colors
Change CSS variables in `:root`:
```css
--ac: #00e5ff;    /* Primary accent (cyan) */
--ac2: #7c5cfc;   /* Secondary accent (purple) */
--ac3: #ff6b3d;   /* Tertiary accent (orange) */
```

### 6. Resume Link
Find the Resume button in the hero section and change `href="#"` to your resume PDF URL.

---

## Admin Panel

### Access
Press **Ctrl + Shift + A** (or Cmd + Shift + A on Mac)

### Default Credentials
- Username: `admin`
- Password: `portfolio2026`

### Change Credentials
Find this line in the script:
```javascript
const CR={u:'admin',p:'portfolio2026'};
```
Change `u` and `p` values.

### What You Can Do
- **Projects tab**: Add / Delete / Toggle Featured
- **Certs tab**: Add / Delete certifications
- **Plans tab**: Add / Delete timeline items
- **About tab**: Instructions for editing About section

All changes save to `localStorage` and persist across page reloads. Clearing browser data resets to defaults.

---

## Deployment (Free — Pick One)

### Method 1: Netlify (Easiest — Drag & Drop)

1. Go to [app.netlify.com](https://app.netlify.com)
2. Sign up with GitHub/email
3. Click **"Add new site"** → **"Deploy manually"**
4. Drag your `portfolio` folder into the drop zone
5. Wait 10 seconds — your site is live at `random-name.netlify.app`
6. Click **"Domain settings"** → **"Edit site name"** to customize URL

**Custom domain (optional)**:
- Go to **Domain management** → **Add custom domain**
- Add CNAME record at your domain registrar pointing to Netlify

### Method 2: Vercel (Via GitHub)

1. Push your `portfolio` folder to a GitHub repository
2. Go to [vercel.com](https://vercel.com) → Sign up with GitHub
3. Click **"Add New"** → **"Project"**
4. Import your repo
5. Framework Preset: **"Other"**
6. Click **"Deploy"**
7. Live at `your-repo.vercel.app`

### Method 3: GitHub Pages (Direct from Repo)

1. Create a GitHub repo (e.g., `my-portfolio`)
2. Push files:
```bash
git init
git add .
git commit -m "Portfolio v4"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/my-portfolio.git
git push -u origin main
```
3. Go to repo → **Settings** → **Pages**
4. Source: **Deploy from a branch**
5. Branch: **main** → Folder: **/ (root)**
6. Click **Save**
7. Live at `your-username.github.io/my-portfolio`

### Method 4: Cloudflare Pages

1. Push to GitHub (same as Method 3 step 1-2)
2. Go to [dash.cloudflare.com](https://dash.cloudflare.com) → **Workers & Pages**
3. Click **"Create application"** → **"Pages"** → **"Connect to Git"**
4. Select your repo
5. Build settings: leave blank (static site)
6. Click **"Save and Deploy"**
7. Live at `your-repo.pages.dev`

---

## Testing Checklist

### Visual Tests
- [ ] Page loads with loader animation (2.4s)
- [ ] Background star field animates with parallax on scroll
- [ ] Stars react to mouse movement (parallax depth effect)
- [ ] Cursor orb follows mouse with smooth delay
- [ ] Depth layer shifts subtly with mouse position
- [ ] Scroll progress bar appears at top with gradient glow
- [ ] Shooting stars appear randomly
- [ ] Grid dividers have animated light pulse

### Navigation
- [ ] Pill nav is centered, semi-transparent with blur
- [ ] Nav background darkens on scroll
- [ ] Active section highlights in nav
- [ ] All nav links scroll smoothly to sections
- [ ] Mobile: hamburger menu opens full-screen overlay
- [ ] Mobile: links close overlay on click

### Hero Section
- [ ] Badge pulses with green dot animation
- [ ] Name has animated gradient text
- [ ] Canvas shows monitor with live typing code + cursor blink
- [ ] Person silhouette with typing arm animation
- [ ] 3 orbital rings with depth-faded particles
- [ ] 12 orbiting data nodes with connection pulses
- [ ] 4 floating hologram cards with scanline effect
- [ ] Perspective grid floor at bottom
- [ ] Code glyphs float and fade by distance
- [ ] Resume button has shine sweep on hover
- [ ] Social icons lift and glow on hover

### About Section
- [ ] Neural network canvas with 60 animated nodes
- [ ] Nodes have gradient connections and layered glow
- [ ] Stat counters animate up when scrolled into view
- [ ] Metric cards have top-glow and radial hover effect
- [ ] Tags lift and glow cyan on hover

### Skills Section
- [ ] 3 cards with gradient border reveal on hover
- [ ] Cards lift with deep shadow on hover
- [ ] Icons scale + rotate slightly on card hover
- [ ] Skill bars animate width when scrolled into view
- [ ] Glowing dot appears at bar endpoint after fill

### Projects Section
- [ ] 5 cards with alternating text/visual layout
- [ ] Even cards reverse direction (RTL)
- [ ] Particle network canvas in each visual area
- [ ] Ghost numbers (01-05) in card body
- [ ] Gradient border reveal on hover
- [ ] Tags brighten on card hover
- [ ] Links shift right and glow on hover

### Timeline
- [ ] Vertical gradient line with subtle glow
- [ ] Dots pulse with radial glow on hover
- [ ] Year labels in monospace cyan
- [ ] Content reveals with scroll animation

### Certifications
- [ ] Cards with top-line gradient reveal on hover
- [ ] Radial glow sweeps from corner on hover
- [ ] Shield icons scale and glow on hover

### Interests
- [ ] Cards with bottom-line gradient reveal
- [ ] Icons scale to 1.15x with purple glow on hover
- [ ] Radial glow rises from bottom

### Contact
- [ ] Split layout: info left, form right
- [ ] Contact links shift right on hover
- [ ] Form inputs glow cyan with shadow on focus
- [ ] Send button has shine sweep effect
- [ ] Form validates all fields before submit

### Footer
- [ ] "Thank You" text with animated gradient
- [ ] Rising particle canvas with 3 color types
- [ ] Bright particles have bloom glow

### Admin Panel
- [ ] Ctrl+Shift+A opens login overlay
- [ ] Login validates credentials
- [ ] Wrong password shows error
- [ ] Dashboard has 4 tabs: Projects, Certs, Plans, About
- [ ] Can add a new project
- [ ] Can delete a project
- [ ] Can toggle featured status
- [ ] Can add/delete certifications
- [ ] Can add/delete plans
- [ ] Changes persist after page reload
- [ ] Close button exits admin

### Responsive (Mobile)
- [ ] All sections stack vertically
- [ ] Hero: visual moves above text
- [ ] Skills: cards stack to 1 column
- [ ] Projects: full-width, no RTL alternation
- [ ] Contact: form below info
- [ ] No horizontal scroll
- [ ] Touch interactions work

### Performance
- [ ] 60fps canvas animations on desktop
- [ ] Smooth scrolling without jank
- [ ] All fonts load from CDN
- [ ] Total file size under 55KB

---

## What's New in v4

Compared to v3:
- **5-layer depth parallax** (was 4) with mouse-reactive movement
- **Perspective grid floor** in hero with CSS 3D transform
- **Depth layer div** that shifts with cursor for environmental parallax
- **Volumetric light cones** — dual warm/cool radial gradients in hero canvas
- **Data pulses** along neural connections and orbital node paths
- **Hologram scanlines** inside floating cards
- **Cross-spike diffraction** on bright stars
- **Blur-to-focus reveal** system (elements deblur as they enter viewport)
- **Gradient border reveal** on cards using mask-composite
- **Enhanced node rendering** — 3-layer glow (outer, mid, core) for all neural nodes
- **Deeper shadows** and more refined glassmorphism across all cards
- **Warmer color accents** with tricolor nebula system (cyan + purple + orange)

---

## Browser Support

| Browser | Status |
|---|---|
| Chrome 90+ | Full support |
| Firefox 90+ | Full support |
| Safari 15+ | Full support |
| Edge 90+ | Full support |
| Mobile Chrome | Full support |
| Mobile Safari | Full support |

---

## SEO Additions (Optional)

Add inside `<head>` for better discoverability:

```html
<meta property="og:title" content="Your Name — AI Engineer Portfolio">
<meta property="og:description" content="Building intelligent systems that bridge research and production.">
<meta property="og:image" content="https://your-domain.com/og-image.png">
<meta property="og:url" content="https://your-domain.com">
<meta name="twitter:card" content="summary_large_image">
<link rel="canonical" href="https://your-domain.com">
```

---

## Upgrade to Next.js (Optional)

For a full framework setup:

```bash
npx create-next-app@latest portfolio --typescript --tailwind
cd portfolio
# Move index.html content into app/page.tsx
# Split CSS into globals.css + Tailwind classes
# Convert Canvas animations to useEffect hooks
# Add API routes for contact form backend
npm run dev
```

---

**License**: MIT — Use freely for personal or commercial projects.
