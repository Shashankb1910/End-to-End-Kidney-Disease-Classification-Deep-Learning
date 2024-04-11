# End-to-End-Kidney-Tumor-Classification-using-Mlflow-and-DVC

### This project employs deep learning techniques to classify kidney tumors using MRI scans. Utilizing TensorFlow with a VGG16 model and Softmax activation, it achieves accurate tumor identification. Integrated with MLflow and DVC for experiment tracking and data versioning, the project also features a Flask web application hosted on AWS EC2. The CI/CD pipeline ensures seamless deployment and updates, making it a comprehensive solution for medical image classification.

instead of using train test split using keras data generator in stage 03 model_training

set MLFLOW_TRACKING_URI=https://dagshub.com/sbadgujar1019/End-to-End-Kidney-Disease-Classification-Deep-Learning.mlflow 

set MLFLOW_TRACKING_USERNAME=sbadgujar1019 

set MLFLOW_TRACKING_PASSWORD=91890639fe54392cfa4cb37af3418b58b08c67a6


MLFLOW_TRACKING_URI=https://dagshub.com/sbadgujar1019/End-to-End-Kidney-Disease-Classification-Deep-Learning.mlflow 
MLFLOW_TRACKING_USERNAME=sbadgujar1019 
MLFLOW_TRACKING_PASSWORD=91890639fe54392cfa4cb37af3418b58b08c67a6 
python script.py


curl -H "Authorization: Bearer 1cb123f74a6adc388c6a471e0778afb35197e8a7" "https://api.dagshub.com/sbadgujar1019/End-to-End-Kidney-Disease-Classification-Deep-Learning.mlflow"


AWS - 848477405825.dkr.ecr.eu-north-1.amazonaws.com/kidney
