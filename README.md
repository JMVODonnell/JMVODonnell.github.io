# jmvodonnell.github.io

Personal portfolio — narrative design, editorial and development.
Live at <https://jmvodonnell.github.io/>.

Plain HTML, CSS and vanilla JavaScript. No build step: edit, commit, push.

## Files

| Path | What it is |
|---|---|
| `index.html` | The whole page, plus the config and content data at the bottom of the file |
| `styles.css` | All styling. Design tokens are the `:root` variables at the top |
| `Images/` | Site images. `og-card.jpg` is the social-share preview |
| `Music/` | Audio for the player |
| `404.html` | Not-found page |

## Adding things

Everything editable lives in the `<script>` block near the bottom of `index.html`.

**Your links** — `SITE`. Leave a value as an empty string and that link stays
hidden, so the site never shows a dead link:

```js
const SITE = {
  email:    'jmvodonnell@gmail.com',
  linkedin: '',   // paste your LinkedIn URL here to make the button appear
  github:   'https://github.com/JMVODonnell',
  ...
};
```

**A game** — add an object to `GAMES` and a slide appears. There is a commented
FRACTURE template in there showing every field. `status` is optional and renders
as a badge (e.g. `'In development'`).

**A track** — add an object to `TRACKS`.

**A testimonial** — copy a `.carousel-slide` block in the testimonials section.
The short quote goes in `.pull-quote`; the rest goes in the `.quote-rest` div
behind the "Read full testimonial" button. Give the div a unique `id` and point
the button's `data-target` and `aria-controls` at it.

## Images

Keep them small. Nothing here needs to be wider than about 1600px; source files
straight from a camera or design tool are typically 20–80x larger than the page
ever displays. Re-export at display size before committing.
