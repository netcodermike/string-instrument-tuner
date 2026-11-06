# String Instrument Tuner

Chromatic microphone tuner with string presets, custom tunings, cents deviation, and reference tones.

**Language:** TypeScript · **License:** MIT · **Data:** Local by default

## What it does

- Chromatic live tuning
- Nine preset instrument families and arbitrary custom strings
- Adjustable concert pitch and reference tone

## Requirements

Node.js 22+ and npm; Python 3 for the optional local HTTP server.

## Install, validate, and run

```sh
npm install --ignore-scripts
npm test
npm start
```

Open http://127.0.0.1:8080 in a modern browser. TypeScript source compiles to `dist/` when running `npm test` or `npm run build`. Start audio with an explicit button click.

## Usage and examples

See [docs/usage.md](docs/usage.md) for a walkthrough and [docs/architecture.md](docs/architecture.md) for implementation details. Tests are deterministic and do not require an exchange, paid API, external model, microphone, or private data.

## Boundaries

Microphone requires HTTPS or localhost and permission. Monophonic periodic signals about 24–1400 Hz; harmonics and noise can reduce accuracy.

## Privacy

No analytics or accounts are built in. Local file tools process only the paths you supply. For model-server and weather apps, the interface and usage guide identify the destination and the data sent. Do not commit personal input files, model credentials, or generated recordings.

## Development

Run the validation commands above before submitting changes. GitHub Actions runs these checks on pushes and pull requests. See the workflow for the reproducible toolchain. A successful workflow verifies the tested paths; manual audio-device behavior is documented separately.
