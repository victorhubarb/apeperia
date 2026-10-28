# Apeperia

A landing page for a fictional app-development company, built with HTML, CSS and JavaScript and no framework. The page has a hero section, benefits, pricing plans, a blog carousel, a contact form and a newsletter dialog. A lot of the work went into making it usable with a keyboard and a screen reader.

**Live demo:** [apeperia-one-blue.vercel.app](https://apeperia-one-blue.vercel.app)

## What's inside

- **Accessible modal.** The newsletter dialog has `role="dialog"` and an `aria-labelledby` title. Opening it moves focus inside and makes the rest of the page `inert`, so Tab cannot leave it. Esc, the close button or a click on the overlay closes it, and focus returns to the button that opened it. The `inert` attribute is backed by the W3C polyfill in `js/inert.js` for older browsers.
- **Blog carousel.** Controls are real links, the visible slide is switched in `carousel.js`, and a visually hidden "(Slide atual)" label tells screen readers which slide is showing.
- **Form validation.** Native HTML5 validation, with a custom message and error styling on the ZIP code field (`validacao-cep.js`).
- **Email typo suggestions.** The [Mailcheck](https://github.com/mailcheck/mailcheck) library suggests a fix when someone types `gmial.com`, and the suggestion is announced with `role="alert"`.
- **Video with subtitles.** A `<video>` with a Brazilian Portuguese `.vtt` track.
- **CSS split by section.** Fifteen small stylesheets (header, plans, blog, contact, dialog and so on), with a shared theme file and media queries for smaller screens.

The page is in Portuguese.

## Run it

No build step and no dependencies. Clone the repo and open `index.html` in a browser.

```bash
git clone https://github.com/victorhubarb/apeperia.git
cd apeperia
```

## Project structure

```
index.html
css/   One stylesheet per section, plus reset and theme
js/    carousel, dialog, inert (polyfill), mailcheck (library), validacao-cep, mailcheck-config
img/   Images, video and subtitle file
```

## Known gaps

- The code uses `var` and `keyCode`, in an older JavaScript style.
- The form does not send anywhere, because there is no backend.
- Blog links point to a site that no longer exists.
- Fonts are loaded from Google Fonts, so the page needs a connection to look right.

---

Victor Hugo Barbosa · [GitHub](https://github.com/victorhubarb) · [LinkedIn](https://www.linkedin.com/in/victorhbarbosa/)
