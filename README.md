# Dog_Breed_Classifier--Udacity_Deep_Learning-Nanodegree
This repository includes the work done for the second project of the Udacity's Deep Learning nanodegree

In this project I built a model that is able to identify whether a person or a dog appears in the picture and then either classify the dog according to its breed, or if a person is identified, find the dog breed that best resembles the person!

Links for both the dog and the faces dataset can be found within the notebook.

Initially, a model is constructed from scracth and trained on the dog images dataset. The training is kept within reasonable timeframes of about 3-4 hours. This, along with the relative simplicity of the model, is the reason we eventually reach a low accuracy of only 12%.
The model is a straightforward Convolutional Neural Network. It consists of 6 convolutional layers divided in two blocks of 3, separated by a maxpooling layer. As an output, there are two fully connected linear layers. The model receives as input a 224x224 pixels color images. For the training, we use the technique of data augmentation in which we basically create random cropped or rotated images drawn from the dataset. 

A higher accuracy is achieved with the technique of transfer learning, in which we basically modify the last layers (classification layer) of a pretrained model. In this project I used the VGG-16 pretrained model and replaced the last layer with a layer applicable to this problem. Specifically I replaced the 1000 output nodes with only 133 (as many as the different dog breeds under consideration).
