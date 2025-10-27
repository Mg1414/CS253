# CS253 — College Path Finder (ELI5 Guide)

This project is a full‑stack web app that helps students discover colleges, compare options, see opinions, and share posts. It has two halves:

- Backend: Node.js + Express + MongoDB (users, posts, tags, replies, OTP)
- Frontend: React (routing + authenticated pages + service calls)

## How to think about it (kid‑friendly):

- The backend is a big librarian: it keeps the books (data), checks your library card (token), and gives you the right page when you ask.
- The frontend is the friendly website: it shows screens based on the URL and only lets you into special rooms if you’re logged in and verified.

## File map with quick mental models:

- `college_backend-main/index.js`
  - Boot the server, connect to DB, mount routes.
- `college_backend-main/middleware/auth.js`
  - The “bouncer”: checks your JWT token.
- `college_backend-main/routes/users.js`
  - Sign up, log in, view profiles, helper endpoints (search/compare/opinion).
- `college_frontend-main/src/App.js`
  - Fetch user once → store in state → choose which component to render.
- `college_frontend-main/src/utils/paginate.js`
  - Simple pagination helper with “skip N then take K” logic.

## Running (dev):

- Backend: `cd college_backend-main && npm i && npm run start` (set env vars for Mongo URL and JWT key)
- Frontend: `cd college_frontend-main && npm i && npm start`

## Why you’ll find this repo easy to read now:

- Each main file starts with a “what/why” block.
- Tricky spots like JWT auth and routing have mini‑explainers.
- No functional changes — your existing workflows remain intact.

If you want me to add diagrams (auth flow, data model, React routing), say the word and I’ll commit those too.
