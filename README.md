# AICTE-Internship

# ♻️ Garbage Classification using YOLOv5

This project focuses on **automatic garbage classification** using the **YOLOv5 object detection model**. It is part of the AICTE Internship and aims to enhance smart waste management through computer vision.

---

## 📂 Project Structure

  -> AICTE-Internship/app.py: Streamlit or Flask web app
  
  -> data/: Additional config or test data
  
  -> Data_garbage/: Main dataset (images and labels for YOLOv5)
    
  ->images/:
      train/: Training images
      val/: Validation images
    labels/:
      train/: YOLO-format labels for training
      val/: YOLO-format labels for validation
    data.yaml: YOLOv5 data config file

  ->Dockerfile: Containerization instructions

  ->yolov5/: YOLOv5 repository (cloned or customized)

  ->wasteDetection/: Python package for detection logic

  ->wasteDetection.egg-info/: Metadata for package distribution

  ->templates/: HTML templates (used if app is Flask-based)

  ->template.py: Script for rendering or support logic

  ->setup.py: Python packaging setup script

  ->requirements.txt: Required Python dependencies

  ->LICENSE: Licensing information (e.g., MIT)

  ->.gitignore: Git exclusion rules

  ->README.md: Project documentation

  ->reseach/: Jupyter notebooks or experimental code


---
## 🧠 Model Overview

We use **YOLOv5** to classify waste items in real-time into the following categories:

- 📦 **Cardboard**  
- 🍾 **Glass**  
- 🛠️ **Metal**  
- 📄 **Paper**  
- 🧴 **Plastic**  
- 🚮 **Trash**

The model is trained on a labeled dataset stored in the `Data_garbage/` directory and integrated into an interactive app via `app.py`.

---

## 🚀 Setup Instructions

### 1. Clone the Repo

```bash
git clone https://github.com/yourusername/garbage-classification-yolov5.git
cd AICTE-Internship

2. Install Dependencies

pip install -r requirements.txt

3. Train the YOLOv5 Model
Make sure your dataset follows YOLO format (images + labels):

cd yolov5
python train.py --img 640 --batch 16 --epochs 50 --data ../Data_garbage/data.yaml --weights yolov5s.pt

4. Run the App

python app.py

---

📦 Dataset

Data_garbage/
├── images/
│   ├── train/
│   └── val/
├── labels/
│   ├── train/
│   └── val/
└── data.yaml

data.yaml :

train: ../Data_garbage/images/train
val: ../Data_garbage/images/val

nc: 6
names: ['cardboard', 'glass', 'metal', 'paper', 'plastic', 'trash']

---

🛠️ Technologies Used
Python 🐍

YOLOv5 by Ultralytics

Streamlit / Flask for Web App

OpenCV

Docker (for containerization)



---
###🧪 Future Work

-Real-time classification via webcam

-Mobile deployment (TensorFlow Lite or ONNX)

-Smart bin integration (IoT)


---
👩‍💻 Author
Rishika A S
Department of IT, St. Joseph’s Institute of Technology


---
📄 License
This project is licensed under the MIT License - see the LICENSE file for details.

