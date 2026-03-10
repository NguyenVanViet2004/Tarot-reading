# Tarot Reading

An interactive three-card tarot spread web app built with Vue 3. Shuffle a full 78-card deck, draw three cards for **Past / Present / Future**, flip them to reveal meanings, and receive a synthesized reading.

## Features

- Full 78-card tarot deck (22 Major Arcana + 56 Minor Arcana) with Vietnamese interpretations
- Shuffle animation with Fisher-Yates algorithm
- Three-card spread with flip-to-reveal interactions
- Upright & reversed card meanings
- Auto-generated reading synthesis once all cards are revealed
- GPU-accelerated CSS transitions between phases
- Responsive design with a dark mystical theme

## Tech Stack

- **Vue 3** (Composition API + `<script setup>`)
- **Pinia** — state management
- **Vue Router** — client-side routing
- **Tailwind CSS v4** — utility-first styling with custom theme
- **Vite** — dev server & build tool
- **TypeScript** — full type coverage
- **Iconify** — icon library (`lucide` icon set)
- **VueUse** — composable utilities
- **Vitest** — unit testing

## Prerequisites

- Node.js `^20.19.0 || >=22.12.0`
- pnpm `10.31.0`

## Getting Started

```sh
# Install dependencies
pnpm install

# Start development server
pnpm dev

# Type-check, compile and minify for production
pnpm build

# Preview production build
pnpm preview
```

## Scripts

| Command | Description |
| --- | --- |
| `pnpm dev` | Start Vite dev server with HMR |
| `pnpm build` | Type-check + production build |
| `pnpm preview` | Preview the production build locally |
| `pnpm test:unit` | Run unit tests with Vitest |
| `pnpm lint` | Lint with oxlint + ESLint (auto-fix) |
| `pnpm format` | Format source files with oxfmt |
| `pnpm optimize:images` | Optimize image assets with Sharp |

## Project Structure

```
src/
├── assets/
│   ├── main.css              # Tailwind v4 config + custom theme
│   └── images/               # 78 tarot card images + card back
├── components/
│   ├── LandingScreen.vue     # Intro screen with CTA
│   ├── ShuffleDeck.vue       # Deck shuffle & draw phase
│   ├── ThreeCardSpread.vue   # Three-card layout with flip
│   ├── TarotCard.vue         # Single card display
│   └── ReadingSynthesis.vue  # Generated reading text
├── composables/
│   ├── useDeckService.ts     # Shuffle, draw, spread logic
│   └── useReadingSynthesis.ts# Reading text generation
├── data/
│   └── tarot-cards.ts        # Full 78-card database
├── stores/
│   └── useTarotStore.ts      # Pinia store (app state)
├── utils/
│   └── cardImages.ts         # Card image URL resolution
├── types.ts                  # TypeScript type definitions
├── meta.ts                   # Page metadata
├── main.ts                   # App entry point
└── App.vue                   # Root component
```

## License

Private
