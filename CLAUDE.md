# RF Properties — Claude Code conventions

## What this project is

Static website for RF Properties, a property development and trades business in Dipton, County Durham. Single `index.html` — no framework, no build step, no Node.

## Stack

- Pure HTML/CSS/vanilla JS, all in `index.html`
- Google Fonts via CDN (Archivo Expanded, Hanken Grotesk, JetBrains Mono)
- No React, no bundler, no npm — keep it that way unless explicitly asked

## Design tokens (do not change without asking)

| Token | Value | Role |
|---|---|---|
| `--slate` | `#1e2a35` | Dark navy — backgrounds, nav, footer |
| `--plaster` | `#f0ece4` | Warm off-white — page background |
| `--steel` | `#5c7a8a` | Mid blue-grey — accents, focus |
| `--oak` | `#a07b50` | Warm tan — primary brand colour, CTAs |
| `--white` | `#ffffff` | Cards, form backgrounds |

Fonts: **Archivo Expanded** (headings, bold), **Hanken Grotesk** (body), **JetBrains Mono** (labels/mono).

Scaffold-joint corner motif: used on `.service-card`, `.motif-card` — two-line corner markers in oak colour.

## Placeholders still to fill (Phase 1)

- `PLACEHOLDER_PHONE` — phone number
- `PLACEHOLDER NAME` — both owners' names (team section)
- `PLACEHOLDER —` — bio lines in team cards
- `hello@rfproperties.co.uk` — confirm or replace
- `PLACEHOLDER_FORM_ENDPOINT` — Formspree/Web3Forms endpoint (Phase 3)
- Gallery items — 3 placeholder cards awaiting real photos (Phase 4)
- Social links — commented out in footer, uncomment when provided (Phase 1)

## Key sections (IDs in index.html)

- `#hero` — headline, sub, CTA buttons, scaffold motif cards
- `#quote-bar` — oak CTA bar; "Click for a Quote" button opens `#quote-modal`
- `#services` — 4 service cards
- `#work` — gallery (`.gallery-item` cards)
- `#about` — about text + two `.team-card` elements
- `#area` — coverage towns as `.area-tag` pills
- `#contact` — contact details + `#contact-form`
- `#quote-modal` — popup triggered by quote buttons; shows `assets/img/Ryan.png`

## Quote modal

The "Click for a Quote" button (in `#quote-bar`) and the "Get a free quote" hero button both trigger `openQuoteModal()`. The modal shows `assets/img/Ryan.png`. Place `Ryan.png` in that path — if absent, the `<img>` hides itself via `onerror`.

## Contact form

Currently falls back to `mailto:` if `PLACEHOLDER_FORM_ENDPOINT` hasn't been replaced. Phase 3 will swap in a real static-form endpoint. Includes a honeypot field (`.hp-field`) for basic spam protection.

## Accessibility requirements

- All interactive elements keyboard-accessible
- `aria-label` on icon-only elements
- `role="alert"` on form messages
- Focus style via `:focus-visible` with oak outline
- `alt` text on all images

## Do not

- Add React, Vue, or any JS framework
- Add analytics or cookie banners unless asked
- Add a backend or server-side code
- Inline base64 images (put files in `assets/img/`)
- Change the colour palette without explicit agreement
