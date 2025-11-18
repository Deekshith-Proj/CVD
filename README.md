# Cats VS Dogs Internship Project
This project implements a high-performance Cat vs Dog classifier using deep feature extraction from multiple pretrained CNN architectures combined with classical machine learning models and a stacking meta-learner.
It was created as part of the Google AI/ML Virtual Internship to demonstrate applied computer vision, transfer learning and ensemble learning.

🚀 Project Overview

Instead of training a single CNN from scratch, this project uses a hybrid pipeline:

✔ Pretrained CNNs for Feature Extraction

EfficientNetB0

ResNet50

MobileNetV2

These models (without the top classification layer) extract meaningful deep features using ImageNet weights.

✔ Classical ML Models for Base Classification

Once deep features are extracted and concatenated, they are fed into four base classifiers:

Random Forest (RF)

Support Vector Machine (SVM)

K-Nearest Neighbors (KNN)

Logistic Regression (LR)

✔ Stacking Meta-Learner

Outputs (probabilities) from the four base models are used as meta-features to train a final model:

MLPClassifier (Neural Network Meta-Learner)

This stacked ensemble improves generalization and outperforms individual models.
