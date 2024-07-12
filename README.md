# AWS-service-lanuch-using-Finger
Hand Gesture Control for AWS Services
This Python script uses OpenCV and cvzone's HandTrackingModule to control AWS services based on hand gestures detected from a webcam feed.

# Features
+ EC2 Instance Control: Open and view EC2 instances on AWS.
+ S3 Bucket Creation: Create S3 buckets with unique names based on UUID.
+ penAI Chat Access: Open OpenAI's chat platform in a web browser.
+ Google Search: Perform a Google search.
+ Exit Application: Exit the application through smallest finger of your hand.

# Requirements
+ Python 3.x
+ OpenCV (cv2)
+ cvzone (HandTrackingModule)
+ AWS CLI configured

# Installation
1. Clone the repository:

    ```
    git clone <repository_url>
    ```
2. Install dependencies:
    ```
    pip install opencv-python
    pip install cvzone
    ```
3. Configure AWS CLI with appropriate credentials.

# Usage
1. Run the script:
    ```
   python hand_gesture_control.py
    ```

2. Choose actions by showing corresponding hand gestures:

+ Thumb Up: Launch EC2 instance and open AWS EC2 console.
+ Index Finger Up: Create an S3 bucket with a unique name and open AWS S3 console.
+ Thumb Up + Index Finger Up: Open OpenAI chat platform.
+ Index Finger Up + Middle Finger Up: Perform a Google search.
+ Pinky Finger Up: Exit the application.

3. Use gestures in front of the webcam to control the script.

# Code Explanation
+ Import Libraries: Import necessary libraries including cv2, os, time, uuid, and HandDetector from cvzone.HandTrackingModule.

+ Initialize Hand Detector: Create an instance of HandDetector to detect hands using the webcam feed.

+ Main Loop: Continuously capture frames from the webcam (cap) and detect hands (hand).

+ Gesture Detection: Depending on the detected hand gestures (fingers), execute corresponding actions:

   + Thumb Up: Execute ec2() to run an EC2 instance and open AWS EC2 console.
   + Index Finger Up: Execute s3(UUID) to create an S3 bucket with a unique name based on UUID and open AWS S3 console.
   + Thumb Up + Index Finger Up: Open OpenAI chat platform in a web browser.
   + Index Finger Up + Middle Finger Up: Perform a Google search using the default web browser.
   + Pinky Finger Up: Exit the application loop.
+ Display and Interaction: Display the webcam feed (photo) with annotated hand detection (image). Exit the application loop on 'Enter' key press.
