# 🤖 Agent Dashboard

Real-time trading agent performance dashboard. Visualizes the performance of 15 trend-following trading agents running on simulated capital.

## Features

- 🏆 **Live Leaderboard** — Top 3 agents with medals and performance metrics
- 📊 **Performance Stats** — Summary metrics (total agents, runs, ROI)
- 📈 **Full Rankings** — Complete leaderboard with win rates and P&L
- 🔄 **Auto-Refresh** — Updates every 60 seconds
- 🎨 **Apple-Level Design** — Glassmorphism, smooth animations, dark mode

## Tech Stack

- **Frontend:** React 18 + Vite
- **Styling:** Modern CSS with animations and gradients
- **Backend:** Express.js API
- **Data:** JSON performance logs

## Setup

### Install

```bash
cd agent-dashboard
npm install
```

### Development

```bash
npm run dev
```

Runs on `http://localhost:5173`

### Build

```bash
npm run build
```

Produces optimized bundle in `dist/`

### Run Server

```bash
npm run server
```

Or combined:

```bash
npm run start
```

Server runs on `http://localhost:3001` with frontend served as static files.

## API

### GET `/api/dashboard`

Returns current agent performance data:

```json
{
  "timestamp": "2026-02-17T22:02:34Z",
  "leaderboard": [
    {
      "id": "8",
      "name": "Risk Taker",
      "roi_percent": 4185.30,
      "total_pnl_usd": 41852.96,
      "win_rate": 70.8,
      "total_trades": 24
    }
  ],
  "summary": {
    "agents": 15,
    "runs": 1,
    "total_pnl": 92760.65,
    "avg_pnl": 6184.04
  }
}
```

## Data Source

Dashboard reads from `../agent_performance.jsonl` (newline-delimited JSON performance logs from the trading simulator).

## Deployment

### Vercel

```bash
vercel deploy
```

### Traditional Server

Build the frontend and run the Express server:

```bash
npm run start
```

---

**Status:** 🟢 Active  
**Last Updated:** Feb 17, 2026  
**Repo:** https://github.com/SuryaNickil/agent-dashboard
