**Abstract**

Breast cancer is one prominent kind of cancer among different cancers that had a significant
share of contribution to the deaths of individuals, especially women. Early identification and
diagnosis of breast cancer has become quintessential in addressing the problem. One of the cost
effective and efficient screening techniques that has been widely adopted is Mammography.
Some of the challenges in diagnosis of breast cancer using mammography screening are
incorrect interpretations by radiologists and false negatives during screening. Conventional
machine learning models had limitations like feature extraction requiring manual intervention
and inoperable on raw images. This research project is aimed at minimizing the above-mentioned
shortcomings and enhance the performance and efficiency of breast cancer detection using Deep
Learning pipeline. The proposed pipeline is constructed from Convolutional Neural Network
(CNN) models with different training approaches performed on the Mammography Image
Analysis Society (MIAS) mammogram image dataset. Preprocessing, augmentation, and
segmentation are performed on the raw images before providing to three CNN models to perform
feature extraction and classification of images into normal, malignant, and benign. Modified
CNN model is trained from scratch while AlexNet and Residual Network-50 (ResNet-50) are
based on transfer learning. The proposed models are evaluated for performance and accuracy
based on confusion matrix and Area Under the Receiver Operating Characteristic Curve (AUCROC),
which determined ResNet-50 to be more accurate and efficient with 98.6% accuracy, 97%
precision, 100% recall and 99% F1-Score.

**Data Flow:**

Mammographic Image data downloaded from MIAS Database.

 MIAS Dataset is uploaded to Amazon S3.

 MIAS Dataset is shared from Amazon S3 to Amazon SageMaker for Data Augmentation.

 Data Augmentation results are then stored in Amazon S3 bucket in a data_augmentation
folder.

 The augmented data is then processed for Image Segmentation.

 The segmented data is then stored in Amazon S3 bucket in data_segmentation folder.

 Segmented data is further used to build, train, validate and deploy the models.
