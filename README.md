# CNN based model for Melonoma Detection
> This project is a part of the course "Convolutional Neural Networks in TensorFlow" by Upgrad. The project is about building a CNN based model for Melonoma Detection.
>
> To build a CNN based model which can accurately detect melanoma. Melanoma is a type of cancer that can be deadly if not detected early. It accounts for 75% of skin cancer deaths. A solution that can evaluate images and alert dermatologists about the presence of melanoma has the potential to reduce a lot of manual effort needed in diagnosis.


## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Observation](#observation)
* [Conclusions](#conclusions)

## General Information
- The dataset consists of images of skin lesions, and the goal is to classify the images into nine classes: pigmented benign keratosis, melanoma, basal cell carcinoma, nevus, squamous cell carcinoma, vascular lesion, actinic keratosis, dermatofibroma, and seborrheic keratosis.
- The dataset consists of 2357 images of malignant and benign oncological diseases, which were formed from the International Skin Imaging Collaboration (ISIC). All images were sorted according to the classification taken with ISIC, and all subsets were divided into the same number of images, with the exception of melanomas and moles, whose images are slightly dominant.
- The dataset consists of 9 classes of skin cancer. The dataset is divided into 80% training and 20% testing.

## Technologies Used
- tensorflow - 2.16.1
- keras - 3.4.0
- seaborn - 0.11.1
- matplotlib - 3.3.4
- pandas - 1.2.4

## Observation
- We have chosen 3 convolutional layers with 16, 32 and 64 filters respectively. We have used 2 dense layers with 128 and 9 neurons respectively.
- We have used 'relu' activation function for all the layers except the output layer where we have used 'softmax' activation function.
- We have used 'adam' optimizer and 'sparse_categorical_crossentropy' loss function.
- We have used 'accuracy' as the metric to evaluate the model.
- We have built 3 model version one with the basic image dataset, second with the augmented image dataset and third with the augmented image dataset and dropout layers.
- The model with the augmented image dataset and dropout layers has the highest accuracy of 0.93 and validation accuracy of 0.83.
- We have noticed there is a class imbalance in the dataset. The class 'seborrheic keratosis' has the least number of images.
- We have used 'ImageDataGenerator' to augment the images. We have used rotation, width shift, height shift, shear, zoom, horizontal flip and vertical flip to augment the images.

## Conclusions
- Finally, we could handle both overfitting and class imbalance issue and the model performance has increased considerably.
- **Train accuracy 93% and Validation accuracy 82%**