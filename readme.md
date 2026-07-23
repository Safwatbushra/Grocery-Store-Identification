# Camera-Based Product Detection System

A real-time grocery product detection system built with YOLOv8 and FastAPI.

## Project Overview
This system detects grocery items from images using a YOLOv8 object detection model
trained on a grocery store dataset. It exposes a REST API endpoint for image upload
and returns detected items in JSON format.

## Model Details
- Model: YOLOv8s (small)
- Framework: Ultralytics YOLOv8
- Training: 30 epochs
- Dataset: Grocery Store Dataset (Roboflow) - 809 images, 14 classes
- Pretrained on: COCO dataset (transfer learning)

## Detected Classes
Tomato, Carrot, Onion, Garlic, Ginger, Cucumber, Capsicum,
Brinjal, Mushroom, Leek Leaves, Redchilli, Solid Potato,
Sweet Potato, Beetroot

## How to Test API
1. Go to http://127.0.0.1:8000/docs
2. Click POST /detect
3. Click "Try it out"
4. Upload any grocery image
5. Click Execute
6. See JSON detection result

##  Project Structure
```
grocery-detection
├── main.py            # FastAPI application
├── best.pt            # Trained YOLOv8 model
├── requirements.txt   # Dependencies
└── README.md          # Project documentation
└── train.ipynb        # training notebook
```

