# Classifying books genre to technical and non-technical on the basis of their book covers

This Classifier tries to categorize books into either technical or non-technical
on the basis of the book cover. The model has been trained using a imagenet
pretrained model with a Resnet-34 architecture.

Freezing the pretrained layers and training only the last layer resulted in an
accuracy of 78%.

Unfreezing the pretrained layers and finetuning all the layers using differential
learning rates resulted in an accuracy of 84%.

Following transformation functions are applied for data augmentation:
1. Zooming
2. Lighting
3. Warping

Below are the sample training images with categories


![Sample Training Images](https://github.com/anubhavmaity/BookCoverClassifier/blob/master/readme_images/snap.png)


After validating the model on the validation set, below is the confusion matrix <br/>


![Confusion Matrix](https://github.com/anubhavmaity/BookCoverClassifier/blob/master/readme_images/confusion_matrix_book_cover.png)

The images and models are been kept in the data/book_cover.

# Installation

pip install fastai==1.0.45
