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

## How to Run

### 1. Clone the repository
git clone https://github.com/YOUR_USERNAME/grocery-detection.git
cd grocery-detection

### 2. Install dependencies
pip install -r requirements.txt

### 3. Run the API
uvicorn main:app --reload

### 4. Open browser
http://127.0.0.1:8000/docs

### API Usage

### Endpoint
POST /detect

### Input
- Image file (jpg, png)

### Output
```json
{
  "detections": [
    {
      "class": "Tomato",
      "confidence": 0.43
    }
  ]
}
```

## How to Test API
1. Go to http://127.0.0.1:8000/docs
2. Click POST /detect
3. Click "Try it out"
4. Upload any grocery image
5. Click Execute
6. See JSON detection result

##  Project Structure
grocery-detection/
├── main.py            # FastAPI application
├── best.pt            # Trained YOLOv8 model
├── requirements.txt   # Dependencies
└── README.md          # Project documentation
