# Breakout Arcade 🎮

A complete, self-contained HTML5 Breakout (Arkanoid-style) arcade game built with vanilla JavaScript and Canvas. Runs instantly in any modern browser — no dependencies, no build step, no external assets.

## Features

- **Physics-based ball movement** with realistic paddle collision angles
- **6 rows × 10 columns of bricks** with alternating neon green/blue colors
- **Particle explosion effects** when bricks are destroyed
- **Web Audio API synthesizer** for retro sound effects (paddle hit, wall bounce, brick break, life lost, victory fanfare)
- **Progressive difficulty** — ball speed increases every 100 points
- **High score persistence** via localStorage
- **3 lives system** with visual indicators
- **Pause/Resume** (press `P` or click button)
- **Mouse and keyboard controls** (←/→ arrows or mouse movement)
- **Responsive overlay UI** for Start, Pause, Game Over, and Victory states

## Screenshot

![Breakout Game](breakout.html)

*Open `breakout.html` in any browser to play instantly.*

## Controls

| Input | Action |
|-------|--------|
| Mouse movement | Move paddle |
| ← / → Arrow Keys | Move paddle |
| Space / Click | Launch ball |
| P | Pause / Resume |

## How to Play

1. Open `breakout.html` in your browser
2. Click **"PRESS START"** or press **Space**
3. Move the paddle with your mouse or arrow keys
4. Launch the ball with **Space** or **Click**
5. Destroy all 60 bricks to win!
6. Ball speed increases every 100 points
7. Earn bonus points for remaining lives on victory

## Difficulty Tweaks

Edit these constants at the top of the `<script>` in `breakout.html`:

```javascript
const INITIAL_BALL_SPEED = 5;      // 4 = easier, 7+ = harder
const SPEED_INC_PER_100_PTS = 1;   // 0 = disable acceleration
const PADDLE_WIDTH = 100;          // 140 = easier, 70 = harder
// In startNewGame(): lives = 3;    // 5 = more forgiving
```

## Technical Details

- **Canvas**: 800×600 pixels
- **Paddle**: 100×15 px, neon green (`#00ff66`)
- **Ball**: 10 px radius, bright orange (`#ff6600`)
- **Bricks**: 60×20 px with 10 px gaps
- **Physics**: Fixed 60 FPS timestep via `requestAnimationFrame` + accumulator
- **Audio**: Web Audio API (no audio files needed)
- **Storage**: localStorage for high score

## Browser Compatibility

Works in all modern browsers (Chrome, Firefox, Safari, Edge) with:
- Canvas API
- Web Audio API
- localStorage
- requestAnimationFrame

## License

MIT — Free to use, modify, and distribute.

---

*Built with vanilla HTML/CSS/JS — no frameworks, no dependencies.*