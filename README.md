# web-slide-fps

Browser-based high-mobility FPS prototype (Three.js + TypeScript + WASM Rapier3D + Geckos.io WebRTC), built with Devin Bots.

## Week 1 MVP Scope (PR #1)
- Fixed 60Hz (`dt = 1/60`) headless Rapier3D simulation (`src/sim/`)
- Kinematic sprint-slide movement with ramp slope acceleration
- Hitscan rifle + 100 shield / 100 HP dummy target with 3s respawn
- Vitest deterministic movement & combat assertions before PR merge
