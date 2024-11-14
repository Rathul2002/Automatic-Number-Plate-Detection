# Automatic-Number-Plate-Detection
# Automatic Number Plate Recognition (ANPR) System

This project is an Automatic Number Plate Recognition (ANPR) system developed in Python. The system uses OpenCV, Tesseract OCR, and Haarcascade to detect and read vehicle license plates from images. When a plate is successfully recognized, the extracted number is sent via email to a specified address.

## Features

- Detects vehicle number plates in an image using two different algorithms:
  - **Algorithm 1**: Edge detection and contour-based detection.
  - **Algorithm 2**: Haarcascade-based detection.
- Extracts the number plate text using Tesseract OCR.
- Compares results from both algorithms and selects the best output.
- Sends an email notification with the detected plate number.

## What is Haarcascade?

Haarcascade is an object detection algorithm based on machine learning, commonly used to detect faces, number plates, and other objects in images.
Here’s how it works in this project:

1. **Feature Extraction**: Haarcascade extracts specific patterns (Haar features) from an image, which are rectangular shapes capturing contrasts (e.g., edges, lines).
2. **Cascade Classifier**: The algorithm applies a series of classifiers in stages, where each classifier is trained to detect specific patterns. The cascade process helps quickly eliminate unlikely regions, focusing on the areas that might contain the target object (e.g., a number plate).
3. **Real-Time Detection**: The sliding window approach allows Haarcascade to scan different regions and scales in an image, making it effective for real-time detection.

In this project, Haarcascade uses a pre-trained XML file (`haarcascade_russian_plate_number.xml`) to detect number plates in images, improving the accuracy of our system.

## Requirements

- Python 3.x
- OpenCV (`cv2`)
- Numpy (`numpy`)
- Imutils (`imutils`)
- Pytesseract (`pytesseract`)
- Regex (`re`)
- SMTPLib (included with Python)

## Installation

1. **Install required libraries**:
   ```bash
   pip install opencv-python numpy imutils pytesseract
