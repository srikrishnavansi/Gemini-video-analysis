# Video Object Analysis and Annotation Using Gemini and OpenCV

This project focuses on analyzing video content to detect and annotate objects using Google Gemini's generative AI capabilities, combined with OpenCV for video processing and annotation. The result is an annotated video that highlights all identified objects and features, along with their properties and appearance times.

---

## **Project Overview**

The main goal is to:
1. Analyze a video and identify all objects and features present throughout its duration.
2. Generate bounding boxes and metadata for each detected object, including its condition, time of appearance, and disappearance.
3. Annotate the video with bounding boxes and labels for all detected objects.

The output is an annotated video that visually displays the identified objects, providing valuable insights into the video's content.
Output video:
   ![Output Video](Gemini-video-analysis/video.mp4_upload")

## **Features**

- **Object Detection**: Identifies all visible objects in the video, along with their properties (e.g., name, condition, bounding boxes, and timestamps).
- **AI-Powered Analysis**: Utilizes Google Gemini's generative AI model for object detection and metadata generation.
- **Dynamic Video Annotation**: Applies bounding boxes and labels to objects in the video based on their appearance.
- **Error Handling**: Includes robust error-handling mechanisms for incomplete data and invalid bounding box formats.

---

## **Project Workflow**

1. **Video Upload**: 
   - The video is uploaded and processed using Google Gemini's file management API.
   - The system waits for Gemini to finish processing the video before proceeding.

2. **Video Analysis**: 
   - The video's length is calculated using OpenCV to ensure annotations cover the entire duration.
   - A detailed prompt is sent to Gemini for object detection and metadata extraction.

3. **Metadata Parsing**: 
   - The JSON response from Gemini is parsed to extract object information, including:
     - Object name
     - Condition
     - Bounding box coordinates
     - Appearance and disappearance timestamps

4. **Video Annotation**: 
   - OpenCV processes the video frame by frame.
   - Objects are annotated with bounding boxes and labels if they are visible in the current frame.
   - Unique colors are used for each object for clear visual distinction.

5. **Output Generation**: 
   - The annotated video is saved in MP4 format, displaying all detected objects with their respective metadata.

---

## **Dependencies**

To run this project, ensure you have the following dependencies installed:

- **Python 3.7 or above**
- Libraries:
  - `google.generativeai`
  - `opencv-python`
  - `opencv-python-headless`
  - `numpy`
  - `json`
  - `logging`

---

## **File Details**

### **Notebook File**
- The project code is saved in a Google Colab notebook for ease of execution and reproducibility.

### **Annotated Video**
- The output is saved as `annotated_video.mp4` in the working directory.

---

## **How to Run**

1. **Setup Dependencies**:
   - Install the required libraries using `pip`:
     ```bash
     pip install opencv-python opencv-python-headless google-generativeai numpy
     ```

2. **Run the Notebook**:
   - Open the provided Colab notebook.
   - Replace the `video_file_path` variable with the path to your input video.
   - Execute the cells in order.

3. **Output**:
   - The annotated video will be saved as `annotated_video.mp4` in the current working directory.

---

## **Approach Highlights**

1. **Prompt Engineering**:
   - A custom prompt is designed to extract comprehensive metadata for all objects in the video, covering the entire duration.
   - Dynamic video length integration ensures accurate start and end times for object annotations.

2. **AI and Vision Integration**:
   - Google Gemini handles high-level object detection and metadata generation.
   - OpenCV applies bounding boxes and renders annotations directly on the video frames.

3. **Error Handling**:
   - Missing or invalid metadata (e.g., malformed bounding boxes) is logged and skipped without interrupting the process.

---

## **Future Enhancements**

- Extend support for real-time object tracking across frames.
- Improve bounding box accuracy using advanced object detection models (e.g., YOLO or SSD).
- Add interactivity, such as allowing users to filter objects by type or condition in the annotated video.

---

## **Acknowledgements**

- This project leverages **Google Gemini** for object analysis and **OpenCV** for video processing and visualization.

---
