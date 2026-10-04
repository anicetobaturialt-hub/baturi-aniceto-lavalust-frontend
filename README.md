# Product Management – React Frontend

React + Vite frontend for the LavaLust Product Management API (Laboratory Exercise No. 6).
Features: register, login, product list, add / edit / delete, logout, automatic token refresh.

This app only talks to the API over HTTP. It never connects to the database.

## Run locally

```bash
cp .env.example .env      # set VITE_API_URL
npm install
npm run dev
```

`VITE_API_URL` is the base URL of the LavaLust API, with no trailing slash:

- Local: `http://localhost:3000` (run `php lava serve --port=3000` in the API repo)
- Deployed: `https://your-api.onrender.com`

On the API side, set `ALLOW_ORIGIN` to this app's URL (e.g. `http://localhost:5173` locally) so CORS allows it.

## Build / deploy (Render Static Site)

| Setting | Value |
|---|---|
| Build command | `npm install && npm run build` |
| Publish directory | `dist` |
| Environment variable | `VITE_API_URL` = your API URL |

Add a rewrite rule `/*  →  /index.html` (Redirects/Rewrites tab) if you later add client-side routes.
