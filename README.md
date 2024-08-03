# Real-Time-Gesture-Control-System-
## Overview

This project focuses on recognizing hand gestures using a webcam and performing specific actions based on the detected gestures. The primary objective is to detect a specific hand gesture (e.g., a gesture with three or more defects between fingers) and execute a predefined action (e.g., pressing the 'space' key) using the `pyautogui` library.

## Implementation

### Image Processing
- Region of Interest (ROI): Defines a rectangular area in the video feed to focus on the hand.
- Gaussian Blur: Smooths the image to reduce noise.
- HSV Color Space Conversion: Converts the image from BGR to HSV color space for better skin color detection.
- Binary Mask Creation: Creates a binary image where skin color is white and the rest is black.
- Morphological Transformations: Applies dilation and erosion to remove background noise.

### Contour Detection
- Contour Finding: Identifies contours in the thresholded image.
- Convex Hull and Defects: Calculates the convex hull and convexity defects of the largest contour.
- Finger Defect Detection: Uses convexity defects to detect spaces between fingers.
- Angle Calculation: Uses the cosine rule to calculate the angles at the defects to identify finger positions.

### Gesture Detection and Action
- Defect Counting: Counts the number of convexity defects with angles less than or equal to 90 degrees.
- Action Triggering: If the number of defects is greater than or equal to 3, trigger the predefined action (e.g., pressing the 'space' key).

### Display
- Results Display: Shows the processed video feed with the detected gestures.

## Features
- Gesture Recognition: Recognizes specific hand gestures based on contour and defect analysis.
- Action Execution: Executes predefined actions based on recognized gestures.
- Real-time Processing: Processes video feed in real-time for immediate feedback.

## User Interaction
1. Run the Script: Execute the script to capture video from the webcam.
2. Perform Gesture: Place your hand inside the defined rectangle area and perform the gesture with three or more defects (e.g., extending three or more fingers).
3. Observe Action: The script will press the 'space' key when the gesture is detected.
4. Exit: Press 'q' to quit the video feed and close the application.

## Summary
This project provides a basic framework for gesture recognition and can be extended with more complex gesture detection and actions. It demonstrates the use of computer vision techniques for real-time hand gesture recognition and interaction with the system.

## Requirements
- Python 3. x
- OpenCV
- NumPy
- pyautogui
- Matplotlib (optional, for visualization)

## Installation
1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/hand-gesture-recognition.git
    cd hand-gesture-recognition
    ```

2. Install the required libraries:
    ```sh
    pip install -r requirements.txt
    ```

3. Run the script:
    ```sh
    python gesture_recognition.py
    ```

## References
- [OpenCV Documentation](https://docs.opencv.org/)
- [pyautogui Documentation](https://pyautogui.readthedocs.io/en/latest/)
- [numpy Documentation](https://numpy.org/doc/stable/)
- [matplotlib Documentation](https://matplotlib.org/stable/contents.html)

---

Feel free to modify and extend this project to suit your needs. Contributions are welcome!
