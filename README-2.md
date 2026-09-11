# Handwritten Digit Recognizer (MNIST + CNN)

A Convolutional Neural Network (CNN) built with TensorFlow/Keras that recognizes handwritten digits (0–9) using the MNIST dataset.

## 📌 Project Overview

This project trains a deep learning model to classify grayscale images of handwritten digits into one of 10 classes (0–9). It was built as part of a 1-Month Artificial Intelligence Internship project.

## 🛠️ Tech Stack

- **Python**
- **TensorFlow / Keras** — for building and training the CNN
- **NumPy** — for numerical operations on image arrays
- **Matplotlib** — for visualizing sample predictions
- **Google Colab** — development environment

## 📂 Dataset

The [MNIST dataset](http://yann.lecun.com/exdb/mnist/) consists of 70,000 grayscale images of handwritten digits (28x28 pixels):
- 60,000 training images
- 10,000 testing images

The dataset is loaded directly through `tensorflow.keras.datasets.mnist`, so no manual download is required.

## 🧠 Model Architecture

The CNN consists of:

1. **Conv2D (32 filters)** + **MaxPooling2D** — detects basic edges/patterns
2. **Conv2D (64 filters)** + **MaxPooling2D** — detects more complex patterns
3. **Conv2D (64 filters)** — detects high-level features
4. **Flatten** — converts feature maps into a 1D vector
5. **Dense (64 units, ReLU)** — combines features to make a decision
6. **Dense (10 units, Softmax)** — outputs a probability for each digit (0–9)

## ⚙️ Training Details

| Setting | Value |
|---|---|
| Optimizer | Adam |
| Loss Function | Sparse Categorical Crossentropy |
| Metric | Accuracy |
| Epochs | 10 |
| Validation Split | 10% |

## 📊 Results

The model achieves approximately **98–99% accuracy** on the unseen test dataset.

## 🖼️ Sample Predictions

The notebook displays 5 sample test images side-by-side with their predicted and actual labels, using Matplotlib.

## 🚀 How to Run

1. Open the notebook `MNIST_CNN_Digit_Recognizer.ipynb` in [Google Colab](https://colab.research.google.com/).
2. Run all cells in order (`Runtime` → `Run all`).
3. View the final test accuracy and sample predictions at the bottom of the notebook.

## 📁 Repository Structure

```
├── MNIST_CNN_Digit_Recognizer.ipynb   # Main Colab notebook with full code
└── README.md                          # Project documentation
```

## 🔮 Future Improvements

- Add a `Dropout` layer to reduce overfitting
- Train for more epochs to further improve accuracy
- Allow users to upload their own handwritten digit images for prediction
- Deploy the model as a simple web app (e.g., using Streamlit or Flask)

## 🙋 Author

Built as part of an AI Internship project.
