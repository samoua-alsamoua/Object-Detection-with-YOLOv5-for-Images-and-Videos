# Object Detection using YOLOv5

This project aims to **detect objects** on images and videos using the **YOLOv5** model pre-trained on the COCO dataset.

---

## Features
- **Object Detection**: Detect objects in images and videos using YOLOv5.
- **COCO Dataset**: The model is pre-trained on the COCO dataset, which includes 80 object categories.
- **File Upload**: Supports uploading images and videos directly in Google Colab.
- **Output**: Saves the processed image or video with bounding boxes and labels.

## Setup

### 1. Requirements
- Python 3.x
- Google Colab (or a local environment with GPU support)
- Required Python libraries:
  ```bash
  pip install torch torchvision opencv-python matplotlib ultralytics
  ```

### 2. Google Colab Setup
1. Open Google Colab: [https://colab.research.google.com/](https://colab.research.google.com/).
2. Upload the script or copy and paste the code into a new notebook.
3. Ensure you are using a GPU:
   - Go to `Runtime` > `Change runtime type` > Select `GPU` under Hardware accelerator.

---

## Usage

### 1. Running the Script
1. Run the script in Google Colab.
2. Choose a task:
   - **1**: Process an image.
   - **2**: Process a video.
3. Upload an image or video file when prompted.
4. View the results.

### 2. Example Input
- **Image File**: Upload a `.jpg` or `.png` file for object detection.
- **Video File**: Upload a `.mp4` file for object detection.

### 3. Example Output
- **Image Output**:
  - The processed image will be saved as `output_image.jpg` and displayed in Colab.
  - Bounding boxes and labels will be drawn on the detected objects.

- **Video Output**:
  - The processed video will be saved as `output_video.mp4`.
  - Bounding boxes and labels will be drawn on the detected objects in each frame.

---

## Code Overview

### 1. Model Loading
- The **YOLOv5** model is loaded using `torch.hub.load('ultralytics/yolov5', 'yolov5s', pretrained=True)`.
- The model is pre-trained on the **COCO dataset** and supports 80 object categories.

### 2. Object Detection
- The `detect_objects()` function performs object detection on an image.
- It uses a confidence threshold (`0.5` by default) to filter out weak predictions.

### 3. Image Processing
- The `process_image()` function processes an image, draws bounding boxes and labels, and saves the output.

### 4. Video Processing
- The `process_video()` function processes a video frame by frame, draws bounding boxes and labels, and saves the output.

### 5. File Upload in Colab
- The `files.upload()` function allows users to upload images or videos directly in Google Colab.

---

## Supported Object Categories
The YOLOv5 model supports 80 object categories, including:
- `person`, `car`, `bicycle`, `dog`, `cat`, `bus`, `truck`, `traffic light`, `stop sign`, etc.

For a full list of supported categories, refer to the [COCO dataset documentation](https://cocodataset.org/#home).

---

## Limitations
- The model may not detect very small or highly occluded objects.
- Large input images or videos may take longer to process.
- The model's maximum input size is limited by GPU memory.

---

## Contact
- **Author**: Samoua Alsamoua
- **GitHub**: [samoua-alsamoua](https://github.com/samoua-alsamoua)
- **Website**: [saalsamoua.github.io](https://samoua-alsamoua.github.io/saalsamoua/)
```
