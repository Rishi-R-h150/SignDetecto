# SignDetecto

**SignDetecto** is a Convolutional Neural Network (CNN)-based image classification project that recognizes hand signs and gestures and converts them into their corresponding words. This project can be used as a foundation for gesture-based communication tools.

---

## Project Overview

Sign language and hand gestures are essential for communication in various scenarios, including assisting people with hearing impairments. **SignDetecto** uses deep learning to classify images of hand gestures into predefined categories accurately.

The model is trained on labeled datasets of hand gestures and can recognize multiple classes of gestures.

---

## Features

- **Multiclass Classification:** Recognizes multiple hand gestures.  
- **Image Input:** Classifies hand gesture images from datasets or real-time input.  
- **Lightweight CNN:** Efficient and suitable for training on moderate hardware.  
- **Real-time Application Ready:** Can be extended to webcam-based gesture recognition.

---

## Model Architecture

The CNN architecture of **SignDetecto** is as follows:

| Layer (Type)                       | Output Shape       | Param #   |
|-----------------------------------|------------------|-----------|
| `Conv2D`                           | (28, 28, 75)     | 750       |
| `BatchNormalization`               | (28, 28, 75)     | 300       |
| `MaxPooling2D`                     | (14, 14, 75)     | 0         |
| `Conv2D`                           | (14, 14, 50)     | 33,800    |
| `Dropout`                          | (14, 14, 50)     | 0         |
| `BatchNormalization`               | (14, 14, 50)     | 200       |
| `MaxPooling2D`                     | (7, 7, 50)       | 0         |
| `Conv2D`                           | (7, 7, 25)       | 11,275    |
| `BatchNormalization`               | (7, 7, 25)       | 100       |
| `MaxPooling2D`                     | (4, 4, 25)       | 0         |
| `Flatten`                          | (400)            | 0         |
| `Dense`                            | (512)            | 205,312   |
| `Dropout`                          | (512)            | 0         |
| `Dense`                            | (24)             | 12,312    |

- **Total Parameters:** 264,049  
- **Trainable Parameters:** 263,749  
- **Non-trainable Parameters:** 300  

This architecture uses a combination of convolutional layers, batch normalization, max pooling, dropout, and fully connected layers to achieve robust gesture classification.

---

## Tech Stack

- **Programming Language:** Python  
- **Deep Learning Framework:** TensorFlow / Keras  
- **Data Handling:** NumPy, OpenCV  
- **Visualization:** Matplotlib, Seaborn  

---



```bash
git clone <repo-url>
