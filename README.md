# SnakeMania

The snake game, with a difficulty setting that actually changes the speed and a high score that survives a reload.

**Live:** https://snakemania-37281.web.app

## Features

- **Three difficulty settings** — the snake moves faster as you raise it
- **Score** that increases by 10 per food eaten
- **High score persisted in `localStorage`**, so your best run is still there next time
- **Food regenerates** at a new random cell each time it is eaten
- **Self-collision and wall collision** end the run
- **Keyboard controls** with arrow keys

## How it works

`Js/script.js` runs the game on a fixed-interval tick. Each tick moves the snake one cell in the current direction, then:

1. If the head lands on the food, the score goes up by 10, the tail is not removed (so the snake grows), and new food is placed.
2. If the head lands on the body or outside the board, the run ends and the high score is compared and saved.

The difficulty setting changes the tick interval, which is why a higher setting is genuinely harder rather than just labelled that way.

## Tech

Plain HTML, CSS and JavaScript. No framework, no build step, no dependencies.

## Run locally

```bash
npx serve .
# or
python -m http.server 8080
```

Then open http://localhost:8080 and pick a difficulty.

## Deploy

```bash
firebase deploy --only hosting --project snakemania-37281
```

## License

MIT — see [LICENSE](LICENSE).
