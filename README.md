# CS4372_Assignment3
# Deep Learning Project: CIFAR-10 Image Classification using Transfer Learning

## Project Overview
This project implements a CNN for image classification on CIFAR-10 using transfer learning with MobileNetV2. It satisfies all assignment requirements.

## Requirements
- Python 3.8+
- TensorFlow 2.13.0+ (includes Keras)
- matplotlib, numpy, pandas, seaborn, scikit-learn

## Installation
pip install tensorflow matplotlib numpy pandas seaborn scikit-learn
python cnn_cifar10_project.ipynb

## How to Run
1. Install dependencies above
2. Run: cnn_cifar10_project.ipynb
3. Outputs saved to outputs/ and models/ directories

## Requirements Satisfaction
1. Keras using Python - Uses tensorflow.keras
2. Transfer Learning - MobileNetV2 pre-trained on ImageNet
3. Fine-tuning - Two-phase training with layer unfreezing
4. No hard-coded paths - Uses relative paths only
5. Train/Test separation - CIFAR-10 split + validation
6. Parameter tuning - 3 experiments with detailed logging

## Generated Outputs
- training_history.png - Accuracy/loss plots
- sample_predictions.png - 25 test samples with predictions
- confusion_matrix.png - Confusion matrix
- parameter_table.tex - LaTeX table of experiments
- cifar10_model.h5 - Trained Keras model

## Parameter Experiments Tested
- Learning rates: 0.001, 0.0005, 0.002
- Dropout rates: 0.3, 0.4, 0.2
- Batch sizes: 64, 32, 128

## Model Architecture
- Base: MobileNetV2 (pre-trained on ImageNet)
- Custom Head: GlobalAveragePooling2D → Dense(128) → Dropout → Output(10)
- Training: Adam optimizer, Categorical Crossentropy loss

## Dataset
- CIFAR-10: 60,000 32x32 color images
- 10 classes: airplane, automobile, bird, cat, deer, dog, frog, horse, ship, truck
- Split: 50,000 training + 10,000 test (automatic)

## Troubleshooting
- TensorFlow not found: pip install tensorflow
- Out of memory: Reduce dataset size in code
- Slow training: Enable GPU acceleration
- Import errors: Install all requirements.txt packages
