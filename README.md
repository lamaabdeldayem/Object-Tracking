
---

# YOLOv8 Object Detection and Tracking 🚀

This project demonstrates the use of the **YOLOv8 model** for **real-time object detection and tracking** in videos. It utilizes the **Ultralytics YOLOv8** model and **OpenCV** for video processing.

---

## 📝 Requirements

Before running the project, ensure that you have the following installed:

- Python 3.7+
- YOLOv8 (from `ultralytics`)
- OpenCV

### 📦 Install Dependencies

Install the necessary dependencies using `pip`:

```bash
pip install ultralytics opencv-python
```

---

## 🗂️ Project Structure

1. **yolov8n.pt** – Pre-trained YOLOv8 model file.
2. **test.mp4** – Sample video file for object detection and tracking (optional, can be replaced with your own video).
3. **main.py** – Python script implementing object detection and tracking using YOLOv8 and OpenCV.

---

## 🚀 How to Run

1. **Clone the repository** or download the project files to your local machine.

2. Ensure you have the **YOLOv8 model weights** (`yolov8n.pt`) downloaded from the **Ultralytics YOLOv8 repository**, or use a different YOLOv8 model variant if needed.

3. **Prepare a video or webcam input**:
   - Replace the video path in the script with your video file, or use `0` for webcam input.

4. **Run the script**:

   ```bash
   python main.py
   ```

   This will start processing the video, displaying the frames with object detection and tracking results. Press `q` to exit the video window.

---

## 🧑‍💻 Code Explanation

### - Model Loading

The YOLOv8 model is loaded with the following line:

```python
model = YOLO('yolov8n.pt')
```

This loads the pre-trained YOLOv8 model for object detection and tracking.

### - Video Capture

A video is loaded using OpenCV's `VideoCapture` function:

```python
cap = cv2.VideoCapture(video_path)
```

### - Object Detection & Tracking

Each frame of the video is processed in a loop where the YOLOv8 model detects and tracks objects:

```python
results = model.track(frame, persist=True)
```

### - Visualization

The results are visualized using OpenCV's `imshow` function, which displays the frames with bounding boxes and object labels:

```python
cv2.imshow('frame', frame_)
```

---

## 🛠️ Key Features

- **Object Detection**: Detects objects in each frame of the video.
- **Object Tracking**: Tracks detected objects throughout the video.
- **Real-time Visualization**: Displays the results on the screen with bounding boxes and labels.
- **Customizable**: Easily replace the video input or use a webcam for real-time detection.

---

## ⚠️ Known Issues

- When using a webcam, ensure that the correct camera is selected in the `cv2.VideoCapture()` function.
- The performance of the model may vary depending on the hardware.

---
