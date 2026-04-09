# Bone Fracture Detection using CNN

## Problem Statement
Bone fractures are commonly identified using X-ray imaging. The objective of this project is to develop a Deep Learning–based image classification system that automatically analyzes X-ray images and determines whether a bone is fractured or normal.  
The proposed model uses a Convolutional Neural Network (CNN) to learn visual patterns from multi-region bone X-rays and classify them into two categories: Fractured and Not Fractured.  

This system aims to:  
- Provide quick automated fracture detection  
- Support medical image analysis workflows  
- Enable consistent classification of X-ray images  
- Serve as a foundation for computer-aided diagnosis systems  

---

## Dataset
Dataset used:  
https://www.kaggle.com/datasets/bmadushanirodrigo/fracture-multi-region-x-ray-data  

Dataset contains:  
- Train images  
- Validation images  
- Test images  
- Two classes:  
  - Fractured  
  - Not Fractured  

The dataset includes multi-region bone X-ray images such as:  
- Arm  
- Leg  
- Hand  
- Shoulder  
- Other bone areas  

---

## Model Used
Convolutional Neural Network (CNN)

The CNN model classifies X-ray images into:  
- Fractured  
- Normal  

---

## Technologies Used
- Python  
- TensorFlow / Keras  
- CNN (Deep Learning)  
- NumPy  
- Matplotlib  
- Kaggle API  

---

## Project Explanation

### 1. Dataset Download
Dataset is downloaded from Kaggle using Kaggle API and extracted into the working directory.

### 2. Data Loading
Images are loaded using TensorFlow:  
- Image size: 224 × 224  
- Batch size: 32  
- Training and validation datasets created from folders  

### 3. Data Preprocessing
- Images resized to 224x224  
- Pixel values normalized (0–255 → 0–1)  
- Corrupted images ignored  
- Dataset optimized using AUTOTUNE  

### 4. CNN Architecture
The model consists of:  
- Conv2D Layer (Feature extraction)  
- MaxPooling Layer (Dimensionality reduction)  
- Conv2D Layer  
- MaxPooling Layer  
- Conv2D Layer  
- MaxPooling Layer  
- Flatten Layer  
- Dense Layer (Fully connected)  
- Output Layer (Sigmoid activation)  

### 5. Model Compilation
- Optimizer: Adam  
- Loss Function: Binary Crossentropy  
- Metric: Accuracy  

### 6. Model Training
The model is trained using:  
- Training dataset  
- Validation dataset  
- Multiple epochs  

### 7. Performance Visualization
Graphs plotted:  
- Training Accuracy  
- Validation Accuracy  
- Model performance comparison  

### 8. Prediction
A test X-ray image is:  
- Loaded  
- Resized  
- Normalized  
- Passed to model  

Model predicts:  
- Fractured  
or  
- Not Fractured  

---

## Output
The model takes an X-ray image as input and outputs:  
- Fractured  
or  
- Normal  
