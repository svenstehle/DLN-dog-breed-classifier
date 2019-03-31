# # Dog breed classifier app from Udacity Deep Learning Nanodegree
Cloned from Udacity. Took first steps towards developing an algorithm that could be used as part of a mobile or web app. Written code will accept any user-supplied image as input. If a dog is detected in the image, it will provide an estimate of the dog's breed. If a human is detected, it will provide an estimate of the dog breed that is most resembling. 
See introduction sections in `dog_app.ipynb` for more details.

### Problem statement:
Piecing together a series of models to perform different tasks: for instance, the algorithm that detects humans in an image will be different from the CNN that infers dog breed. 

### Install and use:
* Clone repo
* Setup virtual environment
* Follow `dog_app.ipynb`
* Import Datasets as described in `dog_app.ipynb` etc.
* Change relevant system paths to your local paths, e.g: `"/data/dog_images/*/*/*"` needs to be changed to point to the correct location of images on your system
* If you want to use more images from a public database, download and add them to the training folder

### Approach:
* Write function to detect human faces in images using OpenCV
* Write function to detect if dogs are present in images. Used pretrained VGG16
* Created CNN from scratch with PyTorch to classify the (resembling) dog breed
* Compared with a CNN created with transfer learning (based on VGG16) to classify dog breeds. Replaced last fc layer in VGG16, all other layers' weights frozen
* Write a function that returns detected dog breed from images with our transfer-learning-VGG16
* Put it all together and write a function that accepts any image and determines whether the image contains a human, dog or neither. Then it outputs the (resembling) dog breed - we have created a first version of our _dog breed classifier app_!
* Test it on our own sample images 

### Possible improvements:
* Continue on the task of writing another face detection algorithm and test performance of that
* Test performance of another pre-trained network for dog-detection in images
* Test performance of unfreezing one additional or more layers in our pretrained transfer learning VGG16 
* Add more dog images to train our own CNN on

### Thoughts and lessons learned:
* CNNs
* PyTorch and relevant modules
* Employing pretrained models
* Image augmentation and dataloaders
* Fine tuning a pretrained model for our problem
* Dog breed classification using our own CNN from scratch is pretty difficult and takes a very long time to train. Transfer learning helps a lot here! 
