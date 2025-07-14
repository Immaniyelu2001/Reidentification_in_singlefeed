# Football Player Re-Identification using YOLOv11 and Deep SORT

## Objective
Track football players within a single video feed using a custom YOLOv11 object detector and Deep SORT tracker. Maintain consistent IDs even when players leave and re-enter the frame.

## Dependencies

Install required packages using:

```bash
pip install ultralytics deep_sort_realtime opencv-python supervision
```

## Files

- `player_tracking.py` – Main tracking script
- `15sec_input_720p.mp4` – Input video
- `best.pt` – YOLOv11 model trained to detect "player" and "ball"
- `output_video.mp4` – Output video with annotated tracks

## How to Run

1. Place `best.pt` and `15sec_input_720p.mp4` in the same folder.
2. Run the script:

```bash
python player_tracking.py
```

3. Output video will be saved as `output_video.mp4`.

## Notes

- Uses Deep SORT for consistent ID tracking.
- Only the "player" class is tracked (as detected by YOLOv11).
