# Shivansh: personal site

Plain HTML/CSS/JS, koi build step nahi. `index.html` browser me kholo ya GitHub Pages pe daal do.

## Folder structure

```
index.html              <- sirf page ka structure + text (sections)
assets/
  hero.jpg              <- hero photo (replace karne ke liye same naam se file badal do)
css/                    <- load order index.html me hai, change mat karna
  base.css              colours (:root), fonts, layout, buttons
  mobile.css            mobile overrides
  hero.css              hero text, photo, film grain
  header-menu.css       top header, full-screen menu, credits panel
  subscribe.css         subscribe form
  sections.css          section background colours
js/
  config.js             email, subscribe endpoint (Apps Script URL)
  data/work.js          Work section ka poora content (fields, poems, projects)
  data/credits.js       Credits list
  work.js  menu.js  subscribe.js  contact.js  header.js  credits.js   <- logic (usually chhedna nahi)
```

## Kya change karna hai -> kahan jao

| Kaam | File |
|---|---|
| Naya project / poem / field add karna | `js/data/work.js` |
| Credits add karna | `js/data/credits.js` |
| Email ya subscribe endpoint | `js/config.js` |
| Hero photo badalna | `assets/hero.jpg` (+ credit line `index.html` me `.photo-credit`) |
| Colours / fonts | `css/base.css` ke top me `:root` |
| Section ka text (Why, Philosophy, Poem, About, Contact, links) | `index.html` |
| Section background colour | `css/sections.css` |
| Social links (GitHub, LinkedIn...) | `index.html`, `id="contact"` section |

## Naya project add karne ka example (`js/data/work.js`)

```js
projects: [
  { title: "Naya Project", year: "2026", description: "Short line.", url: "https://..." }  // url optional
]
```

## Note
CSS files ka order (`index.html` me link tags) mat badlo: mobile/hero rules baad wali files se override hote hain.
