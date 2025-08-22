## 1. Project Introduction

This project leverages the YOLOv8n model to detect and classify road surface damages. The goal is to build an efficient and lightweight solution tailored for deployment on edge devices, supporting real-world applications such as automated road monitoring systems.

Main Objective: Automatically detect cracks, potholes, and other road damages with high accuracy.

Model: YOLOv8n (Nano version) – optimized for high performance with low computational cost.

Dataset: SVRDD (Surface Vehicular Road Damage Dataset) – a specialized dataset for road damage detection training.

## 2. Installation

To install the required libraries, use pip with the requirements.txt file:

```bash
!pip install -r requirements.txt
```

## 3. File Structure

Dataset link: https://zenodo.org/records/10100129

The project is organized as follows (note: dataset structure may slightly differ from the required format below):

```bash
Road-Surface-Damage-Detection/
├── dataset/
│   ├── images/
│   │   ├── train/
│   │   ├── val/
│   │   └── test/
│   └── labels/
│       ├── train/
│       ├── val/
│       └── test/
├── requirements.txt
├── DoAnEmbeddedAI.ipynb (training notebook)
├── ChayMoHinh.ipynb (inference notebook)
└── README.md
```

⚠️ Contact the author to obtain the test set.

## 4. Usage

Training
Use DoAnEmbeddedAI.ipynb to train the model on your dataset.

Inference
Use ChayMoHinh.ipynb to run the trained model on the provided test set.

## 5. Results

After training, the model achieved the following performance metrics:

mAP50: 0.311

mAP50-95: 0.19


These results demonstrate effective localization of road damages. 

Disclaimer: Results may vary slightly depending on the number of epochs or hyperparameters such as learning rate, batch size, etc.

## 6. Future Works

Further optimization: Explore quantization techniques (e.g., INT8) to reduce model size and speed up inference on edge devices.

Dataset expansion: Train on more diverse datasets to enhance model generalization.

Real-world deployment: Build an embedded application on devices like Raspberry Pi or Jetson Nano for real-time predictions.

## 7. Authors

Nguyễn Hoàng Nam

Danh Nat

📧 Email: ng.h.nam0802@gmail.com

🔗 LinkedIn: www.linkedin.com/in/nghnam0802
