# Python Face Recognition

Python Face Recognition is a robust and versatile tool that leverages cutting-edge computer vision techniques to detect, recognize, and analyze faces in images or video streams. This project incorporates powerful libraries like OpenCV, dlib, and face_recognition to deliver functionalities ranging from basic face detection to attendance tracking using face recognition.

---

## Features

### Core Functionalities:
1. **Face Detection**: Accurately locate faces within images or video frames.
2. **Face Recognition**: Match detected faces with known individuals and label them accordingly.
3. **Attendance System**: Automatically mark attendance based on recognized faces and log timestamps.
4. **Facial Encoding**: Generate and store unique encodings for faces for efficient recognition.

### Additional Features:
- Real-time face tracking and analysis via webcam or video input.
- Display recognition accuracy as a percentage for better interpretability.
- Easy integration with external tools or applications through generated CSV attendance logs.

---

## Installation

### Prerequisites
Ensure Python 3.x is installed on your system. Additionally, install the following dependencies:

```bash
pip install opencv-python opencv-python-headless dlib face_recognition numpy
```

##Steps to Get Started
1. Clone this repository or download the project files:

```bash
git clone https://github.com/your-repo/python-face-recognition.git
cd python-face-recognition
```

2. Organize your known face images:
    - Place images in the Imageattend folder.
    - Ensure image filenames correspond to the person's name (e.g., elon.jpg).

3. Run the respective Python script based on your use case:
    - Basic Face Comparison:
    ```bash
    python basic.py
    ```

    - Real-Time Attendance System:
    ```bash
    python facerecog.py
    ```

# Usage
## Basic Face Comparison
- Compare two images (Images/elon musk.jpg and Images/elon test.jpg) to determine if they match.
- Displays the results on-screen, including match confidence.

## Real-Time Attendance System
- Capture video from your webcam and recognize known faces.
- Logs recognized individuals' names and timestamps in Attendance.csv.

# Code Overview
### basic.py
- Loads two images, detects faces, and computes facial encodings.
- Compares encodings to identify matches and calculates confidence levels.
- Displays the results with bounding boxes around detected faces.

### facerecog.py
- Preprocesses images in the Imageattend directory to compute known face encodings.
- Captures video, detects faces in real time, and compares them to the known encodings.
- Marks attendance for recognized faces in Attendance.csv, logging the name and timestamp.

# Customization
### Parameters
- Tolerance for Face Matching: Adjust the tolerance value in facerecog.py for stricter or more lenient matching.
- Image Resize: Modify the scale in imgSmall for faster processing.

### Extensions
- Integrate with cloud storage or databases for centralized attendance management.
- Add support for emotion recognition or age estimation using additional models.

# Contributing
Contributions are welcome! You can:

- Submit bug reports or feature requests via GitHub Issues.
- Create pull requests for enhancements or fixes.

# License
This project is open-source and available under the MIT License.
