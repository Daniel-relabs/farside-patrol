# Farside Patrol

Farside Patrol is a single-file, first-person 3D space-combat game. Patrol an alien sector from a fully rendered cockpit, clear escalating waves of raiders, and spend earned pennies on ship upgrades.

## Run locally

No packages, build step, or asset download are required. Serve the repository with any static file server:

```sh
python3 -m http.server 8000
```

Then open [http://localhost:8000](http://localhost:8000) in a current desktop or mobile browser with WebGL enabled. The game loads Three.js and post-processing shaders from public CDNs, so an internet connection is required for those dependencies.

## Play

- **W / S**: increase throttle / stop
- **A / D**, **arrow keys**, **Q / E**: steer, pitch, and roll
- **Space**: fire manually; auto-fire is available when a raider is in your sights
- **Shift**: boost
- **F**: guided missile
- **H**: heavy missile
- **J**: jump to the next sector
- **X**: eject to restore the hull
- **P**: pause
- **V**: exterior view
- **G**: toggle high-quality graphics

On touch devices, drag on the left side of the screen to steer and use the on-screen Fire, Boost, Missile, and Heavy controls.

## Features

- Procedural planets, starfield, cockpit instrumentation, weapons, explosions, audio, and optional bloom/film-grade effects.
- Escalating enemy waves, including aces and missile-equipped hunters.
- A hangar with a customizable pilot name and picture.
- Persistent high score, pennies, and upgrades stored in the browser with `localStorage`.
- Solo play in any supported browser.

## Multiplayer

The hangar can create or join numbered servers in the published game host. This feature relies on the host-provided `window.claude.use('room')` API, so it is intentionally unavailable from a normal local static server. Local play remains fully functional.

## Project layout

| Path | Description |
| --- | --- |
| `index.html` | The complete game: HTML, CSS, game logic, and rendering code. |

## Browser requirements

Use a modern browser with WebGL and Web Audio support. Sound begins after the first interaction, as required by browser autoplay policies.