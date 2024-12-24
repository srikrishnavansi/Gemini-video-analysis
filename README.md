# Gemini-video-analysis
# Basic Video Object Detection and Annotation with Gemini

This project provides a basic demonstration of using Google's Gemini large language model to perform object detection and annotation on video files. It processes a video, sends frames to Gemini for analysis, and then draws bounding boxes around detected objects in the output video.

## Overview

This initial version focuses on demonstrating the core functionality of combining Gemini's vision capabilities with OpenCV for video processing. It reads a video file, sends the video (after processing) to Gemini with a prompt, receives JSON data containing object information (bounding boxes, etc.), and finally draws those bounding boxes on the video frames to create an annotated output video.

## Features

*   **Video Upload and Processing:** Uploads and processes a local video file for analysis.
*   **Gemini API Integration:** Uses the Gemini API to analyze the uploaded video based on a user-defined prompt.
*   **JSON Response Handling:** Parses the JSON response from Gemini containing object detection data.
*   **Bounding Box Drawing:** Draws bounding boxes around detected objects on the video frames using OpenCV.
*   **Basic Error Handling:** Includes basic error handling for JSON parsing.

## Getting Started

### Prerequisites

*   A Google Cloud project with the Gemini API enabled.
*   A Google Cloud API key or service account credentials.
*   Python 3.7+
*   Required Python packages (install with `pip install -r requirements.txt`):
    *   `google-generativeai`
    *   `opencv-python`
    *   `numpy`
    *   `requests`

### Installation

1.  Clone the repository:

```bash
git clone [https://github.com/your-username/your-repository-name.git](https://github.com/your-username/your-repository-name.git) # Replace with your repo URL
cd your-repository-name
