# Fashion-MNIST Image Classification with CNN

## 📌 Project Overview

This project demonstrates the development of a **Convolutional Neural Network (CNN)** for multiclass image classification using the Fashion-MNIST dataset.

The model is designed to classify grayscale images of clothing items into 10 categories. The project covers image preprocessing, CNN architecture design, model training, regularization, performance monitoring, and final evaluation on unseen test data.

## 🗂️ Dataset

The project uses the **Fashion-MNIST** dataset:

* 60,000 training images
* 10,000 test images
* Image size: **28 × 28 pixels**
* Grayscale images
* 10 classes

The pixel values are normalized to the `[0, 1]` range and reshaped to include a single image channel before being passed to the CNN.

### Classes

* T-shirt/top
* Trouser
* Pullover
* Dress
* Coat
* Sandal
* Shirt
* Sneaker
* Bag
* Ankle boot

## 🧠 CNN Architecture

The model consists of two convolutional blocks followed by fully connected layers:

```text
Input: 28 × 28 × 1
        ↓
Conv2D: 32 filters, 3 × 3, ReLU
        ↓
MaxPooling2D
        ↓
Dropout (0.20)
        ↓
Conv2D: 64 filters, 3 × 3, ReLU
        ↓
MaxPooling2D
        ↓
Dropout (0.25)
        ↓
Flatten
        ↓
Dense: 128 neurons, ReLU
        ↓
Dropout (0.35)
        ↓
Dense: 10 neurons, Softmax
```

The final model contains **421,642 trainable parameters**.

## ⚙️ Training

The model was trained using:

* **Optimizer:** Adam
* **Loss function:** Sparse Categorical Cross-Entropy
* **Metric:** Accuracy
* **Batch size:** 128
* **Maximum epochs:** 20
* **Validation split:** 20%

Two callbacks were used to improve the training process:

* **EarlyStopping** — monitors validation accuracy and restores the best model weights.
* **ReduceLROnPlateau** — reduces the learning rate when validation accuracy stops improving.

## 📊 Results

The model achieved:

| Metric              |     Result |
| ------------------- | ---------: |
| Training Accuracy   |     93.30% |
| Validation Accuracy |     92.57% |
| **Test Accuracy**   | **92.34%** |
| Test Loss           |     0.2250 |

The model achieved **92.34% accuracy on the unseen test dataset**, demonstrating that a relatively compact CNN can effectively learn visual patterns in Fashion-MNIST images.

## 📈 Training Analysis

Training and validation accuracy/loss were tracked throughout the training process.

The project includes visualizations that allow analysis of:

* Training vs. validation accuracy
* Training vs. validation loss
* Model convergence
* Potential overfitting

## 🛠️ Technologies

* **Python**
* **TensorFlow**
* **Keras**
* **NumPy**
* **Matplotlib**
* **Jupyter Notebook**
* **Google Colab / GPU**

## 📁 Project Structure

```text
fashion-mnist-cnn/
│
├── fashion_mnist_cnn.ipynb   # CNN implementation and experiments
├── test.py                    # Additional testing
├── .gitignore
└── README.md
```

## 🎯 Key Takeaways

This project provided practical experience with:

* Image preprocessing for CNN models
* Convolutional neural networks
* Feature extraction using convolutional layers
* Max pooling
* Dropout regularization
* Multiclass image classification
* Model training and validation
* Training callbacks
* Learning rate scheduling
* Model evaluation on unseen data
* Visualization of training metrics

## 👩‍💻 Author

**Svitlana Melnyk**

Python / Data Science Developer

[GitHub](https://github.com/drrttlotr1)
