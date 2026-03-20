# Room Classification using MLP

## Overview
This project implements a Multi-Layer Perceptron (MLP) to classify room images into three categories:
- Bedroom
- Dining Room
- Living Room

The implementation is performed using PyTorch with a structured deep learning pipeline including preprocessing, training, evaluation, and visualization.

---

## Objectives
- Build an MLP model for image classification
- Understand forward propagation in neural networks
- Analyze model performance using visualizations
- Evaluate predictions on unseen data

---

## Dataset Structure
dataset/
├── bed_room/
├── dining_room/
└── living_room/

Each folder contains images belonging to its respective class.

---

## Workflow

### 1. Data Preprocessing
- Images resized to **64x64**
- Converted to tensors
- Flattened for MLP input
- Normalized (0–1 range)

### 2. Model Architecture (MLP)
- Input Layer: 12288 neurons (64×64×3)
- Hidden Layer 1: 512 neurons (ReLU)
- Hidden Layer 2: 256 neurons (ReLU)
- Output Layer: 3 neurons (Softmax)

### 3. Training
- Optimizer: Adam
- Loss Function: CrossEntropyLoss
- Epochs: 50
- Batch Size: 32

### 4. Evaluation
- Test Accuracy calculation
- Prediction analysis
- Class-wise performance

---

## Results

- Model achieved **low to moderate accuracy (~40–50%)**
- High number of incorrect predictions observed

---

## MLP Performance Analysis

### Why Accuracy is Low?
- Images are flattened → spatial structure lost
- MLP cannot capture patterns like edges or textures
- Fully connected layers are not suitable for image data

### Conclusion
MLP is useful for understanding neural networks but not effective for image classification tasks.

---

## Visualizations

All visual outputs are stored in the `Visuals/` folder:

- Training Loss Curve
- Training Accuracy Curve
- Correct vs Incorrect Predictions
- Class-wise Accuracy
- Prediction Grid
- Sample Images

---

## Folder Structure
Room-Classification/
│
├── dataset/
│ ├── bed_room/
│ ├── dining_room/
│ └── living_room/
│
├── notebooks/
│ └── room_classification_mlp.ipynb
│
├── Visuals/
│ ├── training_loss.png
│ ├── training_accuracy.png
│ ├── correct_vs_incorrect.png
│ ├── class_accuracy.png
│ ├── prediction_grid.png
│ ├── single_prediction.png
│ └── sample_images.png
│
└── README.md

---

## Technologies Used

- Python
- PyTorch
- NumPy
- Matplotlib
- PIL (Python Imaging Library)

---

## Key Learnings

- Understanding MLP architecture
- Importance of preprocessing in deep learning
- Limitations of MLP for image tasks
- Model evaluation using multiple metrics and visualizations

---

## Future Improvements

- Use Convolutional Neural Networks (CNN)
- Apply data augmentation
- Improve dataset quality
- Use transfer learning (ResNet, VGG)

---

## Author
Osam Sami

---

## License

This project is licensed under the MIT License.
