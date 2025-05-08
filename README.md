# Facial_recognization
By CNN# Facial Emotion Detection with Song Recommendations

This project implements a facial emotion detection system using deep learning and provides song recommendations based on detected emotions.

## Project Structure
```
facial_recognition/
├── src/
│   ├── models/
│   │   └── emotion_model.py
│   ├── utils/
│   │   └── face_detector.py
│   ├── api/
│   │   └── app.py
│   └── data/
│       ├── raw/
│       └── processed/
├── tests/
├── venv/
├── requirements.txt
└── README.md
```

## Setup Instructions

1. Create and activate virtual environment:
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the API server:
```bash
python src/api/app.py
```

## API Usage

The API provides an endpoint for emotion detection and song recommendations:

- Endpoint: `/detect_emotion`
- Method: POST
- Input: Image file in the request body
- Output: JSON containing detected emotion, confidence score, and song recommendations

Example response:
```json
{
    "emotion": "happy",
    "confidence": 0.95,
    "song_recommendations": [
        "Happy - Pharrell Williams",
        "Walking on Sunshine - Katrina and the Waves"
    ]
}
```

## Features

- Real-time facial emotion detection using CNN
- Face detection using OpenCV
- REST API for emotion detection
- Song recommendations based on detected emotions
- Support for 7 emotions: happy, sad, angry, neutral, surprise, fear, and disgust 
