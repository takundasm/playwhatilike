# PlayWhatILike 🎧

## What this is
PlayWhatILike is a web-based Spotify playlist generator that creates a custom playlist based on a user’s mood and activity.  
Users answer a short set of questions, and the app maps those answers to Spotify genre seeds to generate recommendations.

The frontend is hosted on GitHub Pages and built with vanilla HTML, CSS, and JavaScript.

---

## What works
- Interactive multi-step UI for collecting user mood/activity
- Mapping of answers to Spotify seed genres
- Playlist creation logic using Spotify Web API endpoints
- Track recommendation and playlist population logic

---

## What doesn’t (yet)
- Authentication is currently blocked by Spotify OAuth constraints
- Spotify has deprecated the Implicit Grant flow
- Token exchange cannot be completed without additional setup

---

## Why it’s unfinished
This project ran into an API limitation:
- Spotify no longer supports `response_type=token` and enforces stricter OAuth rules for public (frontend-only) clients.
- Frontend-only authorization now requires Authorization Code Flow with PKCE (in the process of learning how this works).


Completing authentication now requires either:
- Implementing PKCE end-to-end, or
- Adding a backend service to securely exchange authorization codes for access tokens

---

## Next steps
- Implement Authorization Code Flow with PKCE **or**
- Add a lightweight Python backend (e.g. PythonAnywhere) for token exchange
- Add token refresh handling
- Improve genre selection logic using all user answers
- Polish UI/UX

---

## Tech stack
- HTML / CSS / JavaScript
- Spotify Web API
- GitHub Pages (hosting)

---

## Status
🚧 Work in progress — blocked by OAuth flow changes, actively learning and refactoring.
