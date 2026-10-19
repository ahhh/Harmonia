# Harmonia

A relaxation instrument for the browser. It plays an endless, slowly changing chord journey made from well-loved progressions. The progressions walk around John Coltrane's circle of fifths. Binaural beats, soft bells, breath-synced noise and a field of color move in harmony with the music.

Modeled on [Lull](https://super-kataifi-2aab11.netlify.app/). The progressions come from *The Coltrane Circle* (`../circle_progression`) and the color harmonies come from *Color Wheel Studio* (`../color-wheel`).

## How it works

- **Journey.** A seeded generator picks a progression (weighted toward calm ones), plays it two or three times, then moves the key. The key steps by a fifth, or along Coltrane's major-third triangle, before the next progression starts. Chords are voice-led so each tone moves as little as possible. Every journey has a number, and `#j=1234` in the URL replays the same one.
- **Sound.** A detuned pad with a slowly sweeping filter, a sine bass, sparse bell tones, reverb and brown, pink or "ocean" noise. Everything runs in the Web Audio API, with no audio files.
- **Binaural beats.** Each ear gets its own sine wave, either at the chord root or at 136.1 Hz ("Om"). The two differ by delta, theta, Schumann (7.83 Hz) or alpha. They can also drift down from alpha over the session. Headphones are required.
- **Breath.** Coherent (5.5 / 5.5), box (4-4-4-4) or 4-7-8 breathing. The pad and noise swell on the in-breath, and a halo around the circle guides you.
- **Color.** Each pitch class has a hue: its position on the circle of fifths, or its chromatic position, times 30°. A chord becomes a constellation of hues, which can be the chord's own notes or a Color Wheel Studio harmony built on the root (analogous, triadic, golden angle and others). The background glides between chords and never flashes.
- **Mandala.** Each finished progression stays on the circle as a faint figure, so the session slowly draws a pattern.
- **Immerse.** Full screen, keeps the screen on, and hides the controls. Double-tap or press Esc to return.

Keyboard: Space to play or pause, N for a new journey, I for immerse.

## Running and hosting

There's no build step. Open `index.html` in a browser, or run `python3 -m http.server`.

For GitHub Pages: push the repo, then go to **Settings → Pages**, choose **Deploy from a branch** and pick `main` / `(root)`.

Settings are saved in `localStorage`.
