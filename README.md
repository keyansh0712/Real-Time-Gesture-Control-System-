# Real-Time-Gesture-Control-System-
## Overview
This project focuses on recognizing hand gestures using a webcam and performing specific actions based on the detected gestures. The primary objective is to detect a specific hand gesture (e.g., a gesture with three or more defects between fingers) and execute a predefined action (e.g., pressing the 'space' key) using the pyautogui library.
## Implementation
Region of Interest (ROI): Defines a rectangular area in the video feed to focus on the hand.
Gaussian Blur: Smooths the image to reduce noise.
HSV Color Space Conversion: Converts the image from BGR to HSV color space for better skin color detection.
Binary Mask Creation: Creates a binary image where skin color is white and the rest is black.
Morphological Transformations: Applies dilation and erosion to remove background noise.
