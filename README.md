# Bluesharp Trainer

Practice tool for diatonic / blues harmonica (10-hole Richter tuning).
Sibling project to [Harmonica Trainer (chromatic)](https://github.com/aiandylatam/harmonica-trainer).

**Live:** https://aiandylatam.github.io/bluesharp-trainer/

## Status — v0.1 (MVP)

Single-page web app. What it does so far:

- **Scales mode** with the 10-hole Richter layout
  - Blow / Draw rows + bend rows (Blow ♭, Blow ♭♭, Draw ♭, Draw ♭♭, Draw ♭♭♭)
  - Bend cells gold-rimmed; empty bend cells render as placeholders so the grid stays aligned
- **Harp key selector** (12 keys: C, C♯, D, D♯, …, B) — transposes the whole layout
- **Position selector** (1st through 5th plus 12th — straight harp, cross harp, slant, etc.) — shifts the scale tonic relative to the harp's key
- **13 scales** — Major, Natural / Harmonic / Melodic minor, Pentatonics, Blues, Modes, Chromatic
- **Live mic pitch detection** with cents-accurate tuner; matched notes light up on the harp
- **17 instrument tones** — synth + GM-style soundfont samples (Harmonica, Flute, Trumpet, Sax, etc.)
- **A4 reference pitch** adjustable 415–466 Hz
- Settings persist in localStorage

## Roadmap

Planned for later phases:

- **Bending trainer** — pick a target bend, mic feedback on how close you are (the killer Bending Trainer feature)
- **Tabs mode** — visual editor for blues tabs (+1, -2, -3', -3", etc.)
- **Practice mode** — load MIDI / pre-loaded blues songs, see them in tabs + staff
- **Game mode** — Guitar Hero style for harp
- **Overblows / overdraws** — advanced reed control
- **Additional tunings** — Country, Paddy Richter, Spiral, Lee Oskar Melody Maker
- **Circle of Fifths** widget

## Tech

Single standalone `index.html`. Vanilla JS, no build step. Web Audio for synthesis and mic pitch detection (autocorrelation, ACF2+). Google Fonts for Space Grotesk + JetBrains Mono + Noto Music. Soundfont samples via gleitz/midi-js-soundfonts (CDN).

## Local dev

Open `index.html` in any modern browser. Microphone access requires HTTPS or `localhost`.

```bash
python -m http.server 8000
# → http://localhost:8000
```

## Credits

Bootstrapped from the [Harmonica Trainer chromatic codebase](https://github.com/aiandylatam/harmonica-trainer). Inspired by Harmonica Bending Trainer (blowbend) and Let's Bend (open source) for the blues-harp practice patterns.
