## Plan: Looser Line Spacing & Breathing Room

### Goal
Increase line spacing and overall vertical breathing room across the site so the layout no longer feels cramped.

### Changes

1. **Global body line-height** — Increase base `line-height` in `src/styles.css` from the browser default (~1.5) to `1.75` so all text inherits more generous spacing without touching every element individually.

2. **Paragraph blocks** — Update `space-y-6` / `space-y-8` clusters inside text blocks to `space-y-8` / `space-y-10` for more air between paragraphs.

3. **Section padding** — Bump section vertical padding from `py-24 md:py-32` to `py-28 md:py-36` to give each section more room to breathe.

4. **Headings** — Slightly relax heading `line-height` from `leading-tight` to a custom value (~1.15) so multi-line headlines don't feel squeezed.

5. **Card & list gaps** — Increase grid and flex gaps in Services, Process, and Who-I-Work-With sections by one step (e.g. `gap-6` → `gap-8`, `gap-10` → `gap-12`).

### Scope
Purely visual/CSS/utility changes inside `src/styles.css` and `src/routes/index.tsx`. No logic or content changes.

### Outcome
The page will feel more open and readable with airier text and wider section spacing throughout.