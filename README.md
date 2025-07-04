# 🌊 Maritime Obstacle Segmentation for Unmanned Surface Vehicles

Accurate segmentation of maritime environments into **sky**, **water**, and **obstacle** regions is critical for the safe navigation of **Unmanned Surface Vehicles (USVs)**. This project presents a deep learning-based semantic segmentation pipeline using a **ResNet34-based U-Net architecture**, trained on the **LaRS Dataset**, achieving a high mIoU of **95.4%**.

---

## 🚀 Project Overview

This repository contains the full implementation of a semantic segmentation model tailored for maritime scenes. The objective is to enable USVs to autonomously recognize and avoid obstacles in dynamic environments such as harbors, open waters, and near-shore regions.

---

## 🧠 Model Architecture

- **Encoder**: Pretrained **ResNet34** backbone
- **Decoder**: U-Net-style with skip connections
- **Atrous Convolutions**: For multi-scale feature extraction
- **Input**: RGB images (256×256)
- **Output**: Semantic masks with 3 classes (sky, water, obstacle)

---

## 📊 Performance

| Metric    | Value  |
|-----------|--------|
| mIoU      | 95.4%  |
| Precision | 64.9%  |
| Recall    | 45.5%  |
| F1 Score  | 46.9%  |

---

## 📁 Dataset

We use the **LaRS Dataset**:  
📂 [https://lojzezust.github.io/lars-dataset/](https://lojzezust.github.io/lars-dataset/)

- 4008 high-resolution maritime images
- Labeled into 4 classes: **sky**, **water**, **obstacle**, and **undefined**
- Images are preprocessed into 256×256 patches, normalized to [0,1]
- Augmentation includes flips, rotations, brightness and hue adjustments

---

## 🛠️ Setup & Installation

```bash
git clone https://github.com/adityaNarthi/Semantic-Segmentation.git
cd Semantic-Segmentation
pip install -r requirements.txt
