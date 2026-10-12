# Student Complaints Portal: Frontend

React + Vite single-page app. Students submit and track complaints; administrators log in to review, reply to, update and delete them.

## Links
- Backend repository: https://github.com/riteesh186-del/student-complaints-backend
- Live website: https://student-complaints-frontend.onrender.com
- Live API: https://student-complaints-portal.onrender.com/api/complaints (the free host sleeps when idle, so the first request can take up to a minute)

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
