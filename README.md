# Roadmaps — Mobile

## Template copy

This repository is one of the name-substituted Ionic React + Vite template copies in `bookchaowalit-mobile`.
The canonical template is
[`bookchaowalit-mobile/marketing-seo-analyzer-mobile`](https://github.com/bookchaowalit-mobile/marketing-seo-analyzer-mobile).
Consolidation or archiving of the copies is pending owner decision D5 (BD-033), per
`repository-catalog/portfolio/MOBILE-CONSOLIDATION-2026-10.md` in solo-empire.
There is no Capacitor native project here: it builds a Vite web app only, not an Android or iOS binary.

Ionic + React cross-platform mobile app for **Roadmaps**.

Part of [Chaowalit Greepoke](https://bookchaowalit.com)'s 101 Portfolio Projects.

## Features

- **Roadmap board** (Home tab): milestones with target dates, each showing its
  items, a progress bar (in-progress counts as half) and a health badge —
  complete, on-track, at-risk (≤14 days left and under 50%) or overdue. Tap an
  item's status chip to cycle planned → in-progress → done. Add items and
  milestones; everything is saved in `localStorage` (sample roadmap on first run).
- Roadmap logic lives in `src/lib/roadmap.ts` (pure TypeScript, unit-tested).

## Tech Stack

- **Framework:** Ionic 8 + React 18
- **Language:** TypeScript
- **Build Tool:** Vite
- **UI:** Ionic Components + Ionicons

## Getting Started

```bash
npm install
npm run dev
```

## Scripts

```bash
npm run dev         # Vite dev server
npm run typecheck   # tsc (noEmit)
npm run lint        # ESLint flat config (typescript-eslint + react-hooks)
npm test            # vitest unit tests for src/lib
npm run build       # tsc && vite build
```

CI (`.github/workflows/ci.yml`) calls the shared `bookchaowalit/platform-ci-workflows` v1.1.1
(`ci-node.yml` + `security.yml`, pinned by SHA): `npm ci`, lint, typecheck, tests, `npm run build`, and the
gitleaks / Semgrep / OSV-Scanner / Trivy scans. Failures are not masked.

## Build

```bash
npm run build
# Static web build in dist/. A native app would need a Capacitor project, which does not exist yet.
```

## Related

- **Frontend:** [bookchaowalit-website/roadmaps-frontend](https://github.com/bookchaowalit-website/roadmaps-frontend)
- **Portfolio:** [bookchaowalit.com](https://bookchaowalit.com)

## License

MIT
