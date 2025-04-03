# Machinery Detection Using OpenAI & OpenCV

This project detects and analyzes machinery (excavators and dump trucks) in a video stream using OpenCV for image processing and OpenAI's Gemini API for object recognition. The system crops predefined areas of interest (AOI) from the video, sends them to the API, and logs the detected machinery details in a structured format.

## Features
- **Real-time Video Processing**: Captures frames from a video or webcam.
- **Region of Interest (ROI) Cropping**: Extracts specific areas for analysis.
- **AI-Based Machinery Detection**: Uses OpenAI's Gemini model for recognition.
- **Multi-threading for Efficiency**: Sends images asynchronously for faster processing.
- **Result Logging**: Saves responses in structured text files.

## Installation
### Prerequisites
Ensure you have Python 3.8+ installed along with the required libraries:
```sh
pip install opencv-python numpy openai
```

## Usage
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/machinery-detection.git
   cd machinery-detection
   ```
2. Add your OpenAI API key in the script (`api_key="YOUR_API_KEY"`).
3. Run the script:
   ```sh
   python machinery_detection.py
   ```
4. Press `q` to exit the video stream.

## How It Works
1. **Frame Capture**: Reads video frames from a file (`f1.mp4`) or webcam.
2. **ROI Selection**: Crops defined areas (`area` and `area1`) from each frame.
3. **Image Encoding**: Converts cropped images to Base64 format.
4. **AI Processing**: Sends images to Gemini API for machinery detection.
5. **Result Logging**: Saves structured detection results in text files.

## Example Response Format
```
| Machinery Name | Color | Status (Active/Inactive) | Company Name | Area |
|---------------|-------|--------------------------|--------------|------|
| Excavator     | Yellow| Active                   | CAT          | area |
```


