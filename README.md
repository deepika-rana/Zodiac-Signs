# Zodiac-Signs

In this notebook, I trained a CNN to classify images from the Chinese Zodiac Signs Kaggle database. 
#### Import Datasets
Since the data already hosted in Kaggle, directly added the data.

Load in the training and test data, split the training data into a training and validation set, then create Data Loaders for each of these sets of data. I perform some simple data augmentation by randomly flipping and rotating the given image data. Did this by defining a torchvision transform. This type of data augmentation should add some positional variety to these images, so that when training a model on this data, it will be robust in the face of geometric changes (i.e. it will recognize a ship, no matter which direction it is facing).

Network Architecture used is **ResNet 152**.

The following layers were implemented.
#### LINEAR -> ReLU -> Dropout -> Linear -> ReLU -> Linear -> LogSoftmax
Train the Network
Number of epochs used to train the model is 20. Further load the Model with the Lowest Validation Loss and test the Trained Network.
