# AUTOMATIC LICENSE PLATE DETECTION AND RECOGNITION

- DATASET:
  
  Took pictures from [Kaggle](https://www.kaggle.com/datasets/andrewmvd/car-plate-detection)
  
  Annotated it on [Roboflow](https://app.roboflow.com/)
  
  Stored in: ALPDR_data, [Kaggle](https://www.kaggle.com/datasets/sinha05/alpdr-dataset)

## STEP1: Detection
- Used YOLOv5 to train the dataset for 100 epochs.
- Metrics:
  
  ![image](https://github.com/user-attachments/assets/6e5a29a6-d4ea-4224-aaf8-419ee1ff7147)

- How to detect:
!python "\yolov5\detect.py" --weights "\model\last.pt" --img 640 --conf 0.10 --source <img-path> --save-crop

- Detection:
  
![image](https://github.com/user-attachments/assets/8927d8df-9776-4a33-acc3-03a920746fb7)


This is stored after cropping the license plate in the way:


![image](https://github.com/user-attachments/assets/ac39db58-eb97-4d7e-882a-7114897c9946)

