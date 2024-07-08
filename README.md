# YOLO: You Only Look Once

YOLO (You Only Look Once) is a state-of-the-art, real-time object detection system. Unlike traditional object detection algorithms that repurpose classifiers or localizers to perform detection, YOLO applies a single neural network to the full image. This network divides the image into regions and predicts bounding boxes and probabilities for each region. These bounding boxes are weighted by the predicted probabilities.

## Key Features

- **Speed:** YOLO is incredibly fast. Since it frames detection as a single regression problem, it can predict the type and location of objects in an image with just a single network evaluation.
- **Accuracy:** YOLO achieves high accuracy in detecting various objects. The network's unified architecture allows it to efficiently reason globally about the full image and all the objects in it.
- **Versatility:** YOLO is versatile and can be used for a variety of applications, from real-time detection on videos to large-scale batch processing.

## How It Works

YOLO takes an input image and divides it into an S x S grid. For each grid cell, it predicts B bounding boxes, confidence scores for these boxes, and C class probabilities. These predictions are then combined to generate the final detection results.

### Steps:
1. **Image Division:** The input image is divided into an S x S grid.
2. **Bounding Box Prediction:** For each grid cell, B bounding boxes are predicted. Each bounding box includes coordinates (x, y, w, h) and a confidence score.
3. **Class Probability Prediction:** Each grid cell also predicts class probabilities for C classes.
4. **Combining Predictions:** The bounding boxes with high confidence scores are kept, and non-max suppression is applied to remove duplicate detections.

## Applications

- **Autonomous Driving:** Detecting pedestrians, vehicles, and other objects in real-time.
- **Security Systems:** Monitoring surveillance footage for suspicious activities.
- **Retail Analytics:** Analyzing customer behavior and product placement.
- **Robotics:** Enabling robots to interact with and understand their environment.
