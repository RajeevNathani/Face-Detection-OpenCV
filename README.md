# Face-Detection-OpenCV

## Introduction

I have written a code in python which is used to detect faces using bounding rectangles. We can detect as much as many faces we want at a time. I have used MediaPipe package along with cv2. For preprocessing the RGB image, I used the MediaPipe Face Detection. 

### Here is the screenshot of an image in which my face has been detected in real time. 
In this image, my face captured in the mobile has also been detected.

![Screenshot (35)](https://user-images.githubusercontent.com/87267089/125443371-eac53adf-7049-4940-93b0-921ff816dd73.png)

## Configuration Options-

### MODEL_SELECTION
An integer index 0 or 1. Use 0 to select a short-range model that works best for faces within 2 meters from the camera, and 1 for a full-range model best for faces within 5 meters. For the full-range option, a sparse model is used for its improved inference speed. Default to 0 if not specified.

### MIN_DETECTION_CONFIDENCE
Minimum confidence value ([0.0, 1.0]) from the face detection model for the detection to be considered successful. Default to 0.5.

## Algorithm-

1. Firstly, import all the required libraries, here we need cv2 and MediaPipe.
2. Read the image using imread function in cv2 library.
3. Flip the image horizontally for a later selfie-view display.
4. Now, convert this image to RGB using cvtColor(image, cv2.COLOR_BGR2RGB).
5. Now, preprocess this modified image using MediaPipe Face Detection.
6. To improve performance, optionally mark the image as not writeable to pass by reference.
7. Finally, Draw the face detection annotations on the image.

