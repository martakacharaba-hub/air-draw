# Air Draw

Міні-застосунок для малювання пальцем у повітрі перед камерою. Слід з'являється на екрані як світловий неоновий trail — керування повністю жестове.

## Запуск

Потрібен локальний сервер (камера не працює з `file://`):

```bash
python3 -m http.server 8080
```

Відкрий [http://localhost:8080/air-draw.html](http://localhost:8080/air-draw.html).

## Жести

| Жест | Дія |
|------|-----|
| Вказівний палець (решта в кулаку) | Малювання |
| Кулак | Стерти |
| ✌️ Victory | Змінити колір |
| 🖐️ Долоня ~1.5с | Очистити canvas |
| 👍 Like | Зберегти малюнок |

## Технічно

- [MediaPipe Hand Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker) — `numHands: 1`, `runningMode: VIDEO`
- Евристики розпізнавання жестів по tip/pip координатах (без ML-класифікатора)
