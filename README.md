# Tuberculosis Detection using Deep Learning

## Overview
This repository contains a deep learning-based model for automatic tuberculosis (TB) detection using chest X-ray images. The model is inspired by the research paper *"Ensemble Learning Based Automatic Detection of Tuberculosis in Chest X-ray Images Using Hybrid Feature Descriptors."* Our approach leverages deep learning and ensemble learning techniques to enhance diagnostic accuracy.


## YouTube Video
A detailed explanation of our project is available on YouTube. Watch it here:
[![Watch the video](https://img.youtube.com/vi/uC4N8Tq56EE/0.jpg)](https://www.youtube.com/watch?v=uC4N8Tq56EE)

## Model Workflow
The following diagram illustrates the workflow of our TB detection model:

![Model Workflow](Model_illustration.png)


## Features
- Uses Convolutional Neural Networks (CNNs) for feature extraction
- Incorporates handcrafted features (Gabor filters) along with deep learning features
- Employs ensemble learning for improved accuracy
- Trained and tested on publicly available TB datasets (Montgomery and Shenzhen)
- Achieves high accuracy and AUC compared to existing methods

## Dataset
We used two publicly available datasets:
1. **Montgomery Dataset** - Contains 138 chest X-ray images (80 normal, 58 TB positive)
2. **Shenzhen Dataset** - Contains 662 chest X-ray images (326 normal, 336 TB positive)

Both datasets are provided by the U.S. National Library of Medicine (NIH) and are available upon request.

## Methodology
### 1. Data Preprocessing
- Resized images to fit different CNN architectures
- Applied normalization techniques

### 2. Feature Extraction
- Used pre-trained CNN architectures such as InceptionV3, ResNet50, VGG16, and MobileNet
- Extracted handcrafted features using Gabor filters

#### **Gabor Filter**
The **Gabor filter** is a linear filter used in image processing for edge detection and texture analysis. It is particularly useful for medical image analysis as it mimics the visual perception of the human eye. A Gabor filter is created by multiplying a Gaussian function with a sinusoidal wave, making it sensitive to specific frequencies and orientations. In tuberculosis detection, Gabor filters help extract handcrafted features from chest X-rays, enhancing the ability to distinguish TB-positive cases from normal ones.

### 3. Classification
- Used logistic regression and CNN classifiers
- Applied ensemble learning to combine multiple feature sets

### 4. Evaluation Metrics
- Accuracy
- Area Under the Receiver Operating Characteristic Curve (AUC)
- Sensitivity and Specificity

## Model Performance
| Model               | Montgomery Dataset Accuracy | Shenzhen Dataset Accuracy |
|--------------------|--------------------------|--------------------------|
| CNN-based Model    | 86.23%                    | 87.60%                    |
| Gabor Filter Model | 83.33%                    | 80.67%                    |
| Ensemble Learning  | **93.47%**                 | **97.59%**                 |

## Installation & Usage
### Prerequisites
- Python 3.x
- TensorFlow
- Keras
- OpenCV
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

### Installation
Clone the repository and install dependencies:
```bash
$ git clone https://github.com/dev-anshu-singh/tb_project_hackofiesta
$ cd tb_project_hackofiesta
$ pip install -r requirements.txt
```

## Results & Discussion
Our proposed ensemble model significantly improves TB detection accuracy compared to individual classifiers. By combining CNN-extracted features with handcrafted Gabor filter features, the model achieves robust classification results across multiple datasets.

## Future Improvements
- Test on larger and more diverse datasets
- Improve model generalization using data augmentation
- Deploy the model in a real-time application for TB screening


