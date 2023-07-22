# Security-Camera-using-python
This is a Python project that utilizes the OpenCV library to create a real-time video recording program with face and body detection. The primary features of this program are as follows:

* Video capture
* Face and Body detection
* Recording on detection
* Video recording
* Video display
* Control and termination

# # OpenCV setup method 1:
pip3 install opencv-python

# # OpenCV setup method 2:
python -m pip install opencv-python

# Code explanation:

Import the necessary libraries:
cv2: OpenCV library for computer vision tasks.
time: Used for time-related operations.
datetime: Used for obtaining the current date and time.

Set up the video capture using the webcam (camera index 0)

Load Haar cascades for face and body detection

Initialize variables for video recording control

Set the frame size and the video codec for saving the output video

Start an infinite loop for capturing frames from the camera

Convert the captured frame to grayscale for faster processing

Detect faces and bodies in the grayscale frame using Haar cascades

Check if faces or bodies are detected

If detection is already in progress, reset the timer (timer_started) to prevent premature stoppage of recording. Otherwise, start recording by setting the detection flag to True, create a video writer object with a filename based on the current date and time, and print a message indicating that recording has started

If no faces or bodies are detected, but a previous detection was in progress, start a timer (timer_started) to keep track of how long recording should continue after the last detection. If the specified duration (seconds_to_record_after_detection) has elapsed, stop recording by resetting the flags and releasing the video writer. Then, print a message indicating that recording has stopped:

If recording is in progress (detection is True), write the current frame to the video file

Show the current frame with any detected faces/bodies in rectangles

Check if the user pressed 'q', which means they want to quit the program. If so, break out of the loop

Release the video writer and video capture objects, and close all OpenCV windows



