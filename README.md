# CineVault – Movie Discovery Web App

A responsive React app to browse, search and explore movies and TV shows, with a localStorage watchlist.

## Technologies
React 18 (JSX) · Vite · Material UI · React Router · Fetch API · TMDB API

## Selected API
[TMDB](https://www.themoviedb.org/) (v3). *This product uses the TMDB API but is not endorsed or certified by TMDB.* Poster images are served by TMDB's image CDN.

## Run locally
1. `npm install`
2. Create a free TMDB account and request an API key (Settings → API).
3. Copy `.env.example` to `.env` and set `VITE_TMDB_API_KEY` to your **v3 API key**.
4. `npm run dev` and open the printed URL.

## Features
Homepage with 4 sections · Movies / TV pages with genre filter and pagination · Title search · Details page · Watchlist (localStorage) · Responsive layout (drawer menu on mobile) · Loading, empty, missing-poster and error handling.

## Project structure
`src/api.js` (fetch + `useTmdb` hook) · `src/WatchlistContext.jsx` · `src/components/` (Layout, MovieCard, MovieList, Section, Status) · `src/pages/`

## Deployment
Add `VITE_TMDB_API_KEY` as an environment variable on Vercel/Netlify. `vercel.json` and `public/_redirects` handle client-side routing.

## Note on the API key
TMDB's v3 key is designed for client-side use, but Vite embeds it in the built bundle. Never commit `.env`, and never use the private "Read Access Token".
