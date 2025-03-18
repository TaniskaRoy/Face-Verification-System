# Face Verification System

## Project Overview
This project develops a face verification system using both traditional and deep learning approaches. The system leverages a custom dataset of 851 images from 51 individuals (with more than 10 images per person) to perform face recognition and verification.


## Dataset
Utilized a custom dataset consisting of 851 images from 51 individuals (with more than 10 images per person).
The link to the dataset is :https://drive.google.com/file/d/19xRyHXLK5l3i2tkPbl9OqTI4VFZ2U75F/view?usp=sharing
## Approach & Methodology
The project explores different techniques for feature extraction and classification:

1. **PCA (Principal Component Analysis)**:
   - Used for dimensionality reduction to extract key features from the facial images.

2. **Autoencoders**:
   - A deep learning-based approach used to extract features by compressing the input images and reconstructing them. 
   - The accuracy of this approach is evaluated by passing the extracted features through an SVM (Support Vector Machine) classifier.

3. **FaceNet**:
   - A deep learning model used for feature extraction. It directly generates embeddings that are compared for verification.
   - FaceNet combined with SVM achieved near-perfect accuracy.

## Classifiers Used
- **SVM (Support Vector Machine)**: 
  - Trained on features extracted using PCA, Autoencoder, and FaceNet. SVM performed the best in terms of accuracy across all methods.

- **MLP (Multilayer Perceptron)**:
  - Another classifier that was trained and compared with SVM for performance evaluation.

## Results
- **FaceNet + SVM**: Nearly 100% accuracy.
- **PCA + SVM**: 96% accuracy.
- **Autoencoder + SVM**: 93% accuracy.
- **MLP Classifier**: Lower accuracy compared to SVM.

## Files in the Project
1. **Dense_AutoEncoder_7Layers.ipynb**: 
   - Implements an autoencoder to extract features and evaluate them using an SVM classifier.

2. **FaceNet.ipynb**: 
   - Uses the FaceNet model for feature extraction.

3. **PCA_10Sep.ipynb**: 
   - Implements PCA for feature extraction.

## Conclusion
This project showcases how traditional methods (PCA) and deep learning methods (Autoencoders, FaceNet) can be used for face verification, with the FaceNet + SVM combination achieving the highest accuracy.
