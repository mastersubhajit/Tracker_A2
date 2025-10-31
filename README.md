
# 🧠 Computer Vision Project — Image Classification, Object Detection & Tracking

## 📘 Overview
This repository contains three comprehensive notebooks demonstrating key computer vision techniques — **image classification**, **object detection**, and **object tracking** — using both deep learning and traditional computer vision algorithms.

Each task includes implementation, evaluation, and visualization, with comparative performance analysis based on real experimental results.

---

## 🔹 Task 1: Image Classification with CNNs

### 🧾 Objective
To design and compare multiple CNN architectures on the **CIFAR-10** dataset (10 object classes, 60,000 images).

### ⚙️ Implementation
Implemented using **PyTorch**, four model configurations were trained and evaluated:

| Model | Optimizer + Scheduler | Test Accuracy (%) |
|:--|:--:|:--:|
| **ResNet18** | SGD + StepLR | **90.04** |
| **CNN** | Adam + ReduceLR | 86.10 |
| **ResNet18** | Adam + ReduceLR | 86.09 |
| **CNN** | SGD + StepLR | 82.37 |

### 🧩 Experimentation Details
- Compared optimizers: **SGD vs Adam**  
- Evaluated learning rate schedulers: **StepLR** and **ReduceLROnPlateau**  
- Conducted experiments on multiple architecture–optimizer combinations  

### 📊 Visualizations
- Accuracy/Loss curves for training and validation  
- Confusion matrices for class-level performance  
- Misclassified example images  
- Activation maps (Conv Layer 1 and 2) for ResNet and Custom CNN  

### 💬 Discussion
The **ResNet18 with SGD + StepLR** achieved the **highest accuracy (90.04%)** and most stable convergence.  
Adam converged faster but plateaued earlier. The baseline CNN underperformed slightly due to its limited depth and capacity.

---

## 🔹 Task 2: Object Detection

### 🧾 Objective
To evaluate and compare a **two-stage detector (Faster R-CNN)** and a **single-stage detector (YOLOv8n)** on a common dataset.

### ⚙️ Models
- **Two-stage:** Faster R-CNN (TorchVision pretrained on COCO)  
- **Single-stage:** YOLOv8n (Ultralytics implementation)

### 🧩 Dataset
- **Pascal VOC 2007** subset used for evaluation.  
- Uniform preprocessing and same test samples for both models.

### 📈 Results

| Metric | Faster R-CNN | YOLOv8n |
|:--|:--:|:--:|
| **mAP@0.5** | 0.62 | **0.68** |
| **FPS (Inference Speed)** | 3.62 | **12.93** |
| **Model Size (MB)** | 167 | **6.25** |

### 🧠 Visualizations
- Detection bounding boxes on sample test images  
- Precision-recall and mAP curves  
- Side-by-side comparison of inference outputs  

### 💬 Discussion
YOLOv8n provided **higher inference speed (≈13 FPS)** and smaller size (≈6 MB) while maintaining competitive accuracy.  
Faster R-CNN achieved slightly higher precision but at the cost of speed and resource usage.  
For real-time deployment, **YOLOv8n** is preferred; for high-precision offline detection, **Faster R-CNN** excels.

---

## 🔹 Task 3: Object Tracking

### 🧾 Objective
To implement and analyze classical **OpenCV tracking algorithms** on video data.

### ⚙️ Trackers Used
- **MOSSE**  
- **KCF (Kernelized Correlation Filter)**  
- **CSRT (Channel and Spatial Reliability Tracker)**  

### 🧩 Dataset
Short video clips (pedestrian and vehicle scenes) from **Pexels** and **MOT Challenge** datasets.  
Each tracker was initialized with a bounding box and evaluated over full sequences.

### 📈 Results

| Tracker | Average FPS | Success Rate (%) | Frames Tracked | Total Frames |
|:--|:--:|:--:|:--:|:--:|
| **MOSSE** | **60.00** | **66.00** | 524 | 794 |
| **KCF** | 59.91 | 0.80 | 3 | 373 |
| **CSRT** | 46.06 | 35.30 | 212 | 601 |

### 🎥 Visual Outputs
- Video overlays with tracker bounding boxes  
- Frame-by-frame comparison of stability and drift  
- Failure cases (occlusion and re-detection)

### 💬 Discussion
- **MOSSE** offered the **highest speed (60 FPS)** and moderate accuracy — ideal for real-time low-power systems.  
- **CSRT** delivered the **most stable tracking** under occlusion but was slower (~46 FPS).  
- **KCF** struggled under occlusion and scale variation, with very low success rate in this setup.

---

## 📂 Repository Structure

```
├── Task1.ipynb     # Image Classification with CNNs (PyTorch)
├── Task2.ipynb     # Object Detection (Faster R-CNN & YOLOv8)
├── Task3.ipynb     # Object Tracking (OpenCV)
├── data/           # Datasets (excluded from Git tracking)
├── results/        # Saved plots, outputs, and visualizations
└── README.md       # Project documentation
```

---

## 🧰 Dependencies

Install all dependencies using:

```bash
pip install torch torchvision torchaudio ultralytics opencv-python matplotlib seaborn scikit-learn
```

---

## 🚀 How to Run

```bash
# 1. Clone this repository
git clone https://github.com/mastersubhajit/Tracker_A2.git
cd Tracker_A2

# 2. Open notebooks
jupyter notebook Task1.ipynb
jupyter notebook Task2.ipynb
jupyter notebook Task3.ipynb
```

---

## 🏁 Summary of Results

| Task | Topic | Framework | Best Metric(s) | Key Takeaway |
|------|--------|------------|----------------|---------------|
| **1** | Image Classification | PyTorch | ResNet18 (90.04%) | Transfer learning yields top performance |
| **2** | Object Detection | TorchVision / YOLOv8 | YOLOv8: mAP=0.68, FPS=12.93 | YOLOv8 is faster, smaller, and competitive |
| **3** | Object Tracking | OpenCV | MOSSE: 60 FPS, 66% success | CSRT more robust; MOSSE best speed |

---

## 👨‍💻 Author
**Subhajit Ghosh**  
Master’s Student in Artificial Intelligence  
📍 *Italy / India*  
🔗 [GitHub Profile](https://github.com/mastersubhajit)
