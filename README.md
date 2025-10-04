# 🐱🐶 Cat vs Dog Image Classifier with TensorFlow and Gradio

This project is a deep learning image classifier that distinguishes between cats and dogs using a pre-trained **MobileNetV2** model. 
It uses TensorFlow for model building and training, and Gradio for an interactive web interface to make predictions.

---

## 📁 Dataset

We use the [Cats and Dogs Filtered Dataset](https://storage.googleapis.com/mledu-datasets/cats_and_dogs_filtered.zip) provided by Google:

- ~2,000 images for training (cats and dogs)
- ~1,000 images for validation

The dataset is automatically downloaded and extracted in the code.

---

## 🏗️ Model Architecture

- **Base Model:** MobileNetV2 (pre-trained on ImageNet, with weights frozen)
- **Input Size:** 224x224
- **Augmentation:** Random rotations, shifts, zoom, and flips for robust training
- **Output Layer:** Binary classification (Cat = 0, Dog = 1)

---

## 📈 Training Overview

Data is preprocessed using `ImageDataGenerator` with data augmentation for the training set. After training, the model's accuracy and loss on both training and validation sets are visualized.

**Metrics Tracked:**
- Training Accuracy & Loss
- Validation Accuracy & Loss

---

## 🎯 Prediction Function

After training, you can upload an image and receive predictions:

- If confidence > **85%** → 🐶 Dog
- If confidence < **15%** → 🐱 Cat
- Else → ❓ Unknown Image (Not confidently a cat or dog)

---

## 🧪 Gradio Interface

An easy-to-use Gradio web interface is provided. Just upload an image to get a prediction.

**Gradio Input:**
- Image (uploaded by user)

**Gradio Output:**
- Prediction label with confidence score

---

### ✅ Requirements

Make sure you have the following Python libraries installed:

```bash
pip install tensorflow gradio matplotlib numpy
