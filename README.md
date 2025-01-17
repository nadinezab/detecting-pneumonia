# Detecting Pneumonia

<img src="/Images/xrayheader.png" alt="Chest x-ray images" >

*By Nadine Amersi-Belton*

## Problem statement

This project was completed in September 2020, during the worldwide COVID-19 pandemic. To help diagnose patients chest X-rays are examined. Machine learning presents an opportunity to expediate diagnosis and prevent human errors.

Due to insufficient data pertaining to COVID-19 patients, we have chosen to apply machine learning tools, in particular deep neural networks, to detect pneumonia in chest x-ray images.

## Components

* **Jupyter Notebook**

The [Jupyter Notebook](https://nbviewer.jupyter.org/github/nadinezab/detecting-pneumonia/blob/master/pneumonia-detection.ipynb) is our key deliverable and contains details of our approach and methodology, data preprocessing and exploration, deep learning models and results.

* **Presentation**

The [presentation](https://github.com/nadinezab/detecting-pneumonia/blob/master/presentation.pdf) gives a high-level overview of our approach, findings and recommendations for non-technical stakeholders. It is aimed to be between 5 and 10 minutes long.

* **Data**

The dataset was obtained from [Kaggle](https://www.kaggle.com/paultimothymooney/chest-xray-pneumonia). Due to the large file size, the data was not saved in this repository.


* **Blog Post**

A [blog post](https://medium.com/@nadinezab/the-importance-of-domain-knowledge-40d57ae0a91b?sk=f497c9c330990f784de5509ad1cc8460) on Medium was created as part of this project.

## Data exploration and preprocessing

The data consists of just over 5,000 images of chest x-rays of two classes, patients diagnosed with pneumonia and healthy/normal patients. We split the data into training, validation and test sets.

We noted that data is imbalanced, with 3 times more images of patients diagnosed with pneumonia.

<img src="/Images/distribution.png" alt="Distribution in training set" width = "500" >


## Results and recommendations

We applied the following models:
* basic neural network model
* convolution neural network
* convolution neural network with dropout layers
* more complex CNN model
* complex CNN model with L2 regularization
* VGG19 

The CNN model with dropout layers performed best on the validation set and was chosen as our final model. Its performance on the test set was as follows:
* accuracy of 0.78
* recall of 0.99
* F1 score of 0.85

The confusion matrix for the test set is as follows:

<img src="/Images/confmatrix.png" alt="Confusion matrix" width = "500">

With only 3 false negatives, our model has high recall and thus maximises patient safety.

Whilst we would prefer an overall higher accuracy, our focus is on recall as this metric is particularly important for patient safety and to minimize the legal risk.

We would recommend the following actions:
* gather additional data, this classification was undertaken on a small sample size of around 5k images and served as a proof of concept
* address class imbalance to seek to improve performance using say oversampling techniques
* use this tool to support medical professionals whilst it is further improved on

## Contact

* If you have any questions, you can contact me at nzamersi@gmail.com