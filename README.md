# Plant Disease Detection — Computer Vision Pipeline

Computer vision models trained to detect potato leaf diseases from field imagery, developed during an internship for a COP 27 precision agriculture project.

## What's Inside

- **PDDCNN/** — Multi-level CNN classifier: 97.78% test accuracy across 3 disease classes (Early Blight, Late Blight, Healthy) trained on 4,062 labeled potato leaf images
- **YOLO Segmentation/** — YOLOv5 instance segmentation model trained from scratch on 2,598 plant disease images with 3 training trials to optimize precision-recall tradeoff
- **Preprocessing pipeline** — Filtering, noise reduction, and augmentation applied to raw field imagery before downstream Mask R-CNN and YOLOv5 segmentation
- **PV-Hawk/** — End-to-end computer vision pipeline deployed and tested on a 12-row, 1,307m field dataset: frame grouping, GPS-based localization, 3D reconstruction via Structure from Motion, and object tracking

## Key Results

| Model | Task | Performance |
|-------|------|-------------|
| CNN | Disease Classification | 97.78% accuracy, 1.00 precision (healthy) |
| YOLOv5 | Leaf Instance Segmentation | Optimized across 3 training trials |

## Context

Part of an AI-based decision support system for precision agriculture — automating crop monitoring and disease detection using computer vision on field-captured imagery.

## Tech Stack

Python, TensorFlow/Keras, YOLOv5, OpenCV, NumPy, Pandas, Matplotlib