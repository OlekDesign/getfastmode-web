# FastMode — Landing Page Context for Claude Code

## Mission of this document
This document gives Claude Code everything it needs to build the content and structure of the `getfastmode.app` marketing landing page. Do not invent features. Do not use language about restriction, dieting, or before/after body imagery. All copy must reflect the tone and science described below.

---

## Tech stack
- **Framework**: Astro (static, no SSR needed)
- **Fonts**: Bricolage Grotesque ExtraBold (headings) + Inter (body) — load via Google Fonts
- **Always light mode** — no dark mode
- **Colors**:
  - Background: `#FAFAFA`
  - Surface: `#FFFFFF`, `#F0F0F0` (surface-elevated)
  - Green accent (fat burn): `#4CAF7D`
  - Orange accent (peak burn): `#F5A623` (primary), `#FF6B35` (accent)
  - Text primary: `#0A0A0A`
  - Text secondary: `#606060`
  - Text tertiary: `#A0A0A0`
  - Border: `#E5E5E5`
- **No external UI libraries** — raw Astro + CSS
- **Images**: use placeholder `<div>` blocks with aspect ratios where app screenshots will go — label them clearly (e.g. `<!-- PLACEHOLDER: ring timer screenshot -->`)

---

## App overview
**FastMode** is an intermittent fasting tracker for iOS and Android.

**Core loop**: User starts a fast → ring timer shows elapsed time and current metabolic phase → phases advance automatically (Fat Burn at 12h, Peak Fat Burn at 16h) → fast ends → streak grows → weight is logged → progress is visible over time.

**Business model**: Freemium. The timer and streak are free. The "Over time" tab (historical charts, weight tracking) requires Pro. Subscriptions: $4.99/month or $34.99/year (7-day free trial on yearly).

**Platforms**: iOS (App Store) + Android (Google Play)

---

## Brand tone
- Motivational but grounded — not hype, not fad-diet
- Science-backed: references Harvard Health, metabolic science, Nobel-recognized autophagy (2016)
- Warm, close — like a knowledgeable friend, not a brand
- Never use: "diet", "restriction", "forbidden foods", "cheat day", before/after body imagery
- Frame IF as a lifestyle and habit, not a temporary fix
- Audience: health-conscious adults 25–50 who are tired of calorie counting and want something sustainable

---

## Page structure

Build the following sections in order:

---

### 1. NAV
- Logo: "FastMode" wordmark (text, Bricolage Grotesque)
- Right side: App Store button + Google Play button (text links or badges)
- Sticky, transparent with blur backdrop

---

### 2. HERO
**Goal**: Hook the visitor in 3 seconds. Communicate the core value. Drive to download.

**Headline** (H1, large, Bricolage Grotesque ExtraBold):
> You already fast every night.
> FastMode makes it count.

**Subheadline** (Inter, text-secondary):
> A smart intermittent fasting tracker that shows you exactly what's happening in your body — hour by hour. Free to start.

**CTAs**:
- Primary: "Download on the App Store" (black badge style)
- Secondary: "Get it on Google Play"

**Visual**: Full-width dark hero, large placeholder for app screenshot (ring timer, ideally mid-fast showing green Fat Burn phase)

```
<!-- PLACEHOLDER: hero app screenshot — ring timer in Fat Burn phase (green glow) -->
```

---

### 3. INSIGHT HOOK
**Goal**: The "aha moment" — mirror the onboarding step 17 insight that converts users.

**Headline**:
> Did you know you're already fasting right now?

**Body**:
> If your last meal was at 7pm and you woke up at 7am, you just completed a 12-hour fast. FastMode picks up right where you left off — and shows you what your body is doing while you sleep.

**Visual style**: Dark card, green accent border, simple and impactful — no images needed here.

---

### 4. HOW IT WORKS
**Goal**: Explain the core loop simply. 3 steps, visual and scannable.

**Headline**:
> Three phases. One ring. Total clarity.

**Steps**:

1. **Start your fast**
   Set your eating window once. FastMode does the rest — tracking your fast automatically from there.

2. **Watch your body shift gears**
   At 12 hours, you enter Fat Burn. At 16, Peak Fat Burn. Your ring timer changes color as you level up — no guessing required.

3. **Build the habit**
   Your streak grows every day you complete a fast. Miss a day? Streak Freeze has your back. No all-or-nothing pressure.

**Visual**: 3-column layout on desktop, stacked on mobile. Each step has an icon placeholder and a small app screenshot placeholder.

```
<!-- PLACEHOLDER: step 1 — eating window setup screen -->
<!-- PLACEHOLDER: step 2 — ring timer showing Fat Burn (green) and Peak Fat Burn (orange) -->
<!-- PLACEHOLDER: step 3 — streak calendar view -->
```

---

### 5. FEATURES
**Goal**: Showcase key differentiators without overwhelming. Cards layout.

**Headline**:
> Everything you need. Nothing you don't.

**Feature cards** (6 cards, 2–3 columns):

1. **Live Metabolic Phases**
   Your ring timer changes color as your fast deepens — Fasting → Fat Burn (12h) → Peak Fat Burn (16h). Know exactly where you are, always.

2. **Your Personal Goal Date**
   Enter your stats once. FastMode calculates a realistic goal date based on your body, pace, and fasting window. Not "a few months" — an actual date.

3. **Streak System**
   Build a daily fasting habit with visual streaks. The longer your streak, the more you want to protect it. Loss aversion as motivation.

4. **Streak Freeze**
   Life happens. Freeze your streak for one day without breaking it. FastMode knows real life isn't perfect — and it doesn't punish you for it.

5. **Weight Tracking & Trends** *(Pro)*
   Log your weight daily. Watch the trend line move toward your goal. Over time, the data tells a story that the scale alone never could.

6. **Smart Notifications**
   Get notified when you hit Fat Burn, when your eating window is closing, or when your streak is at risk at 11pm. Contextual, never spammy.

---

### 6. SCIENCE SECTION
**Goal**: Build credibility. Anchor FastMode in real science.

**Headline**:
> This isn't a trend. It's biology.

**Body**:
> Intermittent fasting triggers measurable metabolic changes — not theories, not influencer claims. After 12 hours without food, your body begins burning stored fat as its primary fuel. After 16 hours, it enters peak fat-burning mode and begins autophagy — the cellular cleanup process recognized by the Nobel Prize in 2016.
>
> FastMode shows you exactly when these thresholds happen. In real time. On your wrist.

**Pull stats** (3 cards):
- `12h` — When fat burn begins
- `16h` — When peak fat burn and autophagy kick in
- `Nobel 2016` — Autophagy research awarded the Nobel Prize in Physiology

**Source note** (small text, secondary color):
> Referenced from Harvard Health Publishing and peer-reviewed research on intermittent fasting and metabolic health.

---

### 7. PRICING / CTA
**Goal**: Remove friction. Make free feel like enough, Pro feel obvious.

**Headline**:
> Start free. Go deeper when you're ready.

**Two cards side by side**:

**Free**
- Ring timer
- Metabolic phases
- Streak tracking
- Streak Freeze
- Push notifications
- *Download free →*

**Pro** — $4.99/mo or $34.99/yr
- Everything in Free
- Full fasting history
- Weight tracking & trend charts
- Progress toward goal weight
- 7-day free trial on yearly plan
- *Start 7-day free trial →*

---

### 8. FINAL CTA
**Goal**: Last push to download before footer.

**Headline**:
> Your body already knows how to fast.
> FastMode just makes it visible.

**Subtext**:
> Free to download. Available on iPhone and Android.

**CTAs**: App Store + Google Play badges

---

### 9. FOOTER
- Logo wordmark
- Links: Privacy Policy · Terms of Use
- "© 2026 FastMode. All rights reserved."
- App Store + Google Play links (small)

---

## Copy rules for Claude Code
1. Never use "diet", "calorie restriction", "forbidden", "cheat"
2. Never reference specific weight loss numbers (e.g. "lose 10kg in 30 days")
3. Always frame IF as a lifestyle habit, not a quick fix
4. Science claims must stay within what's documented above (12h fat burn, 16h peak + autophagy, Harvard Health, Nobel 2016)
5. Tone is warm and confident — not aggressive, not salesy
6. CTAs should feel inviting, not pressured
7. Light mode only — white/near-white backgrounds, dark text

---

## Placeholder convention
Where app screenshots are needed, use this exact pattern so they're easy to find and replace:

```html
<div class="screenshot-placeholder" data-label="DESCRIPTION">
  <!-- SCREENSHOT: DESCRIPTION -->
</div>
```

Style placeholders as dark rounded rectangles with a subtle border and the label text centered inside.

---

## Files to create
- `src/pages/index.astro` — main landing page
- `src/layouts/Layout.astro` — base layout with fonts, meta, dark mode
- `src/styles/global.css` — CSS variables, resets, typography scale

## Do not create
- A blog (separate task)
- Any backend or API routes
- Any JavaScript framework components (pure Astro + CSS only)
