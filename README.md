# swarmhaul-pitch

Marketing & pitch site for [SwarmHaul](https://github.com/mighty840/swarmhaul) — multi-agent coordination protocol on Solana.

Built with Astro + Tailwind v4. Static-first. Deployed to GitHub Pages.

## Develop

```bash
bun install
bun run dev      # http://localhost:4321
```

## Build

```bash
bun run build    # outputs to dist/
bun run preview  # serve dist locally
```

## Deploy

Auto-deploys to GitHub Pages on every push to `main` via `.github/workflows/deploy.yml`.

## Structure

```
src/
├── layouts/Layout.astro       # HTML shell, fonts, OG metadata
├── components/
│   ├── Nav.astro              # Sticky terminal-style header
│   └── Footer.astro
├── sections/                  # One file per pitch section
│   ├── Hero.astro
│   ├── Problem.astro
│   ├── Protocol.astro         # 5-step lifecycle
│   ├── Demo.astro             # Loom embed slot
│   ├── MCP.astro              # MCP integration story
│   ├── Architecture.astro     # 4-layer breakdown
│   ├── Security.astro         # Audit findings
│   ├── Roadmap.astro          # 4-phase ship plan
│   ├── Team.astro
│   └── CTA.astro
├── pages/index.astro          # Composes everything
└── styles/global.css          # Theme tokens, animations, utilities
```

## Design system

Same palette and fonts as the SwarmHaul dashboard for visual consistency:

- **Mono**: JetBrains Mono (300-700)
- **Display accent**: Instrument Serif italic
- **Palette**: void black ▸ phosphor green ▸ hot magenta ▸ electric cyan ▸ amber

## Content TODO

- [ ] Replace Loom embed placeholder in `Demo.astro`
- [ ] Real OG image (`public/og.png`)
- [ ] Real screenshots / animated swarm visualization
- [ ] Final copy pass on every section
- [ ] Custom domain CNAME
- [ ] Plausible/Umami analytics snippet
