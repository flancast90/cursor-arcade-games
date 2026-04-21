# Changelog

All notable changes to this project are documented here.
Format loosely follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [0.3.0] - 2026-04-19

This release adds the Arcade's first multiplayer game: **Head Soccer**.

### Added
- **Head Soccer** — 1P vs CPU or hotseat 2P. Two big-headed characters, one small ball, custom 2D physics with gravity/elasticity/collision. Ground kicks, air kicks, jumps, and a chargeable power shot.
- **Power-ups** drop into the field mid-match: **Fire** (next kick is a ripping shot that burns through defenders), **Ice** (next kick freezes the opponent on contact), **Giant** (head grows and gains more reach), **Multiball** (extra balls spawned for extra chaos).
- Match formats: configurable goals-to-win (1/3/5) and match-timer length (60/90/120s). First to the goal target or most goals when time runs out.
- Reactive CPU AI that chases, jumps, kicks, and uses power shots.
- In-browser self-test harness at `test/soccer-harness.html` for physics/kick/power-up regression testing (dev-only).

### Changed
- Menu hero copy now advertises five games instead of four.
- Added `soccer`, `head-soccer`, `multiplayer`, `2-player` keywords for marketplace discovery.

## [0.2.2] - 2026-04-19

### Changed
- Consolidated onto a single Marketplace identifier: `flancast90.cursor-snake`. The briefly-live `flancast90.cursor-arcade-games` listing on VS Code Marketplace has been retired. Going forward, all Arcade updates ship to the original `cursor-snake` extension URL (display name: **Cursor Arcade**). The GitHub repository remains at `flancast90/cursor-arcade-games`.

## [0.2.0] - 2026-04-19

This release rebrands the extension from **Monochrome Snake** into **Cursor Arcade** — a multi-game arcade collection with the same minimalist aesthetic.

### Added
- **2048** — slide/merge puzzle with smooth DOM tile animations, 4×4 / 5×5 / 6×6 board sizes, win-and-continue.
- **Blocks** — tetromino stacker with 7-bag randomizer, hold piece, ghost piece, wall kicks, standard line-clear scoring, and speed curves per level.
- **Minesweeper** — 9×9 / 16×16 / 24×16 difficulties, first-click-safe mine planting, flood reveal, flagging, and chord (middle-click or right-click on revealed number).
- Unified main menu with keyboard hotkeys (`1`–`4`) for each game.
- Per-game persistent high scores, keyed by mode/difficulty.
- Global dark/light theme toggle shared across every game.

### Changed
- Display name changed from **Monochrome Snake** to **Cursor Arcade**.
- Commands re-namespaced from `cursor-snake.*` to `cursor-arcade.*`.
- Single-panel webview now routes between the main menu and individual games with zero-latency teardown/mount.
- Design language tightened to pure monochrome across all games (previously Snake-only).

### Removed
- Standalone `snake.js` / `snake.css` bundled as top-level assets. Snake now lives as a module in `media/games/`.

## [0.1.2] - 2026-04-19
- Last Snake-only release under the "Monochrome Snake" display name.

## [0.1.0] - 2026-04-19
- Initial public release (Snake-only, display name *Monochrome Snake*).
- Nine modes, daily challenge, persistent high scores, buffered input queue.
