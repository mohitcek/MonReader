# Image Classification Model

This project develops a machine learning model for classification tasks in the field of computer vision. I am focusing on detecting a page flip from low-resolution images captured from the mobile. This repository contains two jupyter notebook scripts, that train a three-layer CNN model on the low-resolution images of a book from the mobile. The trained model extracts the relevant features and patterns from the low-resolution image and classifies them as 'flip' and 'not flip'.

The two notebooks differ only in the data processing step, `CNN_model_with_data_augmentation.ipynb` implements data augmentation to create a robust model and increase model performance. Both models perform well on the training and testing datasets. Finally, Gradient-weighted Class Activation Mapping (Grad-CAM) is implemented on the output of the final convolutional layer in the network, which examines the gradient information flowing into the final layer.

Here, is an example of a low-resolution image along with the prediction probability and prediction from the CNN model.

![PredictionExample](https://github.com/mohitcek/MonReader/blob/main/figures/Prediction%20Example.png)

The confusion matrix based on the performance of both models is as follows:

![ConfusionMatrix](https://github.com/mohitcek/MonReader/blob/main/figures/CM.png)

Observe that the model without Data Augmentation performs better on the training as well as testing dataset. The following patterns are observed based on the results from Grad-CAM.
- CNN Model (without data augmentation)
  1. The model focuses on the nail of the person's hand and the book's edges.
  2. It is observed that the model classified an image as page flip (value "0") if it can find a book's edge and no fingernails on the right side.
 
- CNN model (with data augmentation)
  1. The model focuses on the edge of the person's finger/hand. Generally, the side of the hand is visible during page flip.
  2. It is observed that the model classified an image as page flip (value "0") if the final layer can detect a large enough area of the hand facing up.

 Here, are a few examples from both models to support the above statements.

1. CNN Model (without data augmentation)
 ![Case0Example1](https://github.com/mohitcek/MonReader/blob/main/figures/Case0_example1.png)
 ![Case0Example2](https://github.com/mohitcek/MonReader/blob/main/figures/Case0_example2.png)
 ![Case0Example3](https://github.com/mohitcek/MonReader/blob/main/figures/Case0_example3.png)

2. CNN Model (with data augmentation)
 ![Case1Example1](https://github.com/mohitcek/MonReader/blob/main/figures/Case1_example1.png)
 ![Case1Example2](https://github.com/mohitcek/MonReader/blob/main/figures/Case1_example2.png)
 ![Case1Example3](https://github.com/mohitcek/MonReader/blob/main/figures/case1_example3.png)
 ![Case1Example4](https://github.com/mohitcek/MonReader/blob/main/figures/case1_example4.png)
