# Student Complaints Portal: Frontend

React + Vite single-page app. Students submit and track complaints; administrators log in to review, reply to, update and delete them.
Backend repository: the separate Spring Boot API this app calls.

## Configuration
| Variable | Purpose | Default |
|---|---|---|
| `VITE_API_URL` | Backend base URL, no trailing slash | `http://localhost:8080` |

`VITE_API_URL` is read at build time, so rebuild after changing it.

## Run locally
Requires Node.js LTS.

```powershell
npm install
npm run dev
```

Open the URL Vite prints, usually `http://localhost:5173`. The backend must be running and must allow this origin through its `CORS_ALLOWED_ORIGINS` setting.

## Build
```powershell
npm run build
```

Output goes to `dist/`.

## Deployment
Deployed on Render as a Static Site: build command `npm install && npm run build`, publish directory `dist`, with `VITE_API_URL` pointing at the deployed backend.
