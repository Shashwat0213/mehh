# MCU Tracker — Frontend Starter

A responsive, local-first MCU tracking frontend with:
- Discover, watchlist and favorites views
- Watched/favorite state saved in localStorage
- Search, type/phase filters and sorting
- Light/dark mode and five accent themes (Stark, Wakanda, Asgard, Hulk, Spider-Verse, Sanctum)
- Editable release countdown
- Local admin preview for adding/deleting titles
- PWA manifest and service worker shell caching

## Run locally
Serve this folder over HTTP (service workers do not work from `file://`):
- VS Code Live Server, or
- `python -m http.server 8080`

Then open `http://localhost:8080`.

## Publish on GitHub Pages
Upload the contents of this folder to the repository root (or configure Pages to the folder containing `index.html`). Open the HTTPS Pages URL and use the browser's install option.

## Current preview limitations
Authentication is a local profile prompt, not secure sign-in. Admin preview changes only this browser. The catalog is a starter dataset and does not fetch live TMDB data yet. Cloud sync, secure roles, user management, metadata import and real multi-device accounts are intentionally deferred to the backend phase.

## Backend phase plan
1. Firebase Authentication (Google + email).
2. Firestore schema for titles, profiles, roles and per-user progress.
3. Firestore security rules and server-side admin authorization.
4. Express endpoints for TMDB metadata import; keep API secrets server-side.
5. Conflict-safe local/cloud sync and offline write queue.
6. Admin CRUD, user/role management and audit log.
7. Verified TMDB attribution and trailer/provider links.
