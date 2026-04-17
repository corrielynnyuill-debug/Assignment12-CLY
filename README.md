# Assignment12-CLY
# Fashion-MNIST Image Classification Using Feedforward Neural Networks

A feedforward neural network built with TensorFlow/Keras to classify grayscale fashion images from the [Fashion-MNIST](https://github.com/zalandoresearch/fashion-mnist) dataset into 10 categories.

## Dataset

Fashion-MNIST contains 70,000 28×28 grayscale images (60,000 train / 10,000 test) across 10 classes:

| Label | Class         |
|-------|---------------|
| 0     | T-shirt/Top   |
| 1     | Trouser       |
| 2     | Pullover      |
| 3     | Dress         |
| 4     | Coat          |
| 5     | Sandal        |
| 6     | Shirt         |
| 7     | Sneaker       |
| 8     | Bag           |
| 9     | Ankle Boot    |

## Model Architecture

```text
Input (28×28) → Flatten (784) → Dense(128, ReLU) → Dropout(0.3)
→ Dense(128, ReLU) → Dropout(0.3) → Dense(10, Softmax)
Optimizer: Adam · Loss: Categorical Cross-Entropy · Epochs: 20

Results
Metric	Value
Test Accuracy	~88.5%
Best F1	0.97 (Trouser)
Lowest F1	0.72 (Shirt)


Quick Start
pip install tensorflow matplotlib scikit-learn seaborn numpy

python fashion_mnist_nn.py

Repository Contents
├── fashion_mnist_nn.py      # Full training and evaluation pipeline
├── fashion_mnist_report.pdf  # Two-page written report
└── README.md

Key Takeaways
Feedforward networks achieve strong baseline accuracy on Fashion-MNIST, surpassing the ~83.5% human benchmark.

Upper-body categories (Shirt, T-shirt, Pullover, Coat) account for most misclassifications due to visual similarity.

Future work includes CNNs, transfer learning (ResNet/VGG), and data augmentation.

License
This project was developed for academic purposes as part of a Business Intelligence Analyst program.
