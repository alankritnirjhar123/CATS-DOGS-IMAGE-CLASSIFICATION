# CATS-DOGS-IMAGE-CLASSIFICATION
Binary Image Classification using Custom Trained Top Layer Dense Model over Pretrained VGG16 CONVOLUTIONAL BLOCKS

# Binary Image Classification Model Using Neural Networks


# *AIM* - Objective is to classify images of dogs and cats using pre-trained Convolutional blocks of VGG16 Model trained on Imagenet Dataset on top of a Custom Trained Top Layer of Sequential Dense Layers




# Dataset:

The Dataset involved was downloaded from Kaggle Website with over 15000 images used for training dataset and 2000 images used for both validation and test datasets.



# Directory Structure:

Directory Structure is necesssary to maintain for using KerasImageDataGenerator to feed the model for fitting and training.
No Augmentation used as Augmentations would have to be saved to disk as separate files since this method of using VGG16 to train dense sequential model doesn't support augmentations on the fly/ augmentations while training the model.




# Steps Involved:

> Arrangement of Images in Directories with a structure consistent with KerasImageDataGenerator requirements.
> Load the Pretrained Convolutional Blocks of VGG16 from Keras Applications.
> Create a Model Architecture of comprising Sequential Dense Layers using Tensorflow and Keras.
> Training and Saving the Weights of the Custom trained TOP LAYERS with the output of Convolutional Blocks of VGG16 on train and validation Datasets
> Using the Trained Top Layer on top of the VGG16 CONVOLUTIONAL BLOCKS to make predictions on the unseen Test Dataset to evaluate the performance.




# MODEL PERFORMANCE:

The performance of the Model is decently good with F1 SCORE & ACCURACY on the test dataset predictions both over 92 PERCENT.




# Key Notes:

The model was very carefully and slowly trained since the outputs from CONVOLUTIONAL BLOCKS OF VGG16 made out top layer highly prone to overfitting the training dataset.
Very High Regularization (L2 - 0.05) with decaying Learning Rate Scheduler for optimizer ADAM had to be used to prevent the Model from overfitting the training dataset.
The VGG16 Convolutional Blocks take several minutes to produce outputs thus the output arrays needed to be saved onto a npy(numpy) file.
