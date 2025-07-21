Driver Drowsiness and Yawn Detection
This project is a real-time driver drowsiness and yawn detection system using computer vision and deep learning. It employs a Convolutional Neural Network (CNN) trained to classify facial states (eyes open, eyes closed, yawn, no yawn) from webcam images to help increase road safety by alerting users when signs of fatigue or drowsiness are detected.

Features
Real-time detection of yawning and open/closed eye states using a webcam

Image preprocessing with OpenCV, including grayscale conversion and resizing

Deep learning classification using a CNN built and trained with TensorFlow/Keras

Automatic alert (sound alarm) when drowsiness is detected based on eye state over consecutive frames

Modular Python implementation for easy integration and future expansion

Dataset
Source: Kaggle Drowsiness Dataset by dheerajperumandla

Classes: yawn, no_yawn, Closed, Open

The dataset includes thousands of labeled images representing various eye and mouth states, supporting robust model training

Installation and Requirements
Python 3.7+

TensorFlow and Keras

OpenCV

playsound (for alarm functionality)

NumPy, Pillow (PIL), Matplotlib (for experiments and visualization)

Install dependencies with:

bash
pip install tensorflow opencv-python playsound numpy pillow matplotlib
How It Works
The webcam feed is continuously processed.

Face and eye regions are detected using Haar cascades.

Each detected eye region is preprocessed and passed through the trained CNN model, which predicts whether the eyes are open or closed.

If both eyes are detected as closed for a threshold number of consecutive frames, an audible alarm is played.

Yawn detection can be implemented similarly by training the model to recognize mouth states.

Usage
Download or train the model (drowsiness_model.h5) and ensure you have the Haar cascade XML files and an alarm audio file in the appropriate directories. Run the main script:

bash
python detect.py
To customize the alarm threshold or paths, modify the configuration section of the script.

Acknowledgments
Dataset courtesy of Kaggle user dheerajperumandla

Built using TensorFlow, Keras, OpenCV, and standard Python libraries

This project demonstrates practical, real-time computer vision techniques for helping prevent drowsiness-related accidents, and it can be adapted for integration into vehicle safety platforms or monitoring applications.
