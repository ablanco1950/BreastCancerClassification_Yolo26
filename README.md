# BreastCancerClassification_Yolo26
Classification of breast cancer (among 2 classes: 0 No cancer, 1 Cancer  ) using the file  https://zenodo.org/records/10519652  dataset breastmnist_128.npz and the Yolo26 model.

 
INSTALLATION:

For training download from:

https://huggingface.co/Ultralytics/YOLO26/blob/main/yolo26n-cls.pt

The pretrained classifier model yolo26n-cls.pt


All packages, if any are missing, can be installed with a simple pip in case the programs indicate their absence in the environment.

If not yet installed, this packages are:

pip install numpy

pip install pandas

pip install keras

pip install tensorflow

pip install opencv-python

pip install ultralytics

pip install scikit-learn

Download all the files that accompany this project in a single folder.

Download  from https://zenodo.org/records/10519652  the  dataset breastmnist_128.npz  and put in the project folder. 

Create and fill the structure that needs yolo26 , executing:

python CreateTrain.py

python CreateVal.py

python CreateTest.py


EVALUATION

python Evaluate_BreastCancer_Yolo26.py

The model displays a list of images whose classes were correctly predicted and those that were not,   resulting in an accuracy of  = 93.98496240601504% (hit predictions / (hit predictions + error predictions)).

It also produces the confusion matrix and the classification report. Images with a prediction confidence level below 0.9, 23 images, are not considered and appear in the CancerImagesRejected.txt file.

   precision    recall  f1-score   support

           0       0.88      0.81      0.85        27

           1       0.95      0.97      0.96       106

    accuracy                           0.94       133

   macro avg 0.92      0.89     0.90       133

weighted avg 0.94      0.94      0.94      133


Confusion Matrix (raw values):
 [[ 22   5]
 [  3 103]]

Only images with a confidence level greater than 0.9 are considered,

Images that do not have a confidence level exceeding 0.9(according to the model), 23 images, are referenced in BreastImagesRejected.txt for manual inspection.
            
   

    
  
![Fig1](https://github.com/ablanco1950/BreastCancerClassification_Yolo26/blob/main/ConfusionMatrix.png)
  

TRAINING

The best.pt model was obtained through training

python Train_BreastCancer_Yolo26.py.

The LogTraining50epoch.docx file, containing the 50-epoch log of the training process, is also included.

REFERENCES:

https://zenodo.org/records/10519652

https://huggingface.co/Ultralytics/YOLO26/blob/main/yolo26n-cls.pt

https://github.com/ablanco1950/SkinLessionClassification_Yolo26

https://github.com/ablanco1950/SkinLesionDetection_Resnet_Pytorch

https://umeshk1255.medium.com/breast-cancer-detection-using-ai-understanding-convolutional-neural-networks-168d91f5cafc


Citation


Jiancheng Yang, Rui Shi, Donglai Wei, Zequan Liu, Lin Zhao, Bilian Ke, Hanspeter Pfister, & Bingbing Ni. (2024). [MedMNIST+] 18x Standardized Datasets for 2D and 3D Biomedical Image Classification with Multiple Size Options: 28 (MNIST-Like), 64, 128, and 224 (3.0) [Data set]. Zenodo. https://doi.org/10.5281/zenodo.10519652
Style
APA
