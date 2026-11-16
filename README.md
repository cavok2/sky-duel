# sky-duel
2D Browser Game

A 2D flight duel: one human player vs one computer opponent, shooting each other down.

## Play

Open `index.html` in any modern browser — the game is fully self-contained (no server, no dependencies, no build step). To serve it instead: `python3 -m http.server` and visit `http://localhost:8000`.

For a hosted version, enable GitHub Pages on this repo (Settings → Pages → Deploy from branch → `main` → `/`), then open the published URL.

## Controls

| Key | Action |
| --- | --- |
| WASD or Arrow keys | Fly |
| Space | Shoot |
| P | Pause |
| R | Restart (after a match ends) |

First plane to zero HP loses. Health bars are top-left (you) and top-right (CPU); your hit count is top-center.

## How it works

Everything lives in `index.html`: canvas rendering, plane physics, a computer opponent AI (orbits the player, strafes, dodges incoming fire, and aims with target-lead prediction), bullet collision, particles, screen shake, and WebAudio sound effects.
