# anvl-status-page

Live status page for the [ANVL](https://anvl.site) platform.

Shows real-time service health, live user/project counts, and 30-day uptime history. Zero backend required — reads directly from ANVL's public API.

## What It Shows

- **Live metrics** — coin site count and registered wallet count (from `/api/stats`, updated every 5 min)
- **Service health** — checks 8 core services: Web Builder, Forge, DEX Tools, GMGN Proxy, Jupiter Swap, Auth (SIWS), Token Launch, Grid Bot
- **Uptime bars** — 30-day visual history
- **Auto-refresh** — re-checks all services every 5 minutes

## Deploy

### Option A — Host on Vercel (recommended)

```bash
git clone https://github.com/anvlproject/anvl-status-page
cd anvl-status-page
npx vercel deploy src/
```

### Option B — GitHub Pages

Push to a repo → Settings → Pages → Source: `src/` folder → Done.

### Option C — Self-host with any static server

```bash
npx serve src -p 4001
# Open http://localhost:4001
```

## Customise

Edit `src/index.html` to:
- Add/remove services from the `SERVICES` array
- Change `BASE` to point to a self-hosted ANVL instance
- Adjust refresh interval (default: 5 minutes)

## License

MIT — [github.com/anvlproject](https://github.com/anvlproject)
