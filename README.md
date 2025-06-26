# Python_ML_NN_Projects

WEAPON DETECTION USING YOLO
===========================

This project implements a real-time weapon detection system using YOLO (You Only Look Once) object detection models. It enhances surveillance by identifying weapons from video streams or images and playing an audio alert when a weapon is detected.

PROJECT STRUCTURE
-----------------
- final_code.ipynb        : Model training, evaluation, and inference
- preprocessing.ipynb     : Converts annotations and prepares data
- dataset/                : Raw image and annotation data
- weapon_detection/
    - images/             : YOLO training/validation images
    - labels/             : YOLO-compatible label files
- data.yaml               : Dataset config for YOLO
- README.txt              : Project documentation

FEATURES
--------
- Converts JSON annotations to YOLO format (.txt)
- Trains YOLOv5 and YOLOv8 models on weapon datasets
- Evaluates models and logs metrics (mAP, precision, recall)
- Runs real-time inference using webcam or video file
- Plays sound alert when a weapon is detected with confidence

REQUIREMENTS
------------
Install required packages:
> pip install -r requirements.txt

Main dependencies:
- ultralytics
- torch
- opencv-python
- playsound

DATA PREPROCESSING
------------------
Run preprocessing.ipynb to:
- Convert JSON bounding box annotations to YOLO format
- Clean up label file extensions (.jpg.txt to .txt)

Ensure folder structure matches YOLO's format.

MODEL TRAINING
--------------
Run final_code.ipynb to:
- Load pretrained YOLOv5 or YOLOv8 models
- Fine-tune using your weapon dataset
- Save trained model to .pt format

Make sure data.yaml points to correct image and label paths.

EVALUATION & INFERENCE
----------------------
- Use model.val() to compute mAP and performance
- Detect weapons in live video feeds
- Bounding boxes and labels shown on screen
- Audio alert triggered for confident weapon detections

DISCLAIMER
----------
This project is for educational and research purposes. Use in real-world scenarios requires rigorous validation.

AUTHOR
------
Aravindh Tiruchirapalli Seetharaman

