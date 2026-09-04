# Base44 Dev Environment

## Overview
Pure frontend Vite + React 19 portfolio app (Three.js, Tailwind v4, Framer Motion).
No backend, no database, no external secrets required.

## Running
```
docker compose -f docker-compose.base44.yml up -d
```
- Web entry point: host port 3000 → container port 5173 (Vite dev server)
- `npm install` runs automatically on container start
- Live reload enabled via bind mount + chokidar polling

## Notes
- The Web3Forms access key is hardcoded in `src/sections/Contact.jsx` (not an env var).
- Vite config has `server.host: true` and `allowedHosts: true` to accept the preview proxy origin.
- Node modules are stored in a named volume to avoid host/platform conflicts.
