# PolyFarm — Dashboard Frontend

A single-page interface for exploring prediction-market portfolio, position and decision-log layouts. This repository publishes the dashboard, **not the trading engine**.

[Portfolio](https://raphoc-hub.github.io/#work)

## What is here

- Portfolio summaries and Chart.js visualizations.
- Position, history and decision views with filters and expandable details.
- Market-category and configuration panels.
- A separate cryptocurrency price widget using Binance's public REST and WebSocket endpoints.

The frontend is contained in [`index.html`](index.html), with Chart.js and fonts loaded externally. There is no package installation or build step.

## Preview locally

Requires Git, Python 3 and an internet connection for external assets.

```sh
git clone https://github.com/raphoc-hub/polyfarm-dashboard.git
cd polyfarm-dashboard
python3 -m http.server 8000 --bind 127.0.0.1
```

Open <http://127.0.0.1:8000/>. Empty portfolio and decision views are expected. On localhost the client attempts `GET /api/state`; the static server returns `404` because no API is included. Stop the server with `Ctrl+C`.

The separate Binance price widget may populate when those endpoints are reachable. That does not connect the portfolio to an engine or demonstrate trading activity.

## Status and provenance

**Public frontend snapshot with empty/demo portfolio state.** The committed `PORTFOLIO` starts without positions; `DECISIONS` and `MULTIBET` are empty. Seed capital and labels such as `LIVE`, `PAPER` or “Scanner is running” are display defaults, not verified account or system status.

The client supports externally supplied state, but this repository does not include the private engine, its API, data pipeline or execution logic. The README describes the committed files; separately deployed copies can contain different data and are not evidence for this snapshot.

No profitability, validated strategy or live-trading claim is made. Treat the interface as a development artifact, not investment advice.

## License

[MIT](LICENSE).
