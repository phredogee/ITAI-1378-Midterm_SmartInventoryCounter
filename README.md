##Midtermn Smart Inventory Counter

# PPE Safety Detection System Using YOLO11

> **ITAI 1378 – Computer Vision and AI Midterm Project**
> **Student:** Alfredo C. Garza

---

# Overview

The PPE Safety Detection System is a computer vision application designed to automatically detect Personal Protective Equipment (PPE) in workplace images. The project uses the YOLO11 object detection model to identify workers and determine whether required safety equipment is present.

Rather than relying on manual inspections, this system demonstrates how modern object detection can assist with workplace safety by identifying essential PPE in real time.

---

# Problem Statement

Construction sites and industrial facilities require workers to wear personal protective equipment such as helmets, gloves, boots, and safety vests. Manual safety inspections can be time-consuming and may miss violations, particularly on large job sites.

This project explores how computer vision can automate PPE detection to improve safety compliance and reduce the need for continuous manual monitoring.

---

# Project Objectives

* Detect multiple PPE categories in workplace images
* Evaluate YOLO11 for PPE object detection
* Measure detection performance using standard computer vision metrics
* Produce a trained model capable of accurate inference on unseen images

---

# Dataset

**Dataset:** Construction PPE Detection Dataset (Roboflow)

Classes:

* Boots
* Gloves
* Helmet
* Human
* Vest

Dataset Summary:

* Training Images: **4,380**
* Validation Images: **420**

---

# Technology Stack

* Python 3.13
* Ultralytics YOLO11
* PyTorch
* OpenCV
* NumPy
* Matplotlib
* NVIDIA RTX 4060 Laptop GPU

---

# Model Training

Model:

* YOLO11n

Training Configuration:

* Epochs: 20
* Image Size: 640 × 640
* Optimizer: AdamW (automatic selection)
* Device: NVIDIA RTX 4060 GPU

---

# Results

| Metric    |    Result |
| --------- | --------: |
| Precision | **90.8%** |
| Recall    | **90.6%** |
| mAP@50    | **93.0%** |
| mAP@50–95 | **73.9%** |

Per-class performance:

| Class  | mAP@50 |
| ------ | -----: |
| Boots  |  97.5% |
| Gloves |  77.3% |
| Helmet |  97.4% |
| Human  |  96.2% |
| Vest   |  96.7% |

The model demonstrated strong overall performance, with particularly accurate detection of helmets, boots, safety vests, and people. Gloves proved to be the most challenging class because they are smaller objects and are frequently partially occluded.

---

# Repository Structure

```text
ITAI1378_PPE_Detection/
│
├── docs/
├── models/
├── notebooks/
├── outputs/
├── README.md
├── requirements.txt
└── data.yaml
```

---

# Example Outputs

The `outputs/` directory contains:

* Training performance curves
* Confusion matrix
* Dataset label visualization
* Sample model predictions

---

# Future Improvements

Potential enhancements include:

* Train larger YOLO11 model variants
* Improve glove detection accuracy
* Test live webcam inference
* Add video-based PPE monitoring
* Deploy as a Streamlit web application

---

# AI Usage

Generative AI tools were used to assist with:

* Project planning
* Documentation
* Repository organization
* Technical explanations

All dataset selection, model training, evaluation, and implementation were completed and verified by the project author.

---

# Acknowledgements

* Ultralytics YOLO11
* Roboflow Universe
* ITAI 1378 – Computer Vision and AI
