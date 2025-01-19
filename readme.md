# Activation Impact on MLP

## Overview
This repo involves modifying the original Multi-Layer Perceptron (MLP) architecture by adding an additional hidden layer. The primary objective is to compare the performance of the modified model with the original architecture and analyze the effect of increased complexity on model accuracy and validation performance.

## Original Architecture
- **Flatten Layer**: Converts input data into a 1D array.
- **Hidden Layers**: Two layers with 128 and 64 neurons, using ReLU activation.
- **Output Layer**: A softmax layer with 10 neurons for classification.

## Modified Architecture
- **Flatten Layer**: Converts input data into a 1D array.
- **Hidden Layers**: Three layers with 128, 64, and 32 neurons, all using ReLU activation.
- **Output Layer**: A softmax layer with 10 neurons for classification.

## Results
The results for the MNIST, Fashion MNIST, and CIFAR-10 datasets were evaluated, and the following charts were generated:

### MNIST Dataset:
![MNIST Accuracy](/charts/mnist1.png)

### Fashion MNIST Dataset:
![Fashion MNIST Accuracy](/charts/fashion_mnist1.png)

### CIFAR-10 Dataset:
![CIFAR-10 Accuracy](/charts/cifar101.png)

---

## Replacing Activation Functions

### Overview
This part focuses on replacing the ReLU activation function in the hidden layers with alternatives such as **tanh** and **sigmoid**. The primary goal is to compare their impact on accuracy and training performance.

### ReLU Activation
- **Advantages**: Simplicity and efficiency in deep models.
- **Limitations**: Can suffer from the "dying ReLU" problem.

### Alternative Activations
1. **Tanh**: Outputs values between -1 and 1, which can be beneficial for datasets where negative activations matter.
2. **Sigmoid**: Outputs values between 0 and 1, making it suitable for probability-based tasks.

### Results
The performance of the models with different activation functions was evaluated on the MNIST, Fashion MNIST, and CIFAR-10 datasets. Below are placeholders for the performance comparison charts:

#### MNIST Dataset:
![MNIST Accuracy - Activation Comparison](/charts/mnist2.png)

#### Fashion MNIST Dataset:
![Fashion MNIST Accuracy - Activation Comparison](/charts/fashion_mnist2.png)

#### CIFAR-10 Dataset:
![CIFAR-10 Accuracy - Activation Comparison](/charts/cifar102.png)

---

## Key Observations
1. Adding an additional hidden layer:
   - Improved accuracy for simpler datasets like MNIST.
   - Marginal improvements for more complex datasets like CIFAR-10, with increased training time.

2. Activation function replacement:
   - **ReLU** generally performed better on all datasets.
   - **Tanh** performed comparably on MNIST but was slower.
   - **Sigmoid** showed lower accuracy and slower convergence.

---

## Conclusion
The results highlight the importance of selecting the right architecture and activation functions based on the dataset's complexity. For simple datasets like MNIST, additional complexity can improve performance. For more complex datasets, careful tuning of hyperparameters and model architecture is essential.

---
