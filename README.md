# Seams — support, terms and privacy

The public pages the App Store listing and the in-app paywall link to.
Plain static HTML, no build step, served by GitHub Pages.

- `index.html` — support and contact
- `terms.html` — Terms of Use
- `privacy.html` — Privacy Policy

The app links to `terms.html` and `privacy.html` from the subscription
screen; App Store Review requires both to be reachable from there. The URLs
are in `src/features/billing/paywall-view.tsx` — if this moves, they move.

**The privacy policy describes real data flows.** Before changing what the
app sends (`src/core/supabase/sync.ts`, `src/core/ai/coach.ts` and the
`analyze-session` function), change this with it. The key frames going to
the AI provider are the part most easily got wrong: the video never leaves
the phone, but stills of the athlete do.
