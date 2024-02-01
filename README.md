# Determining-Authenticity-of-Images

## Introduction
In this modern era where Artificial intelligence and machine learning are continuously evolving,
AI-generated images have caught the attention of many artists and art lovers alike. With the
capability of AI to generate almost authentic images under different visual settings, its use-case in
animations and art is increasing daily. Like other tools, AI Image Generators are also facing
backlash because of their ability to falsify information and create doubt among people over the
authenticity of images shared within the community.
We propose using machine learning techniques to address this challenge and distinguish between
AI-generated and authentic images. By harnessing machine learning, we aim to develop a solution
that can differentiate between real and AI-generated images, providing a valuable tool to address
concerns related to image authenticity.

## Dataset
An extensive survey of datasets from platforms such as Kaggle, PaperswithCode, and Hugging
Face was conducted to facilitate the training of our classification models. After careful
consideration, the CiFAKE Dataset was identified as the most suitable for our problem.
This dataset comprises two primary classes, Real and Fake, subdivided into ten additional
classes. This subdivision enhances the distinctiveness of features within the dataset, ensuring
that our model is well-equipped to classify images beyond the training data. The real images
in the dataset are derived from the Cifar 10 dataset, while the corresponding fake images are
generated using stable diffusion 1.4.

## Results
### SVM Classification
The SVM model was trained on 20000 data points and tested on a test dataset containing 5000
images divided between fake and real images.
The model could accurately classify 4050 images out of 5000 images, with an accuracy score
of 81%. Furthermore, the model achieved an accuracy of 90.4% on the training data.
### Multi-Layer Perceptron
MLP Model Trained on Standardized Pixel Values (`mlp_clf2`) –
The model achieved an accuracy of approximately 79.05% on the test set. The confusion matrix
revealed 7964 true negatives, 2036 false positives, 2155 false negatives, and 7845 true
positives.
MLP Model Trained on Normalized Pixel Values (`mlp_clf3`)-
The normalized model achieved an accuracy of approximately 74.75% on the test set. The
confusion matrix showed 7837 true negatives, 2163 false positives, 2888 false negatives, and
7112 true positives.
### K-Means Clustering
The normalized test set was used to predict the cluster assignments, and an evaluation was
made. Confusion Matrix and Accuracy Score were two of the evaluation parameters used to
test the goodness of the fit of the model.
The best accuracy we got using the K-Means Algorithm was around 59%.
### Gaussian Mixture Model
The Gaussian Mixture Model was trained on 30000 images of each class from the Training
dataset and tested on 20000 images of each class from the Training dataset.
The model could accurately classify 25,549 images out of 40000 with an accuracy score of
63.87%.
### Logistic Regression
The Logistic Regression model was trained on 20000 images of each class and tested on a test
dataset containing 5000 images of each class.
The model could accurately classify 6724 images out of 10000, with an accuracy score of
67.24%.

## Inferences
The AI-generated images, although highly similar to real images, contain some features that are distinct
from actual ones and can be exploited to detect them.
Linear classifiers like logistic regression generate better results than unsupervised clustering models,
showcasing that clustering methods can't capture the distinct features between real and images and
classify them accurately.
The Elbow Method utilized in K-means couldn’t capture the fake and real images and suggested four
optimal clusters, suggesting the drawbacks of unsupervised learning models for image classification.
Although the accuracy in K-Means Clustering was low, it is to be expected since the main problem
statement does not lend itself to a clustering solution but rather a classification-type approach, and so
even with other clustering algorithms like GMM, we could only achieve an accuracy of up to around
63%.
