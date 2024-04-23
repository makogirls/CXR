# X-ray Classification Model: Normal / Pneumonia / Covid-19 / Tuberculosis

This repository details the project for the 2023 Yonsei University Digital Healthcare Bootcamp (2023/07/26-2023/07/28).

## Introduction
Our project aims to differentiate between three diseases (Pneumonia, Covid-19, Tuberculosis) that present with similar symptoms but have distinct causes and therefore require different initial treatments and isolation methods. Rapid and accurate differentiation at early stages is crucial for patient management.

## Motivation
The motivation for selecting this topic stems from the importance of early differential diagnosis to dictate the correct initial treatment and isolation precautions, which vary significantly between these conditions.

## Dataset Introduction
We utilized publicly available X-ray datasets from Kaggle. Our data consists of:
- Tuberculosis: 1788 X-ray images
- Normal, Pneumonia, COVID-19: 2313 X-ray images each

The datasets can be found at the following Kaggle links:
- [Tuberculosis and Pneumonia Dataset](https://www.kaggle.com/datasets/roshanmaur/imbalanced-tuberculosis-and-pnuemonia-dataset?resource=download)
- [Covid19 Pneumonia Normal Chest XRay PA Dataset](https://www.kaggle.com/datasets/amanullahasraf/covid19-pneumonia-normal-chest-xray-pa-dataset)

## Preprocessing
Our preprocessing steps included class balancing, where each class was represented by 1788 images, and data augmentation techniques such as image rotation, zoom, shift, and horizontal flip to increase dataset diversity.

## Model Architecture
The model is a Convolutional Neural Network (CNN) with the following layers:
- Convolution layers with 32, 64, 128, and 256 filters
- Batch normalization and dropout for regularization
- Flatten layer followed by dense layers, with softmax function for the multi-class classification

## Changes and Improvements
- Modified the model from binary to multi-class classification using softmax activation function and categorical cross-entropy loss function
- Experimented with different optimizers (SGD, RMSprop, Adam)
- Applied data augmentation techniques for more robust training
- Tuned hyperparameters and employed early stopping to prevent overfitting

## Results
Our best model achieved a test accuracy of 83.4%. The model showed high sensitivity, indicating a strong ability to detect diseases from the X-ray images.

## Discussion
We discussed various strategies for improving accuracy, such as more convolutional layers or neurons, transfer learning, model ensembling, and improving the dataset.

## Reflections
We reflected on the challenges faced due to limitations in storage and computational resources, as well as the importance of medical knowledge in the development of such models. We also appreciated the significance of collaboration between developers and medical professionals.

## Roles and Responsibilities
Development & Presentation: Park Won-jun, Jeong Jae-won
Planning & PPT: Kang Min-gu, Kim Hyun-soo, Kim Han-jae, Baek In-sung

## References
- Scholarly articles and research papers related to X-ray image classification and CNN models.

## Figures References
- Links to image resources and documentation used for the development and presentation of the project.

## Acknowledgements
A special thanks to everyone who supported and guided us throughout the project, including those who provided valuable resources and data.
