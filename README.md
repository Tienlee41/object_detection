# Fruit Detection using YOLO

This repository contains the official implementation of our submission to the **Kaggle competition: [Fruit Object Detection](https://www.kaggle.com/competitions/2425-ii-ait-3002-2-object-detection)**.  
The goal is to build a fruit detection system that identifies and classifies fruits from static images using the YOLOv11-l model.

---

## 📂 Dataset Description

The dataset is structured into two main folders: `Train` and `Test`.

### Train Folder
- `images/`: Contains `.jpg` images of fruits.
- `labels/`: Contains annotation files in YOLO format.  
  Each label file includes:
  - Class ID:
    - `Apple: 0`
    - `Banana: 1`
    - `Grapes: 2`
    - `Orange: 3`
    - `Pineapple: 4`
    - `Watermelon: 5`
  - Normalized bounding box: `x_center`, `y_center`, `width`, `height`

### Test Folder
- Contains **unlabeled `.jpg` images**, used for **public and private testing**.

### Evaluation Phases
- **Public Test**: Results displayed on the public leaderboard after submission.
- **Private Test**: Final rankings determined from selected submissions using a hidden test set (private leaderboard).

> 🔎 All images are in `.jpg` format.

---

## Evaluation Metric: mean Average Precision (mAP)

The competition uses **mean Average Precision at IoU=0.5 (mAP@0.5)** as the evaluation metric.

- **Precision** = TP / (TP + FP)
- A prediction is correct if **IoU ≥ 0.5**
- **AP** is computed from the Precision–Recall curve for each class.
- **mAP** is the mean of all APs across the six fruit classes.

Participants aim to maximize the **mAP** on the test set to rank higher on both public and private leaderboards.

## Submission link
- [Submission](https://www.kaggle.com/code/letien41/submission) 