# Lacuna-Malaria-Challenge

![lacuna](https://github.com/user-attachments/assets/beca1bfe-dd05-4f28-8e9a-3ab008ad8d09)

## Project Overview

This repository contains the solution for the Lacuna Malaria Detection Competition. The goal of the challenge was to accurately detect and localize malaria parasites in cell images. Leveraging object detection models, my solution achieved a mean Average Precision (mAP) at IoU=0.5 of 86.4%.

![lacuna2](https://github.com/user-attachments/assets/52415d8c-d204-4308-9bbd-df3ffd9407be) 


## Approach

### 1. Data Preparation
Data Source: The provided dataset included annotated images for malaria detection with bounding boxes.

Preprocessing: Standardized image sizes, normalized pixel values, and converted annotations into the required format for model training.

Augmentation: Applied transformations including rotations, flips, scaling, and brightness adjustments to increase data diversity and reduce overfitting.

### 2. Model Selection
YOLO-Based Model: Used a YOLO architecture tailored for object detection, pre-trained on COCO, and fine-tuned on the malaria dataset.
Training Pipeline: Configured using TensorFlow’s object detection API, with custom pipeline settings for optimizer, batch size, and augmentation.

### 3. Training Process

### Hyperparameters:

Batch Size: 8

Epochs: 100

Learning Rate: Fine-tuned for optimal convergence

Device: Trained on a Tesla P100 GPU.

Loss Function: Used a custom object detection loss to handle bounding box regression and classification.

### 4. Model Performance
Achieved mAP50: 86.4%

Class-wise mAP:

Trophozoite: 70.6

White Blood Cell (WBC): 97.77

### 5. Challenges and Solutions
   
Class Imbalance: Tackled using data resampling and focal loss adjustment.

Limited Data: Augmentation strategies and transfer learning helped improve model generalization.

## How to Run

### Clone the repository:
```bash

git clone https://github.com/poppatheduke/Lacuna-Malaria-Challenge

#Run all tabs
```

## Future Improvements

Additional augmentations and custom architectures for better generalization.

Incorporating ensemble methods for higher mAP.
