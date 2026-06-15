# RF Properties Website

Static website for RF Properties — property development, joinery, scaffolding, renovation and handyman services based in Dipton, County Durham.

## Running locally

You need nothing installed except Python (comes with macOS):

```bash
cd /path/to/RFProperties
python3 -m http.server 8080
```

Then open [http://localhost:8080](http://localhost:8080) in your browser.

## Folder structure

```
RFProperties/
├── index.html          ← The entire site (edit this for content changes)
├── assets/
│   ├── img/            ← Photos go here (named clearly, e.g. consett-kitchen-before.jpg)
│   │   └── Ryan.png    ← Photo shown in the "Click for a Quote" popup
│   └── favicon.ico     ← Added in Phase 2
└── README.md
```

## How to edit content

Open `index.html` in any text editor (TextEdit, Notepad, VS Code).

- **Phone number** — search for `PLACEHOLDER_PHONE` and replace all instances.
- **Email** — search for `hello@rfproperties.co.uk`.
- **Team names / bios** — search for `PLACEHOLDER NAME` and `PLACEHOLDER —`.
- **Services text** — find the `<section id="services">` block.
- **Coverage villages** — find the `<div class="area-list">` block.

## How to add a project photo

1. Put the photo in `assets/img/` — compress it first (aim for under 300 KB; use [Squoosh](https://squoosh.app)).
2. In `index.html`, find a `<div class="gallery-item">` placeholder and replace the inner HTML:

```html
<div class="gallery-item">
  <img src="assets/img/your-photo.jpg" alt="Brief description" loading="lazy" />
  <div class="gallery-caption">
    <strong>Job title</strong>
    <span>Location · Type of work</span>
  </div>
</div>
```

## How to publish a change (once deployed to Netlify/Cloudflare Pages)

1. Save your changes to `index.html`.
2. Open Terminal in the project folder.
3. Run:

```bash
git add index.html
git commit -m "describe what you changed"
git push
```

The site updates automatically within about 30 seconds.

## Monthly costs (once live)

| Item | Cost |
|---|---|
| Domain (e.g. rfproperties.co.uk) | ~£10–15/year |
| Hosting (Netlify free tier) | £0 |
| Contact form (Formspree free tier) | £0 |
| Professional email (optional, via registrar or Google) | £0–£5/month |
