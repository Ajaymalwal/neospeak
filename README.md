# NeoSpeak

NeoSpeak is a modern, single-page Text-to-Speech (TTS) web app built with the Web Speech API.

## Features

- Speak text directly in the browser
- Language selection based on available system/browser voices
- Voice dropdown filtering by:
  - Selected language
  - Selected gender (`Female` / `Male`)
- Voice presets (male/female modes) with automatic rate and pitch tuning
- Manual controls for:
  - Rate
  - Pitch
- Playback controls:
  - Speak
  - Pause
  - Resume
  - Stop
- **Get More Voices** helper button with OS guidance for installing additional system voices

## How it works

NeoSpeak uses the browser's built-in `speechSynthesis` engine. Voices come from your operating system and browser, so available voices vary by device.

## Run locally

Because this is a static page, you can run it in either of these ways:

1. Open `index.html` directly in a modern browser (Chrome/Edge recommended), or
2. Serve the folder with any static server.

Example with VS Code Live Server or any local HTTP server is fine.

## Usage

1. Enter or paste text in the input area.
2. Choose `Language`, `Voice`, and `Gender`.
3. Optionally pick a preset voice mode.
4. Adjust `Rate` and `Pitch` as needed.
5. Click **Speak**.
6. Use **Pause / Resume / Stop** to control playback.

## Install more voices

Use the **Get More Voices** button in the app:

- On Windows: opens speech settings guidance (`ms-settings:speech` may open automatically)
- On macOS/Linux: shows steps to install voices from system settings

After installing voices, restart browser and refresh the page.

## Limitations

- Voice quality and availability depend on OS + browser.
- Gender filtering relies on voice-name heuristics provided by the platform.
- Browsers do not allow direct in-app downloading of system voice models through Web Speech API.

## Known Issues / Troubleshooting

- **Voices not showing up initially**: Wait 1–2 seconds, then refresh the page. Some browsers load voices asynchronously.
- **Only a few voices appear**: Install more system voices using **Get More Voices**, then fully restart the browser.
- **No speech output**: Confirm browser tab audio is not muted and system output device is correct.
- **Gender filter seems limited**: Voice names are platform-defined; if names have no gender hints, filtering falls back to available language voices.

## Tech

- HTML
- CSS
- Vanilla JavaScript
- Web Speech API (`speechSynthesis`, `SpeechSynthesisUtterance`)

## License

No license file is currently included in this repository.
