
# Face Detection and Anti-Spoofing

## Overview
Welcome to the **Face Detection and Anti-Spoofing** GitHub repository! This repository contains code and resources for building a model to detect whether a person is real or a spoof using computer vision techniques. We employ a **Convolutional Neural Network (CNN)** for this purpose, in conjunction with a **pre-trained face detection model** from **MediaPipe**.

## Project Overview
In today's digital age, ensuring the authenticity of individuals captured by security cameras is of paramount importance. The goal of this project is to develop a robust solution that can distinguish between real individuals and spoof attempts. Spoofing can include methods like displaying a photograph or using a video feed to deceive the camera.

We utilize a **CNN-based anti-spoofing model** trained on a dataset of real and spoof faces. This model is integrated with **MediaPipe's face detection** to identify faces in real-time and classify them as either **Real** or **Spoof**.

## Key Features:
- **Real-time Face Detection**: Using MediaPipe, the model detects faces from the webcam feed.
- **Spoof Detection**: The model distinguishes between real faces and spoof attempts, making it suitable for security and authentication purposes.
- **Integration**: Combines the power of MediaPipe's face detection and a custom anti-spoofing model for a comprehensive solution.

## Dependencies:
To run the project, you'll need the following Python libraries:
- `tensorflow`: For loading and using the anti-spoofing CNN model.
- `opencv-python`: For capturing webcam frames and processing images.
- `mediapipe`: For face detection.
- `numpy`: For image array manipulations.

## Setup Instructions:
1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-username/Face_detection_anti_spoofing.git
   cd Face_detection_anti_spoofing
   ```

2. **Install dependencies**:
   You can install the required dependencies using `pip`:
   ```bash
   pip install -r requirements.txt
   ```

3. **Download Pre-trained Model**:
   Ensure that the pre-trained model (e.g., `spoof2.h5`) is available in your working directory or provide the correct path to it in the script.

4. **Run the Detection**:
   The model is designed to work with a webcam. Run the following command to start real-time face and spoof detection:
   ```bash
   python anti_spoofing.py
   ```

   The script will open your webcam, detect faces, and label them as **Real** or **Spoof**. Press "q" to exit the webcam feed.

## How it Works:
1. **Face Detection**: The script captures webcam frames and processes them using **MediaPipe**'s face detection model. It identifies the location of faces in each frame.
2. **Anti-Spoofing Classification**: Once a face is detected, the cropped face image is passed through the **anti-spoofing CNN** to predict if the person is real or a spoof.
3. **Display Results**: The webcam feed displays the real-time face detection, with labels indicating whether the person is real or a spoof.

## Example Output:
The model will display the webcam feed with annotations showing whether each detected face is **Real** or **Spoof**.

## Conclusion:
This project provides a solution for distinguishing between real and spoof faces in real-time using **face detection** and **deep learning**. It is a valuable tool for building secure systems where authentication or identity verification is crucial.

