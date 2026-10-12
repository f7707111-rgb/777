# kikiOS — PC Boost

Static site: Game Boy hero, service info and the "Software & Windows" downloads window.
No build step — open `index.html` or deploy the folder to GitHub Pages as is.

## Structure

```
index.html                  home page markup
section.html                folder page (section.html?s=terms)
css/
  base.css                  global rules (hidden scrollbars)
  gameboy.css               Game Boy device
  site.css                  page sections, themes, footer
  components/software.css   "Software & Windows" window
  components/folders.css    folders with hover lift
  pages/section.css         folder page layout
js/
  data/translations.js      EN / RU strings (data-i18n keys)
  data/software.js          Windows ISO and app download list
  data/sections.js          4 folders: terms, BIOS, AME Wizard, network (EN / RU)
  site/theme-init.js        applies saved theme before paint
  site/settings.js          theme + language switches
  site/software.js          renders and opens the downloads window
  site/reveal.js            scroll animations
  site/folders.js           renders folder cards + page transition
  pages/section.js          renders one folder page on section.html
  gameboy/                  console engine (font, lcd, sound, input, main) + games loader
assets/
  fonts/                    AmeSans
  favicons/                 site icons
  icons/social/             Discord, GitHub, X, YouTube
  icons/apps/               white app logos for the downloads window
  icons/misc/               spare icons (not used yet)
  images/sections/          pixel-art covers for the folders
  docs/                     KIKI TWEAKS terms (PDF)
```

## Common edits

- **Add a download:** add a line to `js/data/software.js`; put its white SVG into `assets/icons/apps/`.
- **Edit a folder page:** change texts in `js/data/sections.js`; covers live in `assets/images/sections/`.
- **Change text:** edit `js/data/translations.js` (both `en` and `ru`).
- **Open the window by link:** `…/#software`.
