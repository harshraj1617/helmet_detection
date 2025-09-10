# 🪖 Helmet Detection using YOLOv11 & OpenCV  

## 📌 Overview  
This project implements a **real-time helmet detection system** using **YOLOv11** and **OpenCV**.  
It can:  
- Detect **multiple persons** in a single frame  
- Draw **bounding boxes** around detected objects  
- Classify whether a person is **wearing a helmet** or **not wearing a helmet**  
- Work in **real-time** using a webcam feed or video input  

Helmet detection is crucial for **road safety**, **construction sites**, and **workplace compliance monitoring**.  


## ⚙️ Features  
✅ Real-time detection using webcam/video  
✅ YOLOv11 trained on custom dataset  
✅ Bounding boxes with class labels (`Helmet` / `No Helmet`)  
✅ Detects **multiple people** at once  
✅ Fast and efficient using GPU/CPU  



## 🚀 Installation  

### 1. Clone the repository  
```bash
git clone https://github.com/your-username/helmet-detection-yolov11.git
cd helmet-detection-yolov11
```

### 2. Create virtual environment (optional but recommended)  
```bash
python -m venv yolov11_env
source yolov11_env/bin/activate   # Linux/Mac
yolov11_env\Scripts\activate     # Windows
```

### 3. Install dependencies  
```bash
pip install ultralytics opencv-python numpy
```

---

## 📂 Project Structure  
```
helmet-detection-yolov11/
│-- models/                # YOLOv11 weights (helmet detection model)
│   └── best.pt
│-- helmet_detection.ipynb           # Main script for live detection
│-- requirements.txt       # Dependencies
│-- README.md              # Documentation
```

---

## ▶️ Usage  

### Run live detection with webcam:  
```bash
python helmet_detection.ipynb
```

### Run detection on a video file:  
```bash
python helmet_detection.ipynb --video path/to/video.mp4
```


## 🖼️ Example Output  
- **Green box + "Helmet"** → Person is wearing helmet  
- **Green box + "without Helmet"** → Person is not wearing helmet  

The model will annotate each frame in real-time:  

```
[ Helmet ] - with bounding box ✅
[ No Helmet ] - with bounding box ❌
```


## Dataset & Training  
- Trained on a **custom helmet detection dataset**  
- Model: **YOLOv11** (Ultralytics)  
- Optimized for real-time inference  

If you want to **train your own model**, run:  
```bash
yolo detect train data=data.yaml model=yolov11.pt epochs=50 imgsz=640
```

---

## 🏗️ Future Improvements  
- Improve dataset diversity (motorbikes, construction workers, different angles)  
- Dataset was limited due to computational and resource limitations further if applied on industry level can be fruther improved 
- Deploy as a **Flask/Django web app** or **mobile app**  


## 🙌 Acknowledgements  
- [Ultralytics YOLOv11](https://github.com/ultralytics/ultralytics)  
- [OpenCV](https://opencv.org/)  



## 📜 License  
This project is licensed under the **MIT License** – feel free to use and modify.  
