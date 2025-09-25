# Anecdote: Where Sound Meets Insight

## Overview
Anecdote is an advanced assistive technology designed to enhance accessibility for visually impaired users by combining real-time object detection, distance estimation, and adaptive audio feedback. The system offers a seamless experience for detecting objects, estimating their distance, and providing auditory feedback in multiple languages, ensuring ease of navigation and independence.

## Features

- Object Detection: Utilizes YOLOv8 for highly accurate and efficient real-time object detection.
- Distance Estimation: Dynamically calculates the proximity of detected objects using OpenCV. 
- Multilingual Audio Feedback: Converts detected objects and their distances into spoken feedback using Text-to-Speech (TTS).
- Web-Based Interface: Provides real-time interaction and live object tracking via a browser-based interface.
- Edge Detection Modes: Supports edge detection techniques like Canny, Sobel, and Laplacian of Gaussian (LoG) to enhance object visibility in challenging environments.
- Night Vision Modes: Implements CLAHE, Gamma Correction, and Histogram Equalization for enhanced visibility in low-light conditions.
- Detection Log: Maintains a record of all detected objects with their distances and modes, which can be exported as a PDF report. 



## Technology Stack

- YOLOv8: Deep learning-based object detection.

- OpenCV: Image processing and distance estimation.

- Flask: Backend framework for serving model predictions and managing the web interface.

- HTML/CSS & JavaScript: Frontend for real-time interaction.

- gTTS: Converts detections into real-time voice feedback.

- FPDF: Generates PDF reports for detection logs.

## How It Works

- Live Webcam Feed: Captures real-time video from the user’s webcam or connected camera.

- YOLOv8 Detection: Detects objects in the video feed with precise bounding boxes and classifications.

- Distance Calculation: Estimates the distance of detected objects based on their pixel dimensions and a predefined focal length.

- Audio Feedback: Announces detected objects and their distances via a Text-to-Speech system.

- Supports multiple languages, ensuring accessibility for diverse users.

- Night Vision Modes: Enhances visibility in low-light environments using:

  CLAHE (Contrast Limited Adaptive Histogram Equalization).

  Gamma Correction.

  Histogram Equalization.

- Edge Detection Modes: Offers additional visualization modes for edge detection:

  Canny Edge Detection

  Sobel Operator

  Laplacian of Gaussian (LoG)

## How to Operate

1) Start the Application

2) Run the cameraweb.py script using Python.

3) enter thye following command on the terminal:
     "C:/Users/bhard_og4n/AppData/Local/Programs/Python/Python310/python.exe" "c:/Users/bhard_og4n/Downloads/WEBSITE 2/cameraweb.py"

4) Click the “Go Live” button in the bottom right corner of the screen to start the live server.

5) Access the Web Interface

6) Control the Feed

7) Start the video feed by accessing /start_feed.

8) Stop the video feed via /stop_feed.

9) Switch Modes

   - Regular Detection: Access /video_feed.

   - Night Vision Modes: Access /video_feed_night?mode=[clahe|gamma|histogram].

   - Edge Detection Modes: Access /video_feed_edge?mode=[canny|sobel|log].

10) Generate Reports

11) Access /generate_pdf to download a PDF summary of the latest detections.

## Setup Instructions

- Requirements:

  1) Python 3.10.11

- Required Python Libraries:

  1) Flask

  2) Flask-CORS

  3) OpenCV

  4) gTTS

  5) pygame

  6) FPDF

  7) ultralytics

## Installation

- Clone the repository or download the project files.

- Install the required Python libraries:

- pip install flask flask-cors opencv-python-headless gtts pygame fpdf ultralytics

- Download the YOLOv8 model weights and place them in the specified directory.

- Update the paths in cameraweb.py to match your system’s directory structure.

- Example Usage: 

  Object Detection

  1) Detected objects and their distances are displayed on the video feed.

  2) Audio feedback announces the nearest object and its distance.

## Modes

- Standard Detection: Use /video_feed for normal lighting conditions.

- Night Vision: Enhance visibility using /video_feed_night?mode=[clahe|gamma|histogram].

- Edge Detection: Highlight edges with /video_feed_edge?mode=[canny|sobel|log].

## Generate PDF

- Access /generate_pdf to download a detailed detection log.

## Troubleshooting

- No Video Feed:
 
  1) Ensure the camera is connected and accessible.

  2) Restart the application if the camera feed freezes.

- Audio Feedback Issues:

  1) Ensure all dependencies are installed and working correctly.

  2) Check system audio settings.

- Error in Distance Calculation:

  1) Verify the KNOWN_WIDTH and FOCAL_LENGTH parameters are correctly set.

## Future Enhancements

- Integration with GPS for location-aware navigation.

- Advanced natural language processing for contextual feedback.

- Support for additional languages and regional dialects.

- Improved model accuracy with custom training data.

## Acknowledgments 

- YOLOv8: Object detection model.

- OpenCV: Real-time computer vision library.

- gTTS: Google Text-to-Speech API.

- Flask: Lightweight web framework.

## Acknowledgments

- YOLOv8: Object detection model.

- OpenCV: Real-time computer vision library.

- gTTS: Google Text-to-Speech API.

- Flask: Lightweight web framework.