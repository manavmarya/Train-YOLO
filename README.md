# Training YOLO v5 for custom database

Aims to train the database sourced from Webmarket dataset images (yuhang.rsise.anu.edu.au) based on the bounding boxes provided here:
github.com/ParallelDots/generic-sku-detection-benchmark/tree/master/annotatio….

## Data Pre-processing
1. Conversion from xyxy box system to xywh YOLO system with normalisation
2. Certain values exceeded the resolution of the image (assumed at the corner)

## Preparing for YOLO
1. Seperate labels (.txt file) for each image is created using csv data
2. YOLO git is cloned from https://github.com/ultralytics/yolov5.git

## Training settings
1. Training: Validation ratio is kept at 9:1
2. Images are trained at 640x480 pixels with batch size = 8, epoch = 8 and using YOLOv5s as the default model

## Output
1. can be found inside /content/runs/detect/
