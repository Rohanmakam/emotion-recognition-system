# Facial Emotion Recognition using Neural Networks

A real-time facial emotion recognition system built with Python, OpenCV, and a Neural Network trained using the Backpropagation algorithm. This project detects faces from a camera feed or static images and classifies the dominant emotion.

![Project Demo GIF](https://your-link-to-a-demo-gif.com/demo.gif)
## 📋 Table of Contents
- [About The Project](#about-the-project)
- [Features](#features)
- [System Workflow](#system-workflow)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
- [Model Evaluation](#model-evaluation)
- [Future Work](#future-work)
- [License](#license)
- [Contact](#contact)

## 📖 About The Project

This project presents a machine learning model capable of identifying human emotions from facial expressions. The core of the system is a Neural Network trained with the **Backpropagation algorithm** on a diverse dataset of faces, including various genders, races, and accessories like spectacles or beards.

The system uses a combination of classic and modern computer vision techniques:
* **Haar Cascade Classifiers** for robust, real-time face detection.
* **Canny Edge Detection** for extracting crucial facial features like the contours of eyes and mouth.
* A custom **Neural Network** for classifying the extracted features into distinct emotions.

### Built With
* [![Python][Python.shield]][Python.url]
* [![OpenCV][OpenCV.shield]][OpenCV.url]
* [![TensorFlow][TensorFlow.shield]][TensorFlow.url] (or Keras/PyTorch)
* [![NumPy][NumPy.shield]][NumPy.url]

## ✨ Features
- **Real-time Emotion Detection**: Analyzes video feed from a webcam to detect emotions live.
- **Image-based Recognition**: Can predict emotions from static image files.
- **Multi-Expression Classification**: Recognizes a range of emotions (e.g., Happy, Sad, Angry, Neutral, Surprise).
- **Confidence Score**: Outputs the predicted emotion along with the model's confidence level.
- **Robust Face Detection**: Works with a variety of faces, including those with glasses, moustaches, and beards.

## ⚙️ System Workflow

The project follows a clear pipeline from input to output:

1.  **Input**: Receives an image or a video frame.
2.  **Face Detection**: A pre-trained Haar Cascade Classifier scans the image to locate a human face.
3.  **Preprocessing**: The detected facial region is cropped, converted to grayscale, and resized to a standard size (e.g., 48x48) to ensure consistency.
4.  **Feature Extraction**: Canny Edge Detection is applied to the grayscale face to highlight the essential edges that define the expression.
5.  **Classification**: The resulting feature map is fed into the trained Neural Network, which classifies the emotion.
6.  **Output**: The system overlays the predicted emotion and confidence score on the original image/video feed.

## 🚀 Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

Make sure you have Python 3.8+ and pip installed.
```sh
pip install opencv-python tensorflow numpy
