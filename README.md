# 🛰️ LiDAR-Based 3D Object Detection using KITTI Dataset

This project presents the implementation and comparative evaluation of five state-of-the-art deep learning models for 3D object detection using LiDAR point cloud data. Leveraging the widely adopted **KITTI 3D Object Detection Benchmark**, each model is tested for accuracy and inference speed, and their outputs are visually and analytically assessed.

---

## 📂 Dataset Overview

- **Dataset**: [KITTI 3D Object Detection Benchmark](https://www.cvlibs.net/datasets/kitti/eval_object.php?obj_benchmark=3d)
- **Total Samples Used**: 7,481
- **Components**:
  - `velodyne/` — Raw point cloud data in `.bin` format
  - `calib/` — Calibration files for sensor alignment
  - `label/` — Ground truth object annotations

> ⚠️ **Note**: Due to GitHub’s file size limitations, the full dataset is not included in this repository. Please download it directly from the [KITTI official website](https://www.cvlibs.net/datasets/kitti/eval_object.php?obj_benchmark=3d).

---

## 🧠 Models Implemented

The following five models were implemented and tested:

| Model Name     | Description                                        |
|----------------|----------------------------------------------------|
| **PV-RCNN++**  | Enhanced point-voxel feature fusion for precise 3D detection |
| **CenterPoint**| Anchor-free detection using object center estimation |
| **PointPillars**| Efficient encoding of LiDAR data as pseudo images |
| **SECOND**     | Sparsely Embedded Convolutional Detection network |
| **CIA-SSD**    | Class-balanced anchor-free single-stage detector |

Each model includes:
- Source code
- Two sample output visualizations
- Corresponding performance graphs (accuracy vs. FPS)

---

## 🛠️ Tech Stack & Libraries

The core libraries and tools used include:

```python
import os
import numpy as np
import open3d as o3d
import random
