# Personal Dashboard + API on Raspberry Pi

## Table of Contents
1. [Goal](#goal)
2. [Tech Stack](#tech-stack)
3. [Features](#features)
   - [Phase 1 – Basic MVP](#phase-1--basic-mvp)
   - [Phase 2 – Intermediate](#phase-2--intermediate)
   - [Phase 3 – Advanced](#phase-3--advanced)
4. [Roadmap](#roadmap)

---

## Goal
Build a small web app that shows useful info (like weather, Pi stats, to-do list) and exposes a small API to manage data.

---

## Tech Stack

| Layer      | Technology                                         |
|------------|---------------------------------------------------|
| Backend    | Node.js + Express                                 |
| Frontend   | EJS/Handlebars templates or lightweight React    |
| Database   | SQLite or MongoDB (local on Pi)                  |
| API        | REST endpoints for your data (e.g., to-do items, Pi metrics) |
| Deployment | Raspberry Pi + PM2 (process manager)             |
| Optional   | WebSocket (for real-time updates like CPU/memory usage) |

---

## Features

### Phase 1 – Basic MVP
- Web dashboard showing:
  - Local time/date
  - Weather from an API (OpenWeatherMap or similar)
  - Pi system stats (CPU load, memory, uptime)
- REST API to get system stats
- Simple to-do list stored in DB

### Phase 2 – Intermediate
- Add user authentication (simple username/password)
- Store dashboard preferences per user
- Add ability to schedule tasks/scripts from dashboard
- Add light styling with CSS frameworks (Tailwind or Bootstrap)

### Phase 3 – Advanced
- Real-time system stats (WebSockets)
- Push notifications for tasks or alerts
- Optionally, allow external access (with HTTPS, reverse proxy with Nginx)

---

## Roadmap

1. **Set up development environment**
   - Install Node.js and npm in WSL
   - Scaffold project (`npm init`, install Express, etc.)
   - Create folder structure (`routes/`, `views/`, `public/`, `db/`)
2. **Build backend API**
   - Create REST endpoints for system stats and to-do items
   - Add database integration (SQLite is easiest on Pi)
   - Test endpoints in Postman or curl
3. **Build frontend**
   - Start with server-side rendered pages (EJS/Handlebars)
   - Display API data dynamically
4. **Test locally on WSL**
   - Run your server (`node index.js` or `nodemon index.js`)
   - Make sure API and frontend work as expected
5. **Deploy on Raspberry Pi**
   - Copy files via SCP or Git clone
   - Install Node.js and dependencies
   - Run server with PM2 so it stays alive
   - Optional: configure Nginx as reverse proxy for nicer URLs
6. **Enhancements**
   - Add authentication, WebSockets, external APIs
   - Add logs or data visualization (charts for CPU/memory history)
