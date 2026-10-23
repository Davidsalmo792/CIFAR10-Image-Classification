# IAI600 – CIFAR-10 Image Classification

**University West | Group 9**

## Project Overview

This project focuses on image classification using the CIFAR-10 dataset. The objective is to implement and compare two machine learning architectures:

- Multilayer Perceptron (MLP)
- Convolutional Neural Network (CNN)

The project is developed using Python and PyTorch as part of the IAI600 – Introduction to Artificial Intelligence and Machine Learning course.

## Dataset

CIFAR-10 contains 60,000 RGB images of size 32 × 32 pixels across 10 classes:

Airplane, Automobile, Bird, Cat, Deer, Dog, Frog, Horse, Ship, and Truck.

The dataset is divided into:

| Dataset | Images |
|---|---:|
| Training | 45,000 |
| Validation | 5,000 |
| Testing | 10,000 |

## Data Preprocessing

The following preprocessing steps have been implemented:

1. Dataset exploration and visualization.
2. Class distribution analysis.
3. Stratified training/validation split (90% / 10%).
4. Conversion of images into PyTorch tensors.
5. RGB channel-wise normalization using training-set statistics.
6. DataLoader preparation with a batch size of 64.
7. Reproducibility checks using a fixed random seed of 42.

## Project Structure

```text
CIFAR10_PROJECT/
├── CIFAR10_Project.ipynb
├── data_preparation.py
├── config/
│   ├── split_indices.npz
│   └── preprocessing_config.json
├── .gitignore
└── README.md
```

The CIFAR-10 dataset files are excluded from GitHub and downloaded automatically when needed.

## Installation

Install the required Python libraries:

```bash
python -m pip install torch torchvision numpy matplotlib scikit-learn pandas jupyterlab ipykernel
```

## Usage

The shared data preparation module can be imported into the MLP and CNN notebooks:

```python
from data_preparation import get_cifar10_loaders

train_loader, val_loader, test_loader = get_cifar10_loaders()
```

Both models should use the same dataset partitions and normalization parameters to ensure a fair comparison.

## Project Status

- Dataset preparation and preprocessing: Completed
- MLP model development: In progress
- CNN model development: In progress
- Model evaluation and comparison: Pending
- Final project report: Pending

## Acknowledgment

Generative AI tools, including ChatGPT, have been used to support learning, code development, and documentation. Project members remain responsible for understanding, verifying, and explaining their submitted work.
