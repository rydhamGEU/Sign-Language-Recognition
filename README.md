# Sign-Language-To-Text-and-Speech-Conversion

## Abstract  
Sign language is one of the oldest and most natural forms of communication. This project presents a real-time method using neural networks for recognizing finger-spelling-based American Sign Language (ASL). We propose a Convolutional Neural Network (CNN) method to recognize hand gestures captured by a camera. The purpose is to translate hand gestures into text and speech, making communication easier for the deaf and mute community. The system processes hand gestures through a classifier, training CNN with calibrated images to recognize and convert signs into audio and text output.

## Introduction  
American Sign Language is a predominant form of communication for people who are deaf or mute. Since verbal communication is not an option for them, sign language becomes essential. This project aims to build a model that recognizes finger-spelling-based gestures and converts them into text and speech. This will enable seamless communication between sign language users and non-users.

## Requirements  
Over 70 million people worldwide rely on sign language for communication. However, not everyone understands sign language. This project aims to bridge that communication gap by developing a user-friendly Human-Computer Interface (HCI) that can recognize ASL gestures and translate them into readable text and spoken words.

## Objective  
To create a computer software that utilizes CNN to recognize American Sign Language hand gestures and convert them into both text and speech.

## Scope  
This system benefits both the deaf/mute community and those who do not understand sign language. The user simply performs gestures, and the system interprets them into text and audio, facilitating easy communication.

## Modules

### 1. Data Acquisition  
- Data collection can be done using electromechanical devices like gloves, but they are expensive.  
- A more efficient approach is vision-based detection using a webcam to capture hand gestures.  
- Challenges include variations in hand movements, skin color, lighting, and backgrounds.  

### 2. Data Pre-processing & Feature Extraction  
- Hand detection is performed using the Mediapipe library.  
- The Region of Interest (ROI) is cropped, converted to grayscale, and processed using OpenCV filters.  
- Adaptive thresholding is applied to obtain binary images for better recognition.  
- To handle background and lighting variations, landmark points from Mediapipe are drawn on a plain white background, improving accuracy.

### 3. Gesture Classification Using CNN  
- CNN is a powerful tool for image recognition, consisting of convolutional layers, pooling layers, and fully connected layers.  
- The model learns features at different levels and assigns probabilities to each gesture.  
- Initially, 26 individual gestures were classified, but due to low accuracy, the alphabets were grouped into 8 similar classes.  
- Further refinement using mathematical operations on hand landmarks improved accuracy.  
- Final accuracy achieved: **97% (without clean background) and 99% (with clean background and proper lighting).**  

### 4. Text-to-Speech Translation  
- Recognized gestures are translated into text and converted into speech using the `pyttsx3` library, simulating real-life dialogue.  

## Project Requirements

### Hardware  
- Webcam  

### Software  
- **Operating System:** Windows 8 and above  
- **IDE:** PyCharm  
- **Programming Language:** Python 3.9+  
- **Python Libraries:** OpenCV, NumPy, Keras, Mediapipe, TensorFlow  
