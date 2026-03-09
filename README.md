# MIE1517Project---CIFAKE-Real-vs-AI-Image-Detection-ViT-B16-

# Detecting AI Generated Images with Vision Transformers (CIFAKE)

This is our MIE1517 final project. We trained an image classifier to detect whether a 32x32 image is a real CIFAR 10 photo or an AI generated synthetic image, using the CIFAKE dataset.

## Dataset
CIFAKE (Kaggle):
- 120,000 images total (32x32 RGB)
- 60,000 real images from CIFAR 10
- 60,000 fake images generated with Stable Diffusion v1.4
- Labels: 0 = real, 1 = fake

## Approach
- Transfer learning with a pre trained Vision Transformer (ViT B 16) from torchvision
- Replaced the classification head for binary prediction
- Trained and tuned hyperparameters to improve validation accuracy and generalization

## Results
Best model performance on a held out test set:
- Accuracy: ~96 to 97 percent
- Precision: 96.8 percent
- Recall: 96.4 percent
- F1: 96.6 percent

## Tech stack
Python, PyTorch, torchvision, NumPy, pandas, scikit learn, matplotlib

## How to run
1. Install dependencies (PyTorch and common Python data libraries)
2. Download CIFAKE from Kaggle
3. Run the notebook from top to bottom: load data, preprocess, train, evaluate

## Authors
Lawrence Han, Sally Zhao, Max Li, Xi Chen
