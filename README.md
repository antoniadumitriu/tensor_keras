# CIFAR-10 Image Classification with CNN

This repository contains Python scripts that demonstrate how to build and train a Convolutional Neural Network (CNN) model for image classification using the CIFAR-10 dataset. CIFAR-10 is a widely used dataset in machine learning research, consisting of 60,000 32x32 color images across 10 different classes.

## Requirements

- Python 3.x
- TensorFlow
- Matplotlib

You can install the required packages using pip:

```
pip install tensorflow matplotlib
```

## Usage

1. Clone this repository or download the source code files.

2. Navigate to the project directory.

3. Run the Python script:

```
python cifar10_cnn.py
```

This script will:

- Load and preprocess the CIFAR-10 dataset
- Define and compile a CNN model architecture
- Train the CNN model on the training dataset
- Evaluate the model's performance on the test dataset
- Plot the training and validation accuracy over epochs

## Code Explanation

The provided Python script follows these steps:

1. **Import necessary libraries**: TensorFlow, datasets, layers, models, and matplotlib for visualization.

2. **Load the CIFAR-10 dataset**: The script loads the CIFAR-10 dataset using `datasets.cifar10.load_data()`. The dataset is split into training and test sets.

3. **Preprocess the data**: The pixel values of the images are normalized to be between 0 and 1.

4. **Define the CNN model**: A sequential CNN model is defined using various layers, including convolutional layers (`Conv2D`), max-pooling layers (`MaxPooling2D`), flatten layer (`Flatten`), and dense layers (`Dense`).

5. **Compile the model**: The model is compiled with an optimizer (`adam`), loss function (`SparseCategoricalCrossentropy`), and a metric (`accuracy`).

6. **Train the model**: The CNN model is trained on the training dataset using `model.fit()`. The training progress is monitored for a specified number of epochs (`epochs=10`).

7. **Evaluate the model**: After training, the model's performance is evaluated on the test dataset using `model.evaluate()`. The test accuracy is printed.

8. **Plot training history**: The script plots the training and validation accuracy over the epochs using matplotlib.
