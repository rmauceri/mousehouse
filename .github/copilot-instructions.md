# Mousehouse — Copilot Instructions

Mousehouse is a cozy children's dollhouse/pet simulator, built as a birthday gift. Single HTML file (`index.html`), zero dependencies, runs entirely in the browser.

## Running

Open `index.html` directly in a browser. No build step, no server required.

## Architecture

Flat structure with a top-level `game` / `gameState` object and a `requestAnimationFrame` game loop:

```
CONFIG              — mouse names, twin names, birthday message, initial coins, item catalog
Game state object   — room, mice, furniture, inventory, happiness, goals, coins
Input handlers      — click/tap on furniture, mice, shop items
Game loop           — update mouse AI → tick timers → render current room
Render functions    — room backgrounds, furniture sprites, mouse sprites, HUD, speech bubbles
LocalStorage        — save/load full game state
```

## Personalisation — edit CONFIG first

The `CONFIG` object at the top of `index.html` controls all the gift-specific content:
- Mouse names (default: Shadow, Cloud)
- Twin names (default: Nico, Rose)
- Birthday message shown on first load
- Starting coin balance and birthday bonus (100 coins on first run)

**Always edit CONFIG for name/message changes rather than hunting through render code.**

## Rooms and items

- **3 rooms**: Bedroom, Kitchen, Living Room — each with its own background and furniture slots
- **20+ decoration items**: matchbox bed, thimble cup, fairy lights, acorn shelf, etc.
- Items are purchased from the **Moustazon Prime** shop using coins and placed in rooms

## Mice AI and personality

- 2 mice with distinct personalities (gen-Z humor, distinct speech bubble lines)
- Behavior: wander room, interact with placed furniture, approach each other, react to player taps
- Happiness system: rises when mice interact with furniture they like, decays over time
- Goals system: completing goals earns bonus coins

## Mini-games

- **Cheese Chase** — side-scrolling runner; mouse dodges obstacles to collect cheese
- **Doomscroll** — social media parody; tap/swipe mechanic

## Conventions

- **No external dependencies** — never add a CDN link, import, or network call.
- **Warm, cute aesthetic** — color palette: purples, soft greens, warm oranges. Pixel-art-adjacent mouse sprites. All copy should match the gen-Z / cozy-cute tone of the existing speech bubbles.
- **Canvas for gameplay, DOM for UI** — rooms and mice render on `<canvas>`; shop, HUD, and modals use DOM/CSS.
- **Touch-first** — designed for phones; all interactions via tap/swipe.
- **LocalStorage** — full game state saved on every meaningful action. Key prefix: `mousehouse_`.
- **Offline-first** — no network calls, no CDN.
- **`build-prompts.md`** documents the 10-phase incremental build history — useful for understanding why features are layered the way they are before making structural changes.

## Commits

All commits in this repo include:
```
Co-authored-by: Copilot <223556219+Copilot@users.noreply.github.com>
```
