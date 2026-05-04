# Hartwell Construction Co. — Project Handoff

## File Location
- **Main file:** `/Users/tystr/Downloads/index.html`
- **Hero image:** `/Users/tystr/Downloads/hartwell-room.avif` (copied from `/Users/tystr/Documents/Business/Utopia Labs/Utopia Labs Website/Media/room example.avif`)
- **Local server:** `http://127.0.0.1:8765/index.html` (Python HTTP server — restart with `cd /Users/tystr/Downloads && python3 -m http.server 8765 --bind 127.0.0.1 &`)

---

## What Was Built
Single-file HTML landing page for a fictional home construction company called **Hartwell Construction Co.**

### Design System
- **Font:** Urbanist (Google Fonts) — weight 300 body, 500 headings
- **Palette:** Dark charcoal `#1C1C1C` background, white text, surfaces at `#2A2A2A` / `#333333`
- **No frameworks** — pure HTML/CSS with minimal vanilla JS (IntersectionObserver scroll reveals)
- **Skills used during build:** `high-end-visual-design`, `design-taste-frontend`

### Sections (top to bottom)
1. **Nav** — fixed full-width bar, transparent background (photo bleeds through on right), floating hairline bottom border, SVG logo mark (two offset squares), 5 links (Home active/bold, Services, About, Blog, Contact), white pill CTA "Get a Quote" on far right
2. **Hero** — true 50/50 split grid: left = dark bg + tagline + subtext + two buttons, right = full-height photo
3. **Services** — asymmetric zig-zag card grid (double-bezel cards), 4 services: Custom Homes (large), Renovations, Design-Build, Project Management (full-width strip)
4. **About strip** — 3 stats (38 years, 247 homes, 3 states) + description text
5. **Footer** — brand name, contact links, copyright

### Hero Buttons
- **Get a Quote:** white fill, dark `#1C1C1C` text, white border, uppercase
- **Learn More:** transparent, solid white border, white text, uppercase
- Both identical size: `padding: 15px 28px`, no arrow

---

## Key Design Decisions / Rules
- Nav is transparent so hero photo bleeds through on the right side
- Nav bottom border: `height: 0.75px; background: #FFFFFF` — floating (inset 64px from edges via `::after` pseudo-element)
- Cards use double-bezel architecture (outer shell + inner core)
- No gradients/fades on photo edges — hard clean cut between dark bg and photo
- Hero grid: `grid-template-columns: 1fr 1fr` (true 50/50)
- Nav height: `78px`
- "Home" nav link has class `nav-active` (font-weight 600, full white)
- Grain overlay on body via CSS SVG feTurbulence (fixed, pointer-events-none, opacity 0.028)
- **`.nav-left` width: `50%`** — this constrains the logo + nav links to the left (dark) half of the screen exactly, since the nav has symmetric 64px padding and the hero is a 50/50 split

### Hero Photo — Current State ✅
- **File:** `hartwell-room.avif` (served locally, same folder as index.html)
- **Source:** `/Users/tystr/Documents/Business/Utopia Labs/Utopia Labs Website/Media/room example.avif`
- **Filter:** `grayscale(0.15) contrast(0.95) brightness(0.95)`, hover reveals full color
- **object-position:** `center center`
- The image is a warm industrial/rustic interior — user-selected and confirmed as looking great

---

## Current Status
The page is complete and the user is happy with how it looks. Possible next steps to explore:
- Mobile responsiveness (nav collapses, hero stacks vertically)
- Scroll-triggered counter animation on the About stats
- Real contact form or CTA modal for "Get a Quote"
- Adding a Portfolio/Projects section with photo cards
- Deploying to a real host (Netlify, Vercel, etc.)

---

## Continuation Prompt (paste into a new Claude window)

```
Read /Users/tystr/Downloads/hartwell-handoff.md and pick up where the previous session left off. The Hartwell Construction Co. landing page lives at /Users/tystr/Downloads/index.html and is served locally at http://127.0.0.1:8765/index.html (restart the Python server if needed: cd /Users/tystr/Downloads && python3 -m http.server 8765 --bind 127.0.0.1 &).

The page is in a good state — hero image is set, nav links are positioned correctly within the dark half of the screen. Continue with whatever the user asks next.
```
