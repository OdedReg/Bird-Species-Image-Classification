<h1 align="center">Bird Species Image Classification</h1>

![Bird Species](https://github.com/OdedReg/Birds-Classification/blob/main/Birds.jpg)

## Table of Contents
- [Overview](#overview)
- [Dataset](#dataset)
- [Methods](#methods)
- [Results](#results)
- [Conclusions](#conclusions)
- [Contact](#contact)
  
## Overview
This repository contains a deep learning project focused on classifying 525 bird species using convolutional neural networks (CNNs). The dataset comprises 84,635 training images, 2,625 test images, and 2,625 validation images, with each image having dimensions of 224 x 224 x 3.

## Dataset
The dataset is organized into training, testing, and validation sets, each containing 525 subdirectories for the respective bird species. The images were curated via internet searches and filtered to remove duplicates. Notably, the dataset is unbalanced and predominantly features male species, which may affect the classifier's performance on female species images.

## Methods
The project includes three main approaches:
1. A custom-built 6-layer CNN architecture trained using PyTorch Lightning.
2. Transfer learning experiments with ResNet34 and DenseNet121.
3. Feature Extraction using DenseNet121 and XGBoost.

### Results
| Model Name      | Train Loss | Test Loss | Train Acc | Test Acc | Running Time (Minutes) | Epochs |
|-----------------|------------|-----------|-----------|----------|------------------------|--------|
| CNN-6 Layers    | 0.197570   | 0.444069  | 0.945515  | 0.886476 | 132.639                | 20     |
| DenseNet-121    | 0.151845   | 0.224838  | 0.957441  | 0.935238 | 142.300                | 17     |
| ResNet-34       | 0.285467   | 0.349107  | 0.918529  | 0.899048 | 59.407                 | 13     |
| XGBoost         | N/A        | N/A       | 1.000000  | 0.584000 | 43.441                 | N/A    |

## Conclusions
- DenseNet-121 outperformed other models with a test accuracy of 93.5%.
- Transfer learning proved effective for training complex networks  within a relatively short timeframe.
- The custom CNN model showed competitive performance to ResNet-34, a more complex architecture.
- Feature extraction alone was insufficient to achieve competitive performance.
- The discrepancy in the number of epochs can be attributed to early stopping, indicating efficient training convergence.

## Contact
For any queries or discussions, please open an issue on the GitHub repository or contact me at odedregev14@gmail.com.
