# Road Rivals

Family road-trip car-spotting game. Single-page mobile web app — no build step, no dependencies.

## Stack
- Pure HTML + CSS + JS in `index.html`
- Image assets in `assets/`
- Scores and history stored in `localStorage`
- Designed for iPhone Safari (add to home screen)

## Deploy target
Cloudflare Pages static site. Root directory is `/` (the repo root).
Build command: *(blank)* — Output directory: `.`

To deploy via CLI:
```bash
npx wrangler pages project create road-rivals --production-branch main
npx wrangler pages deploy . --project-name road-rivals
```

## Game rules

| Car | Points |
|---|---|
| Tesla ⚡ | 1pt — **locked on first turn** |
| Green Bean 🫘 | 2pts |
| Pinch Mini 🎩 | 2pts |
| Punch Buggy 🐞 | 3pts |
| Pink Panther 🐆 | 5pts |
| Police 🚔 / Fire 🚒 / Ambulance 🚑 | 1pt · 2pt (lights) · 3pt (lights+siren) |

**First spot of each game = 2× points. Tesla cannot be the first spot.**

## Features
- 2–5 players with name persistence
- Pulsing gold "FIRST SPOT = 2× POINTS!" banner until first score claimed
- Tap car → pick player (or pre-select player then tap car)
- Emergency vehicles: tap → popup to pick point level
- Undo last score, Reset game, Game Over (saves to history)
- History screen: stats, all-time wins bar chart, full game log
- Celebration overlay + confetti on first spot and game over

## Owner
Adam — adam@safeteksolutions.com.au
