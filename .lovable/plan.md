## Ettel Daskal — Portfolio Site

A hybrid site: a single-page landing for first-time visitors, plus dedicated case-study routes for anchor projects so you can show depth, not just links.

### Identity (blended)

- **Headline positioning:** "Educational storyteller and creative content developer for mission-driven organizations."
- **Tagline:** "Copy with heart."
- **Voice:** warm, first-person, articulate. Magazine/editorial — not corporate, not freelancery.
- **Primary CTA everywhere:** "Book a Free Call".

### Visual System

- **Palette (HSL shadcn tokens in `src/styles.css`):** primary `#1A3CC8`, secondary `#EFEAE4` (warm cream as page background), accent `#E8A53A`, deep ink foreground.
- **Type:** The Seasons (display headings, generous tracking) + Inter (body). Installed via `@fontsource`.
- **Style:** editorial magazine — wide margins, generous whitespace, 1px hairline borders (no drop shadows), soft 6–10px corners, balanced density, small-caps eyebrows, drop-cap intro on About.
- **Motion:** subtle hover lift on cards, hero typewriter on headline, respect `prefers-reduced-motion`.
- **No photos.** Lucide icons + CSS/SVG geometric shapes only, per brief.

### Sitemap

```text
/                          Landing (all sections, hash anchors)
/work                       All Work index (categorized grid)
/work/torah-nugget         Case study
/work/school-newsletter    Case study
/work/donor-gift-book      Case study (book-style layout)
/work/event-songs          Case study
```

### Landing page sections (`src/routes/index.tsx`)

1. **Sticky nav** — wordmark "Ettel Daskal" left; About / Work / Services / Contact right; accent "Book a Free Call".
2. **Hero** — split layout. Left: eyebrow ("Copy with heart"), large serif headline with typewriter effect cycling phrases ("Values-based." "Compassionate." "Mission-driven."), supporting line, primary CTA + secondary "See the work". Right: abstract editorial panel (cream + cobalt geometric SVG composition, no images).
3. **About** — first-person bio (2–3 paragraphs from your About intro, condensed). Three stat callouts verbatim: 12,500+ copies printed · $10,000 generated from one newsletter · 5 years teaching · BA in psychology (4 stats in a row, hairline-divided).
4. **What I do (Services)** — 4-card editorial grid blending brief services with your portfolio categories:
   - Educational Publishing & Curriculum
   - Donor & Organizational Storytelling
   - Website & Mission Copy
   - Creative Campaigns & Event Content
5. **Selected Work** — 4 anchor projects as magazine-style tiles (number + category eyebrow + title + one-line summary). Each tile links to its case study route. Tiles for items with Drive links also expose "View original ↗" opening in a new tab.
6. **Approach / Philosophy** — short editorial section pulling from your "core themes" (emotionally intelligent storytelling, audience sensitivity, research + accessibility).
7. **Testimonials** — full-bleed `bg-primary` section, large serif pull-quote treatment. **Will use your real quotes verbatim once you paste them**; until then placeholder cards with `// TODO`.
8. **Contact** — Name / Email / Service (dropdown) / Message. zod validation; on submit builds `mailto:etteldaskal@gmail.com` with subject "New website inquiry from {name}" and URL-encoded body. CTA: "Book a Free Call".
9. **Footer** — wordmark, email, simple nav.

### Case study template (per project route)

Each follows your structure exactly:

```text
eyebrow category · large serif title
Overview (1–2 sentences)
Objective
Audience
My Role
Approach
Outcome
Selected Samples — link cards opening Drive in new tab
← Back to all work | Book a Free Call
```

Four anchor case studies (drafted by me from your brief, then you edit):

- **Torah Nugget** (Educational Publishing) — 3 Drive sample links
- **School Community Newsletter** (Donor Storytelling) — 2 Drive samples; lead with the $10K organic-donations outcome
- **Donor Gift Book** (Donor Storytelling) — Drive folder; **book-style layout**: two-page spread mockup using CSS (centered spine, page-turn affordance on hover), large pull quotes
- **Event Songs / Creative Campaigns** — placeholder until you provide samples

### `/work` page

Three category bands (Educational Publishing · Donor & Organizational · Creative Campaigns & Event · Education & Curriculum) with case-study cards under each.

### Waiting on you before I build

1. **Reference design image** ("image of boy") — to derive layout rhythm.
2. **Logo / wordmark** (if you have one; otherwise I'll set type-only).
3. **Real testimonials** — quote, name, title/org.
4. **Any sample images/spreads** for the case studies (otherwise case studies render with type-only layouts + Drive links).
5. **Event Songs samples** (the brief left this empty).

### Technical notes

- TanStack Start v1, file-based routing under `src/routes/`. Landing on `index.tsx`; case studies under `src/routes/work.*.tsx`.
- Tailwind v4: tokens in `src/styles.css` under `@theme inline`. Fonts via `@fontsource/the-seasons` (or closest available; fall back to `@fontsource/cormorant-garamond` if The Seasons isn't on @fontsource — I'll confirm at install time) and `@fontsource-variable/inter`.
- One `head()` on the index route + per-route `head()` on each case study (unique title/description/og).
- Semantic HTML, single H1 per route, AA contrast, visible focus rings, alt text on every SVG.
- No backend; contact form is mailto-only.
- Drive links open in new tab with `rel="noopener noreferrer"`.

Reply with your uploads (or "skip") and your testimonials, and I'll build.
