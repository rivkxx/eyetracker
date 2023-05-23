Table of Contents
Introduction
Installation
Usage
Configuration
Eye Tracking Algorithm
Dependencies
Contributing
License
Introduction
The Eye-Tracking App is designed to track the movement of a user's eyes using a camera feed. It utilizes the OpenCV library and the Dlib facial landmarks predictor to detect and track the eyes in real-time. The app can serve as a starting point for developing more advanced eye-tracking systems or conducting eye-related research.

Installation
To use the Eye-Tracking App, you need to follow these installation steps:

Clone the repository:

shell
Copy code

git clone https://github.com/your-repository.git
cd eye-tracking-app

Install the required dependencies:

shell
Copy code
pip install -r requirements.txt
Download the shape predictor file:

Download the pre-trained shape predictor file (shape_predictor_68_face_landmarks.dat) from the Dlib website.
Extract the file and place it in the root directory of the Eye-Tracking App.
Run the app:

shell
Copy code
python eye_tracking_app.py
Usage
To use the Eye-Tracking App, follow these steps:

Ensure that your webcam or camera is connected and functioning properly.
Launch the Eye-Tracking App by running the eye_tracking_app.py script.
The app will open a new window displaying the camera feed.
The app will detect and track the user's eyes in real-time.
Perform any additional processing or analysis based on the eye movements as per your requirements.
Press the 'q' key to quit the app.
Configuration
The Eye-Tracking App provides a few configuration options that can be modified according to your needs. These options can be found in the eye_tracking_app.py script.

LEFT_EYE_INDEX and RIGHT_EYE_INDEX: These constants define the indices of the facial landmarks corresponding to the left and right eyes. Adjust these values if needed, based on the facial landmarks used by the shape predictor model.
python
Copy code
# Constants for eye landmarks
LEFT_EYE_INDEX = 36  # Example value, modify if needed
RIGHT_EYE_INDEX = 45  # Example value, modify if needed
Eye Tracking Algorithm
The Eye-Tracking App utilizes a basic eye tracking algorithm that tracks the movement of the eyes based on the center points of the detected eyes. The algorithm performs the following steps:

The app captures video frames from the camera feed.
Each frame is converted to grayscale for face detection.
Faces are detected using the Dlib face detector.
Facial landmarks are extracted for each detected face using the Dlib shape predictor.
The eye coordinates are extracted from the facial landmarks.
The center points of the left and right eyes are calculated using the extracted eye coordinates.
The eye movement is tracked by analyzing the changes in the position of the eye centers over time.
The eye tracking algorithm provided in this app is a basic implementation. For more accurate
