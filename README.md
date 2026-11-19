# Presenter Camera

A single-page web app that shows your webcam in a floating, always-on-top picture-in-picture window, which is handy for presenting or recording a screen with yourself in the corner. It can blur or replace the background behind you.

Everything runs in your browser. Video never leaves your computer.

## Features

- **Picture-in-picture**: pop the camera out into a small window that stays on top of other apps. In Chrome and Edge it's resizable and keeps all effects.
- **Background blur or image replacement**, using MediaPipe's selfie segmentation models.
- **Capture background**: step out of frame to snapshot the empty room, which helps separate you from similar-coloured surroundings.
- **Tuning controls** for outline tightness, smoothing, edge softness and more, each with a tooltip explaining it.
- **Remembers everything** across reloads: settings, background image and captured background are stored in your browser.

## Run it

Browsers only allow camera access on `https://` or `localhost`, so serve the folder locally:

```sh
python3 -m http.server 8000
```

Then open <http://localhost:8000>.

## Browser support

- **Chrome / Edge**: everything works best here.
- **Safari**: picture-in-picture works; blur and edge softening may not render.
- **Firefox**: no picture-in-picture button. Use Firefox's own PiP toggle on the video instead.

The segmentation library and models load from jsDelivr and Google's model storage the first time you turn on a background effect, so that step needs an internet connection.
