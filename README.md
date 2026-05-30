# PolyFarm — Quant Dashboard

Live quantitative trading dashboard for the PolyFarm automated prediction market system.

## Security Note

- **Demo data** — This repo contains empty/demo data only. Production portfolio, decisions, and bet data are injected at deploy time by the PolyFarm engine.
- **Auto-deployed** — Deployed to Netlify and Google Drive by `deploy_dashboard.py` on every scan cycle.

## Features

- Portfolio overview with equity tracking and P&L
- Open positions with real-time edge calculations
- Decision feed with model reasoning per trade
- Dark brutalist-luxury design with Chart.js
- Dynamic data loading from API when live

## Tech

- HTML/CSS/JS single-page app
- Chart.js for data visualization
- GitHub Pages (demo) / Netlify (production)

## Related

- [PolyFarm Engine](https://github.com/raphoc-hub/polyfarm) (private) — The Python trading system
