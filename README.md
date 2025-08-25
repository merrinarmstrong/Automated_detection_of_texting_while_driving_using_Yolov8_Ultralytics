# Automated_detection_of_texting_while_driving_using_Yolov8_Ultralytics

<div align="center">
  <h1>Texting While Driving Detection Using YOLOv8</h1>
</div>

![Python](https://img.shields.io/badge/Python-3.9+-blue)
![Ultralytics YOLOv8](https://img.shields.io/badge/YOLOv8-Ultralytics-red)
![OpenCV](https://img.shields.io/badge/OpenCV-4.5+-blue)
![Roboflow](https://img.shields.io/badge/Dataset-Roboflow-orange)
![License](https://img.shields.io/badge/License-MIT-brightgreen)

> A computer vision-based pipeline that detects texting while driving using YOLOv8. Built for real-time monitoring with a focus on privacy compliance (GDPR).

---

## 📌 Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset](#dataset)
3. [Model Architecture](#model-architecture)
4. [Evaluation Metrics](#evaluation-metrics)
5. [Results](#results)
6. [Installation](#installation)
7. [Usage](#usage)
8. [Future Work](#future-work)
9. [Contributors](#contributors)
10. [License](#license)

---

## 📖 Project Overview

Texting while driving is a major cause of road accidents. This project presents an **automated detection system** using the **YOLOv8 object detection model** to identify drivers who are texting while driving. The system is trained on a curated dataset and shows high precision and recall.

---

## 📁 Dataset

- **Source:** Roboflow “Phone While Driving” dataset  
- **Classes:** `Phone`, `Wheel`  
- **Splits:**
  - Training: 620 images
  - Validation: 177 images
  - Testing: 89 images

Annotation format: YOLO bounding boxes.

---

## 🧠 Model Architecture

- **Framework:** YOLOv8 by Ultralytics
- **Components:**
  - **Backbone:** CSPDarknet53 + C2f
  - **Neck:** FPN + PAN
  - **Head:** Bounding box and class predictions

---

## 📊 Evaluation Metrics

| Metric        | Validation | Test   |
|---------------|------------|--------|
| mAP50-95      | 0.888      | 0.855  |
| mAP50         | 0.987      | 0.983  |
| Precision     | 0.967      | 0.973  |
| Recall        | 0.981      | 0.978  |

---

## ✅ Results

- High detection accuracy on both `Phone` and `Wheel` classes
- Minimal overfitting between validation and test sets
- Clear potential for real-world deployment

---

## 🛠️ Installation

```bash
git clone https://github.com/YOUR_USERNAME/texting-detection-yolov8.git
cd texting-detection-yolov8
pip install -r requirements.txt