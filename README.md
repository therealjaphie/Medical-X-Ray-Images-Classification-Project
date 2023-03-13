# Evaluating Various ML Algorithms on Image Classification of Medical X-Rays
## by Josephine Ochai


## Dataset

The dataset used for this project was acquired from three sources online. It contains 11,210 x-ray images distributed amongst four datasets for four body parts - chest, elbow, shoulder and wrist.
Details of each dataset is provided below:

* **Chest:** The chest dataset consists of 3583 images obtained from [Kaggle's Chest X-Ray Image Repository](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia). The samples are mixed i.e both 'normal' and 'pneumonia' samples are used.

* **Elbow & Shoulder:** The elbow and shoulder dataset consist of 3000 and 2073 images respectively, both obtained from [Kaggle's Finger X-Ray Image Repository](https://www.kaggle.com/alexandersuh/finger-xray). This repository contains over 70,000 images in total of several body parts including, but not limited to finger, wrist, elbow, shoulder etc. Thus, both datasets were easily obtained from this repository.

* **Wrist:** The wrist dataset consists of 2554 images. A part of this dataset was obtained from [Mendeleys's Wrist Fracture X-Rays](https://data.mendeley.com/datasets/xbdsnzr8ct/1). The other part was obtained from the [Finger X-ray Images](https://www.kaggle.com/alexandersuh/finger-xray) discussed earlier.



## Summary of Process

Before building my models, all images are preprocessed to ensure they are of equal size and that they are all rendered in greyscale form.
Additionally, feature extraction is performed on the images and data stored as a numpy array. Each image class of the dataset is also visualised. Next, a stratified data split with 30% test size is carried out on both the original and features extracted dataset.

In the first experiment, convolutional neural networks (CNN) is used for image classification of the original dataset and in the second, image augmentation is implemented to the train set before classifying with a CNN model again.

the next set of experiments focuses on the features extracted data and makes use of a random forest model for classification after which the features' train set is balanced using the Synthetic Minority Oversampling Technique (SMOTE) to reduce bias, and then the random forest model is run again.

These four experiments are evaluated using the precision, recall and f1-score metrics and confusion matrices are also plotted for better illustration. The results of the experiments are documented.

