# Agent Instructions

## Project Shape

- This is a dependency-free static HTML5 Canvas game; there is no package manifest, bundler, test runner, linter, or build step.
- `index.html` is the browser entrypoint and loads `game.js` directly; `favicon.svg` is the only other runtime asset.
- `game.js` contains the entire game: input handling, entity classes, state transitions, update loop, rendering, and `requestAnimationFrame` startup. Preserve its section-based organization when changing it.
- The game world is fixed at `800x600` in both the canvas markup and `game.js`; movement wraps at both edges, so changes to dimensions must stay synchronized.

## Run And Verify

- For local development, run `npx serve .` from the repository root and open `http://localhost:3000`; opening `index.html` directly is also supported.
- There are no automated checks. After gameplay changes, manually verify loading, keyboard controls (`ArrowLeft`, `ArrowRight`, `ArrowUp`, `Space`), shooting, asteroid splitting, lives/game over, restart with Space, and level progression.
- Keep runtime code browser-native and dependency-free unless the repository gains an explicit manifest/build workflow.
