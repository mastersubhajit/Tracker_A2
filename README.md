# Tracker A2 — Computer Vision Tasks

## Project Overview
This repository contains a series of three Jupyter Notebooks (`Task1.ipynb`, `Task2.ipynb`, and `Task3.ipynb`) that explore different computer vision workflows, model training techniques, and performance evaluations.  
The focus is on understanding object tracking and detection pipelines using modern deep learning methods.

---

## Repository Structure

```
📂 Tracker_A2/
│
├── Task1.ipynb      # Dataset preparation, visualization, and preprocessing
├── Task2.ipynb      # Model training, performance analysis, and trade-off discussion
├── Task3.ipynb      # Advanced experimentation and final evaluation
├── data/            # (Ignored) Large datasets such as CIFAR-10
└── README.md        # Project documentation
```

---

## Task Summaries

### ** Task 1 — Data Preparation & Preprocessing**
- Loaded and structured datasets (e.g., CIFAR-10).  
- Implemented preprocessing pipelines for normalization and augmentation.  
- Defined data loaders and visualized sample images.  
- Established the foundation for subsequent model training and testing.  

**Core Skills Demonstrated:**  
Data handling, preprocessing, visualization, dataset exploration.

---

### ** Task 2 — Model Development & Analysis**
- Trained deep learning models for object recognition/tracking.  
- Compared model performance using accuracy, loss curves, and inference speed.  
- Documented trade-offs between model size, speed, and accuracy.  
- Concluded with insights into optimal model configurations for balanced performance.

**Sections Included:**
- **Discussion Summary**  
- **Performance Analysis**  
- **Trade-off Summary**  
- **Conclusion**

**Core Skills Demonstrated:**  
Model optimization, evaluation, and critical performance assessment.

---

### ** Task 3 — Experimental Evaluation**
- Conducted additional experiments for performance validation.  
- Fine-tuned models and hyperparameters.  
- Verified model robustness on unseen or augmented data.  

**Core Skills Demonstrated:**  
Experimental design, hyperparameter tuning, and validation testing.

---

## Setup Instructions

### **1. Clone the Repository**
```bash
git clone https://github.com/mastersubhajit/Tracker_A2.git
cd Tracker_A2
```

### **2. Create and Activate Virtual Environment**
```bash
python3 -m venv .venv
source .venv/bin/activate  # macOS/Linux
.venv\Scripts\activate     # Windows
```

### **3. Install Dependencies**
```bash
pip install -r requirements.txt
```

If `requirements.txt` is missing, manually install key packages:
```bash
pip install torch torchvision matplotlib numpy jupyter
```

---

## Data Handling
The dataset (`cifar-10-python.tar.gz`) is **not included** in this repository due to GitHub’s 100MB file limit.  
To run the notebooks:
1. Download the dataset manually from [CIFAR-10](https://www.cs.toronto.edu/~kriz/cifar.html).  
2. Place it in a `data/` folder:
   ```
   Tracker_A2/data/cifar-10-python.tar.gz
   ```

> **Note:** The `data/` directory is listed in `.gitignore` to prevent large file uploads.

---

## Results Summary
| Task | Focus | Key Output |
|------|--------|------------|
| Task 1 | Dataset processing | Visualized and prepared input data |
| Task 2 | Model training | Performance graphs and trade-off analysis |
| Task 3 | Experimental validation | Refined model performance |

---

## Technologies Used
- **Python 3.12**
- **PyTorch**
- **Torchvision**
- **Matplotlib**
- **NumPy**
- **Jupyter Notebook**

---

## 🧑‍💻 Author
**Subhajit Ghosh**  
Computer Vision | Deep Learning Enthusiast  
🔗 [GitHub Profile](https://github.com/mastersubhajit)
