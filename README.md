# RAHUL.exe // PORTFOLIO

```
   ____  ___    __  ____  ______       _____  ________
  / __ \/   |  / / / / / / / /  |     / __/ |/ / ____/
 / /_/ / /| | / /_/ / / / / /| |    / _/ |   / __/
/ _, _/ ___ |/ __  / /_/ / ___ |  / /___/   / /___
/_/ |_/_/  |_/_/ /_/\____/_/  |_| /_____/_/|_/_____/

>> STATUS: ONLINE
>> THEME:  NEO_BRUTALISM
>> STACK:  ZERO_DEPENDENCIES
```

The personal site of **Rahul Prajapati** — full stack developer, system design.
Live at **[roldex.me](https://roldex.me)**.

---

## /// WHAT_THIS_IS

A single-file static portfolio aimed at clients: what I build, what I've shipped,
and how I work. Deliberately unfashionable in its implementation — no framework,
no build step, no dependencies to rot.

**One HTML file. ~66KB. One external request (fonts).**
Nothing renders behind JavaScript, which is what makes it both fast and indexable.

---

## /// TECH_STACK

| COMPONENT   | TECHNOLOGY                         | NOTES                            |
| :---------- | :--------------------------------- | :------------------------------- |
| **MARKUP**  | `HTML5`                            | Semantic, single file            |
| **STYLING** | `Hand-written CSS`                 | Custom properties, no framework  |
| **SCRIPT**  | `Vanilla JS`                       | ~60 lines, no libraries          |
| **ICONS**   | `Inline SVG`                       | No icon font                     |
| **FONTS**   | `Space Grotesk` + `JetBrains Mono` | Preconnected, `display=swap`     |
| **BUILD**   | —                                  | There isn't one. Open the file.  |

### Why no framework

The previous version of this page loaded the Tailwind CDN compiler (a
render-blocking script that rebuilds the CSS in the browser on every visit),
an icon webfont for ten icons, and made live API calls on load. All of it is
gone. If the argument of the site is that I care about performance, the site
itself has to be the evidence.

---

## /// FEATURES

### 01. CUSTOM_CURSOR

White core, black ring, white halo — readable on the cream background, the black
sections and the yellow section alike. Expands to a yellow disc over interactive
elements. Desktop pointer only; never shown on touch.

### 02. REVEAL_ANIMATION

`IntersectionObserver`, unobserved after firing. Respects
`prefers-reduced-motion` — the whole page falls back to static.

### 03. MARQUEE

Pure CSS, `transform`-only, pauses on hover.

### 04. GRACEFUL_IMAGE_FALLBACKS

Every image degrades to a typographic placeholder rather than a broken-image
icon if it fails to load.

### 05. SEO

Canonical, Open Graph and Twitter tags, plus JSON-LD (`Person` +
`ProfessionalService`) so search engines can connect the identities.

### 06. ACCESSIBILITY

Skip link, visible focus rings, semantic landmarks, labelled form fields,
`aria-hidden` on decoration.

---

## /// FILE_STRUCTURE

```bash
.
├── assets/
│   ├── rahul.jpg            # portrait (square)
│   ├── learning-leaders.png # project shot (16:9)
│   ├── buxar-police.png     # project shot (16:9)
│   └── og.png               # social card (1200x630)
├── index.html               # the whole site
└── README.md                # you are here
```

---

## /// RUN_LOCALLY

```bash
git clone https://github.com/<user>/<repo>.git
cd <repo>
python3 -m http.server 8000   # or just open index.html
```

There is no install step. That is the point.

---

## /// DEPLOY

Static host of choice. The custom domain is `roldex.me`.

**GitHub Pages** — Settings → Pages → source `main` / root, set the custom
domain, then point the apex at GitHub with four A records
(`185.199.108–111.153`) and `www` at `<user>.github.io`. Enable *Enforce HTTPS*
once the certificate provisions.

**Cloudflare Pages / Netlify / Vercel** — connect the repo, no build command,
output directory `/`.

---

## /// CONTACT

- **MAIL**: `roldexstark@gmail.com`
- **LINKEDIN**: [rahulprajapati19](https://www.linkedin.com/in/rahulprajapati19/)
- **INSTAGRAM**: [@roldexstark](https://www.instagram.com/roldexstark/)
- **LOCATION**: India · working remotely

> "The best engineers don't just build software — they solve problems worth solving."

---

**© 2026 RAHUL PRAJAPATI // SYSTEM_END**
