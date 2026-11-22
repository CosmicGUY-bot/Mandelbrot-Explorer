# Mandelbrot Explorer

An interactive Mandelbrot set viewer that runs in your browser. One HTML file, no dependencies, no build step.

**Vibe coded with [Claude](https://claude.ai):** I described the project and Claude wrote the code. I then read through it to understand the math.

## Run it

Open `index.html` in any modern browser.

## Use it

- **Click or tap** the picture to zoom in on that point.
- **Mouse wheel** zooms in and out around the cursor.
- **Zoom out** and **Reset** buttons move you back.
- **Detail** raises the iteration count. Increase it when you zoom deep and the picture turns blurry.
- **Colors** switches between three palettes.

## The math

For each point `c` in the complex plane, start with `z = 0` and repeat:

```
z → z² + c
```

If `|z|` stays bounded forever, `c` belongs to the Mandelbrot set (drawn black). Otherwise, the number of steps before `|z|` escapes decides the color. A smooth coloring formula based on `log(log|z|)` removes the visible color bands.

## Places to explore

Type these into the code (`cx`, `cy` in `reset()`) or zoom in by hand:

| Name | Center | Zoom width |
|------|--------|-----------|
| Seahorse Valley | -0.745 + 0.113i | 0.01 |
| Elephant Valley | 0.275 + 0.007i | 0.02 |
| Mini Mandelbrot | -1.768 + 0.002i | 0.01 |

## Ideas to extend

- Add a Julia set mode (`z → z² + c` with a fixed `c` and a varying starting `z`).
- Render in a Web Worker for faster deep zooms.
- Add a button to download the current picture as a PNG.

## Host it for free

1. Push this repo to GitHub.
2. Go to **Settings → Pages**.
3. Choose branch `main` and `/ (root)`, then save.
4. Your site will be at `https://<your-username>.github.io/<repo-name>/`.

## License

MIT, see [LICENSE](LICENSE).
