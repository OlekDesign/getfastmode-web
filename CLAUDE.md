# FastMode — getfastmode.app

## Project
Landing page for FastMode, an intermittent fasting tracker for iOS and Android. Built with Astro (static, no SSR). Light mode only.

## Stack
- Astro, pure CSS, no UI libraries
- Fonts: Bricolage Grotesque ExtraBold (headings) + Inter (body) via Google Fonts
- No JavaScript frameworks — vanilla JS only where needed
- Images: `<div class="screenshot-placeholder" data-label="...">` for app screenshots

## Key files
- `src/pages/index.astro` — main page
- `src/layouts/Layout.astro` — base layout with fonts
- `src/styles/global.css` — CSS variables, reset, typography
- `src/components/Nav.astro` — sticky nav with scroll blur
- `context/fastmode-landing-page-context.md` — full copy and section spec

## Design Context

### Users
Health-conscious adults 25–50 tired of calorie counting, wanting a sustainable lifestyle habit. Daily use — morning check-ins, commute. Curious about science, not obsessed with grind. Want to feel informed and in control, not pressured.

### Brand Personality
**Purposeful · warm · confident.** A knowledgeable friend who gets excited about the science and wants to share it. Not a coach yelling, not a meditation guru whispering — somewhere in between.

### Reference & Anti-Reference
- **Reference**: Headspace / Calm — smooth rhythm, organic feel, breathing space
- **Hard anti-ref**: Fitness/gym aggro, corporate SaaS (gradient hero, 3-col grid, testimonial avatars)
- **Soft anti-ref**: Generic health app (stock salads, pastel blob shapes)

### Design Principles
1. **Science as warmth** — data and facts are reassuring, not clinical
2. **Earn every pixel** — no decorative cards, no icon-above-heading grids, no filler
3. **Momentum over perfection** — interface conveys progress and forward motion
4. **Confident whitespace** — generous but never empty for its own sake
5. **Orange is scarce** — use primary accent for one thing per section max

### Colors
- Background: `#FAFAFA`, Surface: `#FFFFFF`, Border: `#E5E5E5`
- Text primary: `#0A0A0A`, secondary: `#606060`, tertiary: `#A0A0A0`
- Primary orange: `#F5A623`, Accent: `#FF6B35`, Fat Burn green: `#4CAF7D`
