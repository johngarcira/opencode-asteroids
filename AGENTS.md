# Agent Guide

## Project Shape

- This is a dependency-free static HTML5 Canvas game; there is no package manifest, bundler, test suite, linter, or build step.
- `index.html` is the browser entrypoint and loads `game.js` plus `favicon.svg`; `game.js` contains the complete game state, input handling, update loop, rendering, entities, collisions, and scoring.
- The canvas and game coordinates are fixed at 800x600 (`index.html` and `game.js`); change both locations together if the resolution changes.
- Treat `index.html` and `game.js` as the executable source of truth. The README mentions features such as power-ups that are not implemented in the current code.

## Run And Verify

- Open `index.html` directly, or run `npx serve .` and visit `http://localhost:3000`.
- There are no automated checks to run. Verify gameplay manually in a browser, including movement, shooting, asteroid collisions/splitting, level progression, and Space-to-restart after game over.

## Change Boundaries

- Keep the game dependency-free and browser-native unless the task explicitly requires introducing tooling; all runtime code currently belongs in `game.js`.
- Preserve the existing Spanish user-facing labels unless the requested change includes localization or copy changes.
