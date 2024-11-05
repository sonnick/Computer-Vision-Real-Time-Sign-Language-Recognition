# Real-Time Sign Language Recognition Using Computer Vision & Machine Learning¶

## Introduction
Sign Language Recognition (SLR) systems bridge the communication gap between individuals with speech and hearing impairments and those without. This project presents a machine learning-based method to recognize American Sign Language (ASL) fingerspelling gestures with 95.7% accuracy, covering all 26 letters of the alphabet. The system processes hand gestures, filters them, and applies a classifier to predict the correct ASL letter. Using neural networks and image processing techniques, this approach offers a promising tool for improving communication accessibility.

![amer_sign2](https://github.com/user-attachments/assets/51d762c2-dbe1-4942-b1f5-0f72d667c8ff)


## Dataset
This project leverages the Sign Language MNIST dataset, a reworked version of the classic MNIST format, specifically designed for ASL fingerspelling. Key features of the dataset:

* Classes: 24 classes for ASL letters A-Z, excluding "J" and "Z," as these require motion.
* Format: Each image is a 28x28 grayscale (0-255) pixel image stored as CSV rows with labels.
* Size: Training set includes 27,455 images, while the test set comprises 7,172 images.
* Data Augmentation: The original hand gestures were augmented with various filters and transformations to improve model robustness and generalization. * Augmentations included cropping, resizing, gray-scaling, pixelation, brightness adjustments, and slight rotations.

  ![amer_sign3](https://github.com/user-attachments/assets/ee68a02a-e440-4537-85d0-a139315b49a1)


## Project Overview
1. Problem Statement:
   
Recognizing ASL gestures in real-time requires both accuracy and efficiency due to the dynamic nature of hand gestures and finger positions. Our goal is to create a model capable of accurately recognizing these static gestures in real-time, enabling smoother communication between ASL users and non-users.
![american_sign_language](https://github.com/user-attachments/assets/9962cde8-825d-4569-9054-733c77a9cb7c)


3. Methodology:
   
* Image Preprocessing: Hand gestures are preprocessed with image enhancements to improve class separability.
* Model Architecture: A convolutional neural network (CNN) is employed to classify each gesture.
* Training and Evaluation: The model was trained on the Sign Language MNIST dataset and evaluated on a separate test set, achieving 95.7% accuracy.

4.  Key Technologies: 
* Machine Learning: Neural networks, specifically CNNs, for image classification.
* Image Processing: OpenCV and ImageMagick for preprocessing images.

## PREDCTING ON LIVE WEBCAM
This final section captures live video from the default camera and processes the frames in real-time for sign language recognition. It defines a specific region of interest (ROI) within the captured frame, which is then converted to grayscale and resized to 28x28 pixels to match the input requirements of the trained model. A rectangle is drawn around the ROI for visual reference, and the model predicts the corresponding sign language letter from this region. The predicted letter is overlaid onto the original frame, allowing for real-time feedback. The loop continues to capture and process frames until the Enter key is pressed, at which point the video capture is released, and all OpenCV windows are closed. This demonstrates how we have used computer vision and machine learning for real-time sign language interpretation.

## Sign for Letter   B
<img width="505" alt="Capture B" src="https://github.com/user-attachments/assets/06027ac3-12a0-4a35-a3c1-e928bf165f8f">

## Sign for Letter C
<img width="960" alt="Cap C" src="https://github.com/user-attachments/assets/dcfb2aa4-bc8c-42a7-828a-dda4023adc5e">

## Sign for Letter O
<img width="960" alt="Capture 0" src="https://github.com/user-attachments/assets/7017a12d-ca31-4c6c-a1a2-d51b488a6bbe">




