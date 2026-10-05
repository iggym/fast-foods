# fast-foods

> A field guide to fast food — menus, numbers, history, and how the same idea tastes in a dozen countries.

**Live page:** https://iggym.github.io/fast-foods/

## What this is

A single hand-written HTML page about fast food, built as a hypermedia piece: every interaction is
either a link, a form-free native element, or CSS.

- **No JavaScript.** The dark-mode switch is a checkbox and a `:has()` selector. The accordions are
  native `<details>`. Navigation is ordinary anchor links.
- **No framework, no build step, no dependencies.** Open `index.html` in a browser and it works.
- **One image.** `assets/hero.webp` (with a JPEG for social previews); everything else is CSS and
  inline SVG.

## Project structure

```
fast-foods/
├── index.html          # the whole site
├── assets/
│   ├── hero.webp       # hero image, WebP
│   └── hero.jpg        # same image, JPEG, for og:image
├── .nojekyll           # serve files verbatim on GitHub Pages
├── LICENSE
├── README.md
└── .gitignore
```

## Running it locally

```bash
git clone https://github.com/iggym/fast-foods.git
cd fast-foods
open index.html          # macOS  (or: xdg-open index.html / start index.html)
```

No server required. If you'd rather use one:

```bash
python3 -m http.server 8000   # then visit http://localhost:8000
```

## The page

| Section | What's in it |
|---|---|
| The definition | The three promises every fast food meal is built on |
| The repertoire | Eight items that scaled into a global industry |
| The numbers | Market size, QSR share, regional split, and a restaurant-count chart |
| The timeline | 1921 to the 2020s, in ten steps |
| The world tour | Twelve local answers to the same format |
| Trivia | Five things worth knowing |
| Sources | Every figure labelled with where it came from |

Market figures are cited inline and in the Sources section, and are framed as ranges because the
analysts disagree — "fast food" is a fuzzy boundary. Figures checked 5 October 2026.

## Roadmap

- [x] Decide on a tech stack — plain HTML and CSS
- [x] Add the source
- [x] Publish via GitHub Pages
- [ ] Add a test that validates the markup
- [ ] Add CI (GitHub Actions)
- [ ] Add more sections (nutrition, regional chains, pricing over time)

## Contributing

1. Fork the repo
2. Create a feature branch: `git checkout -b feat/my-feature`
3. Commit your changes: `git commit -m "feat: add my feature"`
4. Push the branch: `git push origin feat/my-feature`
5. Open a pull request

Commit messages in this repo loosely follow [Conventional Commits](https://www.conventionalcommits.org/).

## License

Released under the [MIT License](LICENSE).
