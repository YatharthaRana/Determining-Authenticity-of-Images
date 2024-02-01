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
