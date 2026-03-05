# Real-Time Object Detection System using YOLO

## Project Description

The Real-Time Object Detection System is a machine learning project that uses the **YOLO (You Only Look Once)** deep learning algorithm to detect objects in images, videos, and live webcam streams. The system processes visual data and identifies objects by drawing bounding boxes and assigning class labels with confidence scores.

This project uses the **Ultralytics YOLO framework** and **PyTorch** for deep learning inference. It supports real-time detection and can process various input sources including images, videos, and live camera feeds.

The main goal of this project is to demonstrate how **computer vision and deep learning techniques** can be applied to automatically detect and classify objects in visual data.

---

## Project Requirements

### Hardware Requirements

| Component | Minimum Requirement   | Recommended Requirement      |
| --------- | --------------------- | ---------------------------- |
| Processor | Dual-Core 2.0 GHz     | Intel i5 / Ryzen 5 or higher |
| RAM       | 4 GB                  | 8 GB or higher               |
| Storage   | 10 GB free space      | 20 GB or higher              |
| Graphics  | Integrated GPU        | Dedicated GPU (optional)     |
| Display   | 1024 × 768 resolution | 1920 × 1080 resolution       |

### Software Requirements

* Python 3.10 (64-bit recommended)
* Git
* PyTorch
* Ultralytics YOLO
* OpenCV
* NumPy
* Pillow
* Matplotlib
* Requests
* PSUtil
* Polars

Recommended IDEs:

* Visual Studio Code
* PyCharm
* Jupyter Notebook

---

## Database Setup (Short Overview)

This project **does not require a traditional database**. Instead, the system uses:

* Pretrained YOLO model weights (`.pt` files)
* Input media files (images or videos)
* Output results stored locally

Detection results are automatically saved in the following directory:

```
runs/detect/
```

This folder stores processed images or videos with bounding boxes and detected object labels.

---

## How to Run the Project Locally

Follow the steps below to set up and run the project on your local machine.

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/ultralytics-object-detection.git
cd ultralytics-object-detection
```

### 2. Create a Virtual Environment

#### Windows

```bash
py -3.10 -m venv venv
.\venv\Scripts\activate
```

#### macOS / Linux

```bash
python3.10 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

Upgrade pip and install required libraries.

```bash
pip install --upgrade pip setuptools wheel
pip install numpy==1.26.4
pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
pip install pillow==10.3.0
pip install opencv-python==4.9.0.80
pip install ultralytics
```

### 4. Verify Installation

Run the following command to verify that YOLO is installed correctly.

```bash
yolo checks
```

---

## Running the Project

### Detect Objects in an Image

```bash
yolo predict model=yolo11n.pt source="image.jpg" device=cpu save=True
```

### Detect Objects in a Video

```bash
yolo predict model=yolo11n.pt source="video.mp4" device=cpu show=True save=True imgsz=480
```

### Real-Time Detection Using Webcam

```bash
yolo predict model=yolo11n.pt source=0 device=cpu show=True save=True imgsz=416
```

Press the window close button to stop the webcam detection.

---

## Output Results

Detection results are automatically saved in:

```
runs/detect/
```

Example output structure:

```
runs
 └── detect
      └── predict
           ├── image.jpg
           └── video.mp4
```

Each output file contains bounding boxes and object labels detected by the YOLO model.

---

## Key Features

* Real-time object detection
* Supports image, video, and webcam input
* High-speed detection using YOLO architecture
* Automatic result visualization
* Output saving for analysis

---

## Technologies Used

* Python
* PyTorch
* Ultralytics YOLO
* OpenCV
* NumPy
* Pillow

---

## Applications

* Smart surveillance systems
* Traffic monitoring
* Autonomous vehicles
* Security and safety systems
* Industrial automation

---

## Conclusion

This project demonstrates the power of **deep learning and computer vision** in building intelligent systems capable of analyzing visual data automatically. By leveraging the YOLO architecture, the system achieves **fast and accurate object detection** suitable for real-time applications.
