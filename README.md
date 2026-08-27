# AI-Generated Image Detection with Vision Transformers

## Overview

This project fine-tunes a pretrained Vision Transformer to distinguish real CIFAR-10 images from synthetic images generated with Stable Diffusion. The model is trained on the CIFAKE dataset as a binary image classifier.

## Dataset

CIFAKE contains 120,000 RGB images at 32 × 32 resolution:

- 60,000 real images from CIFAR-10
- 60,000 synthetic images generated with Stable Diffusion v1.4
- Binary labels: real and AI-generated

## Methodology

- Loaded a pretrained ViT-B/16 model from torchvision
- Replaced the original classification head for binary prediction
- Resized and normalized images for the pretrained architecture
- Fine-tuned model and training hyperparameters
- Evaluated generalization on a held-out test set

## Key Results

The best model achieved approximately:

- Accuracy: 96–97%
- Precision: 96.8%
- Recall: 96.4%
- F1 score: 96.6%

These results show that transfer learning with a Vision Transformer can effectively identify synthetic images in the CIFAKE dataset.

## Technologies

Python, PyTorch, torchvision, Vision Transformer, NumPy, pandas, scikit-learn, matplotlib

## How to Run

1. Download the CIFAKE dataset from Kaggle.
2. Install PyTorch and the required Python data libraries.
3. Open the notebook and run the data-loading, preprocessing, training, and evaluation sections in order.

## Contributors

Lawrence Han, Sally Zhao, Max Li, Xi Chen
