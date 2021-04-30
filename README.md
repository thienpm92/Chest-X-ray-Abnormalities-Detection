# Chest-X-ray-Abnormalities-Detection

Project apply VinBigData Chest X-ray dataset to detect abnormalities  using Yolo5 of https://github.com/ultralytics/yolov5 as the detector. Dataset get from https://www.kaggle.com/c/vinbigdata-chest-xray-abnormalities-detection

# Pre-processing data
python pre_processing_data.py 
python split_data.py 

# Training 
train.py --img 640 --batch 16 --epochs 5 --data models/data.yaml --weights yolov5x.pt

# Testing
python detect.py --weights runs/train/exp2/weights/best.pt --img 640 --conf 0.25 --source data/images/train/000d68e42b71d3eac10ccc077aba07c1.jpg
