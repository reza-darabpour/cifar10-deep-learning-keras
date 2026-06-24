# CIFAR-10 Deep Learning Project with Keras

This repository contains a deep learning project using **TensorFlow/Keras** on the **CIFAR-10 image dataset**.

The project explores different neural network configurations and training strategies for image classification. It also includes a binary classification task for detecting horse images from the CIFAR-10 dataset.

## Project Overview

CIFAR-10 is a well-known image classification dataset that contains 60,000 color images in 10 different classes. Each image has a size of 32×32 pixels.

In this project, neural network models are trained and compared using different activation functions, normalization techniques, optimizers, and training strategies.

The project includes:

* Multi-class classification on CIFAR-10
* Comparison of SELU and ReLU with Batch Normalization
* Binary classification for horse vs non-horse images
* Freezing and unfreezing model layers
* Comparison of different optimizers
* Monte Carlo Dropout experiment

## Objectives

The main objectives of this project are:

* To train neural networks on the CIFAR-10 dataset
* To compare SELU activation with ReLU and Batch Normalization
* To analyze training and validation loss/accuracy
* To convert CIFAR-10 into a binary classification problem for horse detection
* To study the effect of frozen and trainable layers
* To compare different optimizers
* To experiment with Monte Carlo Dropout for regularization and uncertainty estimation

## Dataset

This project uses the CIFAR-10 dataset provided by Keras.

The dataset contains 10 image classes:

```text
airplane
automobile
bird
cat
deer
dog
frog
horse
ship
truck
```

The images are normalized by scaling pixel values between 0 and 1.

## Project Workflow

The notebook follows these main steps:

1. Import required libraries
2. Load the CIFAR-10 dataset
3. Normalize image data
4. Train a neural network using SELU activation
5. Train another neural network using ReLU activation and Batch Normalization
6. Compare the performance of both models
7. Convert the dataset into a horse vs non-horse binary classification problem
8. Use a previously trained model as a base model
9. Freeze model layers and train a new binary classifier
10. Unfreeze layers and retrain the model
11. Train models using different optimizers
12. Compare optimizer performance using training and validation curves
13. Apply Monte Carlo Dropout

## Models and Experiments

### 1. SELU Model

A neural network is trained using SELU activation functions and Lecun Normal initialization.

This experiment is used to study the performance of self-normalizing neural networks.

### 2. ReLU with Batch Normalization

Another neural network is trained using ReLU activation functions, He initialization, and Batch Normalization layers.

The performance of this model is compared with the SELU-based model.

### 3. Horse vs Non-Horse Classification

The CIFAR-10 labels are converted into a binary classification problem:

```text
horse = 1
non-horse = 0
```

A new binary classifier is trained using the previously trained model as a base model.

### 4. Frozen and Trainable Layers

The project compares two training strategies:

* Using frozen base layers
* Unfreezing layers and making them trainable

This helps analyze the effect of transfer-learning-style training on the binary classification task.

### 5. Optimizer Comparison

Different optimizers are tested and compared, including:

* Adam
* AdaGrad
* SGD
* Nadam
* SGD with momentum
* Nesterov SGD with momentum

The comparison is based on training loss, validation loss, training accuracy, and validation accuracy.

### 6. Monte Carlo Dropout

Monte Carlo Dropout is implemented by forcing dropout to remain active during prediction/training behavior. This experiment is used to study regularization and uncertainty-related behavior in neural networks.

## Visualizations

The notebook includes several plots, such as:

* Training loss
* Training accuracy
* Validation loss
* Validation accuracy
* Comparison between SELU and ReLU models
* Comparison between different optimizers
* Monte Carlo Dropout training curves

## Project Structure

```text
cifar10-deep-learning-keras/
│
├── cifar10_deep_learning_keras.ipynb
├── requirements.txt
└── README.md
```

## File Description

* `cifar10_deep_learning_keras.ipynb`: Main Jupyter Notebook containing the deep learning experiments.
* `requirements.txt`: List of required Python packages.
* `README.md`: Project description and instructions.

## Requirements

This project requires Python 3.

Required Python packages:

```text
tensorflow
numpy
matplotlib
scikit-learn
```

You can install the required packages using:

```bash
pip install -r requirements.txt
```

## How to Run

1. Clone or download this repository.
2. Install the required packages:

```bash
pip install -r requirements.txt
```

3. Open the Jupyter Notebook:

```bash
jupyter notebook cifar10_deep_learning_keras.ipynb
```

4. Run the notebook cells step by step.

## Notes

The CIFAR-10 dataset is automatically downloaded using Keras when the notebook is executed.

If the notebook loads a saved model file such as:

```text
model_2_relu.keras
```

make sure that the file exists in the project directory, or run the model training cells first and save the model before loading it.

## Applications

This project can be useful for:

* Learning TensorFlow and Keras
* Image classification practice
* Understanding neural network training
* Comparing activation functions
* Comparing optimizers
* Practicing transfer-learning concepts
* Studying dropout and regularization
* Deep learning coursework and educational projects

## Author

Reza Darabpour

## License

This project is provided for educational and learning purposes.
