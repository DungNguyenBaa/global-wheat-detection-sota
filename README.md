# Global Wheat Detection SOTA 🌾🔍

A high-performance object detection pipeline optimized for high-density, small-object detection in agricultural imagery. This repository implements the core strategies utilized in the **1st place winning solution** of the Global Wheat Detection Challenge.

## 🚀 Key Features
- **Multi-Scale Feature Fusion:** Optimized backbones (EfficientDet, YOLOv8, Faster R-CNN) with heavy focus on FPN enhancements.
- **Robust Augmentation:** Specialized augmentations for agricultural data (Mosaic, MixUp, Random Crop).
- **Ensemble Strategy:** Weighted Boxes Fusion (WBF) for combining multi-model predictions.
- **TTA (Test Time Augmentation):** Multi-scale and flip-based TTA for maximum precision.

## 🏗️ Architecture
- **Backbone:** EfficientNet-B7 / ResNet-101.
- **Neck:** BiFPN for bidirectional feature flow.
- **Heads:** Specialized regression heads for tight bounding box localization.

## 🛠️ Usage
```bash
pip install -r requirements.txt
python inference.py --image sample_field.jpg --weights checkpoints/wheat_model_final.pth
```