# Human Pose Estimation Using YOLO11

## Overview
This assignment uses YOLO11 Pose and OpenCV to estimate human body pose from a video. It detects the COCO-17 body keypoints and creates a new video containing only a white skeleton on a black background.

## Repository contents
- `pose_estimation.ipynb` — Google Colab notebook with the complete implementation.
- `requirements.txt` — Python dependencies.

## Run in Google Colab
1. Open [pose_estimation.ipynb](https://colab.research.google.com/github/NishantKumar071/nlpassignment/blob/main/Pose-Estimation/pose_estimation.ipynb) in Google Colab.
2. Run the cells from top to bottom.
3. When prompted, upload your own video (for example, `nlpvideo(1).mp4`).
4. The notebook creates, previews, and downloads `skeleton_final.mp4`.

## How it works
1. YOLO11n-Pose detects human body keypoints in each video frame.
2. ByteTrack is enabled to maintain tracking across frames.
3. OpenCV creates a black frame and draws white keypoints and COCO skeleton connections.
4. FFmpeg converts the result to an H.264 MP4 video.

## COCO keypoints
The model predicts 17 keypoints: nose, eyes, ears, shoulders, elbows, wrists, hips, knees, and ankles.

## Notes
- The notebook processes the first detected person in each frame. It can be extended to draw every detected person.
- Keep the full body visible and well-lit for better keypoint detection.
- The input video is uploaded at runtime and is not committed to this repository.
- Google Colab normally provides FFmpeg. If it is unavailable, install it with `!apt-get -qq install ffmpeg`.

## Technologies
Python, Ultralytics YOLO11 Pose, OpenCV, NumPy, ByteTrack, FFmpeg, Google Colab.

## Author
Nishant Kumar
