Spline Interpolation for Frame Rate Enhancement
Project Overview
This project implements spline interpolation to increase the frame rate of videos, enhancing visual smoothness and fidelity. It uses cubic spline interpolation, a numerical method well-suited for creating smooth transitions between video frames.

Team Members:
Narayan Soni - 2301240
Arjun Rao - 2197557

Team Name:

Environment Setup
Prerequisites
Python 3.8 or above
Pip package manager
MacOS - Apple Silicon


Requirements File
A requirements.txt file should include all necessary Python libraries:
numpy==1.26.4
scipy==1.13.0
opencv-python==4.9.0.80
matplotlib==3.8.4

Libraries Required
Install the required libraries using the following command:

pip install -r requirements.txt

Dataset
Source: Video from YouTube, representative of typical digital video content.
Frame Rate: Originally at 30 FPS, downsampled to 10 FPS for processing.
Duration: 15 seconds clip.

Preparing the Dataset
Download the video from YouTube.
Use a video processing tool to downsample the video to 10 FPS.
Trim the video to a length of 15 seconds.
Store the video at an absolute path and ensure it is correctly referenced in the script.

File Hierarchy

.
├── README.txt
├── ground truth.mp4
├── input.mp4
├── main.py
├── output2_video.mp4
├── output_video.mp4
└── requirements.txt



Usage
To run the spline interpolation script, navigate to the src/ directory and execute:

python3 main.py

Output
The script will generate a video with an increased frame rate, ensuring smoother playback. The results include the output video and possibly frames comparison plots if implemented in the script.

output_video.mp4: This is the primary output file where the video with enhanced frame rate, processed using cubic spline interpolation, is stored. The video will display smoother motion compared to the original due to the increased frame rate.
output2_video.mp4: This file may contain an alternative interpolation output or a variant of the enhancement process. (Please specify the exact nature of this file in the script comments or here if it has a specific purpose.)
Viewing Results
Check the project root directory for the output files. Play the videos to visually compare the enhanced smoothness in motion with the original input video.

