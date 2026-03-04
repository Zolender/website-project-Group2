# Website Clone (Group TailwindCSS Practice)

A group project built to practice **Tailwind CSS** by recreating a website from a **Figma design**. The goal was to translate a real design into responsive UI while building confidence with Tailwind utility-first styling.

## What we built

A static multi-page website (vanilla HTML + JS) with Tailwind:

- `index.html` — Landing page
- `menu.html` — Mobile menu page
- `contact.html` — Contact / imprint page
- `dataPrivacy.html` — Data privacy page

Shared sections live in `src/sections/` and are injected into pages at runtime using `fetch()`.

## Tech stack

- HTML + JavaScript (vanilla)
- Tailwind CSS (CLI)
- Google Fonts (Outfit)

## Getting started

### Install dependencies

```bash
npm install
```

### Development (watch Tailwind)

```bash
npm run dev
```

This watches `src/input.css` and outputs compiled CSS to `dist/output.css`.

### Build once

```bash
npm run build
```

### Run locally

Because sections are loaded via `fetch()`, use a local server (opening files directly may block requests).

Options:

**VS Code Live Server**
- Install the Live Server extension
- Right click `index.html` → “Open with Live Server”

**Node static server**

```bash
npx serve .
```

## Project structure

```text
.
├─ dist/
│  └─ output.css             # Tailwind compiled output
├─ src/
│  ├─ input.css              # Tailwind input + custom CSS vars for hero sizing
│  ├─ assets/                # images used by the pages/sections
│  └─ sections/              # HTML partials loaded via fetch()
│     ├─ header.html
│     ├─ hero.html
│     ├─ description.html
│     ├─ strategy.html
│     ├─ reference.html
│     ├─ footer.html
│     ├─ menuContent.html
│     ├─ contactInfo.html
│     └─ dataPrivacyInfo.html
├─ index.html
├─ menu.html
├─ contact.html
├─ dataPrivacy.html
└─ package.json
```

## What I learned / improved on

- Translating a real **Figma design** into pixel-close HTML layouts.
- Using Tailwind’s responsive utilities (`sm:`, `md:`, `lg:`) to adapt components across breakpoints.
- Working with advanced shape layouts using `clip-path` and custom CSS variables.
- Building a simple “component system” for static sites using `fetch()` + HTML partials.
- Handling navigation behaviors across multiple pages (menu toggle, anchor scrolling).

## Known issues / improvement ideas

- JS logic for loading sections and toggling the menu icon is repeated across pages — could be extracted to a shared JS file.
- `dist/output.css` is committed. Decide whether to keep it tracked or generate it only during build.
- Add better error handling if a section fails to load.
- Improve accessibility (focus states, skip link, contrast checks).

## Next steps checklist

### Documentation
- [ ] Add screenshots (hero, references, menu)
- [ ] Add the Figma link (if public) or a design preview image
- [ ] Add contributors/credits for group members

### Refactors
- [ ] Create a shared script (e.g. `src/main.js`) for: component loading, menu icon toggle, footer adjustments
- [ ] Standardize CSS path usage across pages (`./dist/output.css` vs `/dist/output.css`)

### UX / polish
- [ ] Add `prefers-reduced-motion` support for scroll/parallax effects
- [ ] Add small performance improvements (cache fetched partials)

## Credits

Group project for learning Tailwind CSS and implementing a Figma design.

## License

No license specified yet.