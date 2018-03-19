# tfClassifier - Simple model retraining
## Image Classifier Retraining
1. Clone this repo
* Create a folder to hold your new classification options. This will be the file path referenced in step 7
```
$ mkdir ~/tom_classifier
```
* Add an images folder in the directory created in step 2
```
$ cd tom_classifier
// In the tom_classifier directory
$ mkdir images
```
* Set up folders of images to retrain on with each new classification as the folder name inside the images folder. (e.g. - For the "Tom Classifier", the folders  would be named "Tom Hanks", "Tom Cruise", and "Tom Brady", etc..)
```
// In the tom_classifier/images directory
$ mkdir Tom\ Hanks
$ mkdir Tom\ Cruise
$ mkdir Tom\ Brady
```
* Gather images for each classification (I think 200 is the minimum) and put them in the appropriate folder created in step 3
* Follow instructions to [get into a Python environment for Tensorflow](https://www.tensorflow.org/versions/r1.3/install/install_mac)
* In Terminal, navigate to the `image_classification` folder in the repo
```
// After cloning the repo
$ (tensorflow) cd tfClassifier
$ (tensorflow) cd image_classification
```
* Copy and paste the following script into your Terminal, remembering to replace the occurances of "YOUR_FILE_PATH" with the file path to the directory that contains the folder which holds the classification folders you created in step 2 (e.g. - `~/tom_classifier/`)
```
$ python retrain.py --model_dir ./inception --image_dir YOUR_FILE_PATH/images --output_graph YOUR_FILE_PATH/output.pb --output_labels YOUR_FILE_PATH/labels.txt --how_many_training_steps 500
```
* Hit `Enter` begin retraining the model
* Once the model has been retrained, open the `retrain_model_classifier.py` file and enter the file path created in step 2
* Choose an image that was not included in the training and running it through your newly trained model
```
$ python retrain_model_classifier.py PATH_OF_IMAGE_TO_BE_CLASSIFIED
```

For more information check out the information below.

### tfClassifier -- Original Documentation

This repository contains code to:
1) setup the tensorflow imagenet classifier which is capable of identifying 1000 objects.
2) setup a retraining script that takes in your own images and trains a new mdoel that you can use.
3) Using tensorflow to build a text classification system.

setting up tensorflow classifier and retraining it

find the tutorials here:
1) https://sourcedexter.com/quickly-setup-tensorflow-image-recognition/
2) https://sourcedexter.com/retrain-tensorflow-inception-model/
3) https://sourcedexter.com/tensorflow-text-classification
