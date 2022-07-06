# Bone-Fracture
## Abstract 
Disabilities in human bone can be identified by medical image. Radiologist scans the bone of human and prints the medical image. They prepare the reports based on the medical image. This takes much time to complete the whole process. In order to avoid this, an automated abnormality detection system using medical images is been proposed. This work mainly focuses on fracture detection. It takes data as input and digitalizes the images by scanning. The pre-processing techniques are performed on medical images and the data is divided into two datasets that is trained dataset and test dataset. Later edge detection, feature extraction and classification are performed. Finally, this work is tested with test dataset and accuracy of the work is calculated.
## Problem Statement
The Radiologist spend much time in identifying fracture in bone and write the report. Some system gives less accuracy and some systems give more accuracy but contains  below 50 images in their dataset. This project predicts the given image has fracture or not by considering feature extraction values and also shows the high accuracy.
## Proposed System
Bone fracture is commonly occurred when much force is applied than required. Sometimes it may be critical when bone is broken in different places. Minor fractures cannot be identified easily. Radiologist analysis the medical image and conclude whether the bone is fractured or not. This takes much time and also cause pressure for the radiologist. In order to detect the bone fracture automatically this system is proposed.
The medical images here we consider is X-ray images of hands and leg of human bone and detect the fractures present in them. Images contain noise that may occurred due to fingerprints or while image extraction or some other. The noise while extraction is called as salt and pepper noise. For removal of this noise median filter is applied.
The median filter preserves the edges and remove the noise. After applying median filter Sobel edge detection technique is used. It is a image gradient operator. The Sobel edge detects the edges in both horizontal and vertical directions. The gradient magnitude is calculated for detected edges and produce the edge detected image.
The edge detected image is used for feature extraction. Gray level Co-occurrence matrix is used for feature extraction of the digitalized images. It maps between the pixel brightness of image. Entropy, energy, contrast, correlation, asm, homogeneity, area, perimeter is measured for extracting features. As GLCM is second order derivate of statics it helps to find information of each pixel.
SVM classifier is the binary classifier and is one class classifier. It performs binary classification and regression estimation task, minimizes the error and provide effectiveness in classification so it is very efficient to use. Here the classification is supervised and has two data set one is training dataset and other is test dataset. Training dataset train the support vector machine for the classification and the test dataset test the classification accuracy. In this approach two data set is used to classify the biomedical processed image into fractured and un-fractured.
## Implementation
### Dataset
The dataset ratio percentage for train, validation, and test were 70, 30 % respectively.

Kaggle: https://www.kaggle.com/datasets

Radiopaedia: https://radiopaedia.org/
### Technologies
For detection process software used is jupyter and programming language is python 3.8.1v and windows 10 is used.
### Training Method
We first given the dataset consisting of fractured and non- fractured images. The Preprocessing step is performed i.e., conversion of image to gray scale. The Sobel edge detection is used to detect the edges of image in horizontal and vertical direction. The gradient of images is calculated and obtained as a single image.
The GLCM feature extraction is used to extract the texture features of the image. These features are contrast, correlation, energy, entropy, asm. These values are stored in the database and labelled with their train name. The data is divided with 70% train data and 30% test data. By using contour function the extreme points of bones are identified. By using the angles as condition, the given image is predicted whether it is hand or leg.
### Model Evaluation
The model was evaluated by calculating the mean Average Precision, mean Average Recall and F1-score metrics. The metric is calculated on the taken dataset. The procedure to calculate the accuracy of the object detection metric varied based on the dataset. The accuracy obtained is around 92%.
## Conclusion
For detecting the fracture automatically this project is been developed so that it will be helpful for the report generation. We summarize the following points:

● The model performance, of the proposed system using the SVM classifier on available
dataset, was 92% accuracy.

● The helps the radiologist by giving the value as fractured or not.

● The accuracy of the proposed system was low due to:
- Outliers detection
- Some Minor fractures are not identified
## Future Enhancement
The proposed method detects the fracture easily. In future the different types of fractures should be identified. We would like to increase the size of the dataset, and types of diseases to use the same model in the medical environment.
