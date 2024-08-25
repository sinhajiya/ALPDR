# AUTOMATIC LICENSE PLATE DETECTION AND RECOGNITION

KAGGLE NOTEBOOK: (https://www.kaggle.com/code/sinha05/alpdr)

- DATASET:
  
  Took pictures from [Kaggle](https://www.kaggle.com/datasets/andrewmvd/car-plate-detection)
  
  Annotated it on [Roboflow](https://app.roboflow.com/)
  
  Stored in: ALPDR_data, [Kaggle](https://www.kaggle.com/datasets/sinha05/alpdr-dataset)

## STEP1: Detection
- Used YOLOv5 to train the dataset for 100 epochs.
- Metrics:

  ![image](https://github.com/user-attachments/assets/6e5a29a6-d4ea-4224-aaf8-419ee1ff7147)

- How to detect:
!python "\yolov5\detect.py" --weights "\model\last.pt" --img 640 --conf 0.10 --source [img-path] --save-crop

   ![image](https://github.com/user-attachments/assets/c0cf842e-4ded-4364-bd15-5c9686e96eef)


- MODEL:
   The best model after 100 epochs is stored on [Kaggle](https://www.kaggle.com/models/sinha05/alpdr_yolov5_model)

## STEP2: PreProcessing
- Convert RGB to HSV

   ![image](https://github.com/user-attachments/assets/4127e47a-1fc4-4cef-82df-b09b5f6207fa)

- GrayScale Extraction

    ![image](https://github.com/user-attachments/assets/5f2d8902-aae0-4938-8a04-d357b4ca979d)

 - Morphological Transformation
   
    ![image](https://github.com/user-attachments/assets/13cca17f-6495-46b6-aae2-5d4a165676c5)

- Gaussian Smoothing for noise reduction
  
    ![image](https://github.com/user-attachments/assets/fc16e460-f7fd-40db-a5a1-378828717c56)

  ## STEP3: Text Recognition

  For OCR, pytesseract is used.
  
     ![image](https://github.com/user-attachments/assets/e14dd977-751c-49cc-9e3e-353427834f2e)


