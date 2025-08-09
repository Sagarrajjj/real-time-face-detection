Real-Time Face Detection using OpenCV
This repository contains a simple yet effective project for real-time face detection using Python and the OpenCV library. The application captures video from your webcam, processes each frame, and draws a green rectangle around any detected human faces.

This is an excellent starting point for anyone interested in computer vision and can be used as a foundational component for more advanced projects like facial recognition, emotion analysis, or security systems.

Key Features
Real-Time Detection: Processes video frames from the webcam in real time.

Haar Cascade Classifier: Utilizes a pre-trained Haar Cascade classifier for efficient face detection.

Visual Feedback: Draws a green bounding box around each detected face.

Simple and Clean Code: The script is straightforward and easy to understand, making it ideal for learning.

Prerequisites
To run this project, you will need to have Python and the OpenCV library installed.

Python 3.x

OpenCV (cv2)

Installation and Usage
Follow these steps to set up and run the project on your local machine.

Step 1: Clone the Repository
First, clone this repository to your local machine using git.

git clone https://github.com/Sagarrajjj/real-time-face-detection
cd real-time-face-detection

Note: Replace your-username with your actual GitHub username.

Step 2: Install OpenCV
If you don't have OpenCV installed, you can easily install it using pip.

pip install opencv-python

Step 3: Run the Script
The project uses the haarcascade_frontalface_default.xml file, which is typically installed with the cv2 library. You need to make sure the path to this file is correct in your code. The provided script assumes it's in a standard location.

To run the script, simply execute the following command in your terminal:

python main.py

A window will open showing the live video feed from your webcam with faces detected and highlighted.

To exit the application, simply press the 'a' key on your keyboard.

Troubleshooting
If you encounter an error like cv2.error: (-5:Bad argument) in function 'detectMultiScale', please check your code for a typo. The correct keyword argument is minSize, not miSize.

# Correct code
faces = face_cap.detectMultiScale(
    col,
    scaleFactor=1.1,
    minNeighbors=5,
    minSize=(30, 30), # <-- Note the correct spelling: minSize
    flags=cv2.CASCADE_SCALE_IMAGE
)

License
This project is licensed under the MIT License.
