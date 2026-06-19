# Air Draw

A mini-app for drawing with your finger in the air in front of a camera. The trail appears on screen as a glowing neon line — fully gesture-controlled.

## Run locally

Requires a local server (camera won't work with `file://`):

```bash
python3 -m http.server 8080
```

Open [http://localhost:8080/air-draw.html](http://localhost:8080/air-draw.html).

## Gestures

| Gesture | Action |
|---------|--------|
| Index finger (rest in fist) | Draw |
| Fist | Erase |
| ✌️ Victory | Change color |
| 🖐️ Open palm ~1.5s | Clear canvas |
| 👍 Thumbs up | Save drawing |

## Technical

- [MediaPipe Hand Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker) — `numHands: 1`, `runningMode: VIDEO`
- Gesture detection via tip/pip heuristics (no ML classifier)
