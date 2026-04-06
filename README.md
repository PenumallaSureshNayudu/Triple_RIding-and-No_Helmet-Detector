# 🚀 Helmet & Triple Riding Detection Web App

A real-time AI-powered web application built using **Streamlit** and **YOLOv8** to detect:

- 🪖 Helmet violations  
- 👥 Triple riding on motorcycles  

The system processes images and videos and displays only the **highest-confidence detection per frame**, helping improve road safety monitoring.

---

## 🌐 Live Demo

👉 https://hel-triple-ride-detection-1.onrender.com/

---

## 🎯 Motivation

Motorcycle violations like **not wearing helmets** and **triple riding** are major causes of road accidents.

Manual monitoring is:
- ⏱️ Time-consuming  
- 👀 Error-prone  
- 🚔 Limited by manpower  

This project uses AI to:
- Improve accuracy  
- Reduce human effort  
- Enhance traffic rule enforcement  

---

## 🧠 Model Training Overview

### 📊 Dataset
- 6,050 annotated images  
- Classes:
  - Safe riding  
  - No helmet  
  - Triple riding  

---

### ⚙️ Preprocessing
- Resized to 640 × 640  
- Data augmentation:
  - Rotation  
  - Flipping  
  - Brightness adjustment  
  - Mosaic & MixUp  

---

### 🏗️ Model Architecture
- Backbone: CSPDarknet + C2f  
- Neck: PANet  
- Head: Anchor-free detection  

---

### 🏋️ Training Setup
- Epochs: 100  
- Batch size: 16  
- Optimizer: AdamW  
- LR Scheduler: Cosine annealing  
- Loss:
  - BCE  
  - CIoU  
  - Distribution Focal Loss  

---

## 📊 Results

- Precision: 0.895  
- Recall: 0.863  
- mAP@0.5: 0.919  

### 🏆 Best Performance
Triple riding detection:
- Precision: 0.929  
- Recall: 0.935  
- mAP@0.5: 0.964  

---

## 🌟 Features

- Upload images (.jpg, .png)  
- Upload videos (.mp4)  
- Shows only highest-confidence detection  
- Adjustable confidence threshold  
- Fast YOLOv8 inference  
- Clean Streamlit UI  

---

## ⚙️ Setup & Run Locally

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/hel_triple_ride_detection.git
cd hel_triple_ride_detection
