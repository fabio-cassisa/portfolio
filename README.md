# portfolio

terminal-inspired personal site — dark-first, monospace, interactive.

built because every portfolio i made before felt too polite.  
this one boots like a system, runs like a terminal, and hides things for people who poke around.

### live

🟢 [dagas-portfolio.vercel.app](https://dagas-portfolio.vercel.app)

### what's in here

- **terminal ui** — collapsible command-line at the bottom of every page. real commands (`help`, `ls`, `cat <project>`, `neofetch`), tab completion, command history, and 30+ easter eggs
- **neofetch block** — tech stack rendered as a system info dump
- **project tiers** — flagship and supporting projects, each in terminal-window cards
- **experience + education** — full timeline, no fluff
- **view transitions** — smooth page morphs via astro's client router
- **custom 404** — terminal-themed "file not found"
- **og card** — auto-generated terminal-style social preview

### stack

`astro` · `tailwind v4` · `typescript` · `jetbrains mono`

### design decisions

- dark-only — the terminal _is_ the design. no light mode toggle
- crt scanlines, green accent (#4ade80), macOS window chrome
- all images compressed to webp (~96KB total for 5 thumbnails)
- zero platform-specific emoji in the UI — text characters inherit theme color
- easter eggs reward curiosity: `hack`, `matrix`, `rm -rf /`, `crash`, `reboot`, `disco`, and more

### run locally

```sh
npm install
npm run dev       # localhost:4321
npm run build     # static output in dist/
```

### structure

```
src/
├── components/   # navbar, footer, hero, neofetch, terminal, project cards
├── data/         # info.ts — all content lives here
├── layouts/      # single layout with view transitions
├── pages/        # index, projects, 404
└── styles/       # global.css — terminal design system
```

update `src/data/info.ts` to change what the site displays.

---

<sub>built by fabio cassisa</sub>
