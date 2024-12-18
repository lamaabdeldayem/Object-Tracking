## YOLOv8 Object Detection and Tracking

This project demonstrates the use of the YOLOv8 model for real-time object detection and tracking in videos. It utilizes the **Ultralytics YOLOv8** model and **OpenCV** for video processing.

## Requirements

Before running the project, ensure that you have the following installed:

- Python 3.7+
- YOLOv8 (from `ultralytics`)
- OpenCV

### Install Dependencies

You can install the necessary dependencies using pip:

    < pip install ultralytics opencv-pythonx >

## Project Structure
1. yolov8n.pt – Pre-trained YOLOv8 model file.
2. test.mp4 – Sample video file for object detection and tracking (optional, can be replaced with your own video).
3. main.py – Python script that implements object detection and tracking using YOLOv8 and OpenCV.
## How to Run
1. Clone the repository or download the project files to your local machine.

2. Make sure that you have downloaded the YOLOv8 model weights yolov8n.pt from the Ultralytics YOLOv8 repository or use a different YOLOv8 model variant if needed.

3. Prepare a video or webcam input:

-Replace the video path in the script with your video file, or use 0 for webcam input.
4.Run the script:
```bash
python main.py

```
This will start processing the video, and it will display the frames with object detection and tracking results. Press q to exit the video window.

## Code Explanation
## -Model Loading: The YOLOv8 model is loaded using the following line:

python
```bash
model = YOLO('yolov8n.pt')
```
This loads the pre-trained YOLOv8 model that will be used for object detection and tracking.
## -Video Capture: A video is loaded using OpenCV's VideoCapture function:

````bash
cap = cv2.VideoCapture(video_path)
````
## -Object Detection & Tracking: Each frame of the video is processed in a loop where the YOLOv8 model detects and tracks objects in the frame:

```bash
results = model.track(frame, persist=True)
```
## -Visualization: The results are visualized using OpenCV's imshow function, which displays the frames with bounding boxes and object labels.

```bash
cv2.imshow('frame', frame_)
```
## Key Features
 -Object Detection: Detects objects in each frame of the video.
 -Object Tracking: Tracks the detected objects throughout the video.
 -Real-time Visualization: Displays the results on the screen with bounding boxes and labels.
 -Customizable: The script allows you to easily replace the video input or use a webcam for real-time detection.
## Known Issues
-If using a webcam, make sure that the correct camera is selected in the cv2.VideoCapture() function.

-The performance of the model may vary depending on the hardware.
