# Nyota Survey - Full project (Frontend + Backend)

This repository contains:
- `frontend/` - static pages (index.html, grant.html, payment.html, wait.html)
- `backend/` - Node.js + Express example server with M-Pesa Daraja (STK Push) integration sample

## Quick local run (backend)
1. cd backend
2. cp .env.example .env and fill with your Daraja sandbox credentials (or production if ready)
3. npm install
4. npm run dev
5. Start ngrok (if you need callbacks): `ngrok http 3000` and set `STK_CALLBACK_URL` to the ngrok URL + `/api/stk-callback`

## Frontend hosting
- You can host the `frontend/` folder on GitHub Pages:
  1. Create a new GitHub repo
  2. Commit the contents of `frontend/` to the `gh-pages` branch or enable GitHub Pages from main branch (docs folder)
  3. In GitHub Pages settings, point to the branch/folder and publish

## Deployment suggestions for backend
- Render, Railway, or Heroku can host the backend. Make sure to set environment variables in the platform's dashboard.

## Important security notes
- Never commit real credentials to source control.
- Use HTTPS in production.
- Validate webhook calls from Safaricom before trusting them.
