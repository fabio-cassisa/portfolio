# astro-folio24

personal portfolio site — experience, education, and project showcase. dark-first with theme toggle, auto-generated sitemap, and SEO meta tags out of the box.

## context

built on top of [uzair ahmed's astro portfolio template](https://github.com/uzzii-21/astro-portfolio). the template provided a clean starting point — i customized the content, added experience entries, swapped social links, and fixed up project URLs and metadata over time.

the design is intentionally minimal. content lives in a single `info.ts` data file that drives the entire site — experience, education, projects, and social links.

## stack

`astro 1` · `tailwind css` · `typescript` · `netlify`

## structure

```
src/
├── components/
│   ├── general/
│   │   ├── Footer.astro          # social links (X, GitHub, LinkedIn)
│   │   ├── MetaHead.astro        # SEO, OG tags, favicons
│   │   ├── Navbar.astro          # logo + theme toggle
│   │   ├── ProjectCard.astro     # thumbnail with hover overlay + links
│   │   └── ProjectsWrapper.astro # responsive grid wrapper
│   └── home/
│       ├── Experience.astro      # timeline section (experience + education)
│       └── Hero.astro            # intro section
├── data/
│   └── info.ts                   # all content lives here — single source of truth
├── layouts/
│   └── Layout.astro              # navbar + main + footer shell
├── pages/
│   ├── index.astro               # home — hero, experience, featured projects
│   └── projects.astro            # all projects grid
├── styles/
│   ├── custom-styles.css         # gradient heading animation
│   ├── fonts.css                 # Inter + Outfit @font-face declarations
│   └── style.css                 # tailwind layers + component styles
├── types/
│   └── index.ts                  # TypeScript interfaces
└── utils/
    └── index.ts                  # logo helper (initials from name)
```

## setup

```bash
npm install
npm run dev       # localhost:3000
npm run build     # static output → dist/
```

## notes

- all content is driven from `src/data/info.ts` — edit that file to update experience, projects, or social links
- theme toggle persists via localStorage with `prefers-color-scheme` as default
- sitemap and robots.txt are auto-generated via astro integrations
- self-hosted Inter and Outfit fonts (all weights) in `public/assets/fonts/`
- astro v1 — upgrade to v4+ is planned but not yet done

## status

🟢 live — [portfolio24-dagas.netlify.app](https://portfolio24-dagas.netlify.app)

---

<sub>built by [fabio cassisa](https://github.com/fabio-cassisa) · template by [uzair ahmed](https://github.com/uzzii-21)</sub>
