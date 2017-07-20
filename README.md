# Rainforest image classification
This programme uses convolutional neural networks to classify different Amazon rainforest images, following the Kaggle competition

This folder contains 5 different programmes:

* rainforest_functions.py: 

    This folder contains different functions that will be called from the other programmes

* readimages.ipynb: 

    Converts the train images into DataFrames (one for each RGB color) and writes them in a .csv file. Due to lack of memory, the images have been resized, but this step is not needed.

* readimages_test.ipynb: 

    Converts the train images into DataFrames (one for each RGB color)

* rotateimages_RGB_separate.ipynb: 

    a) Reads all the initial train images stored as pixels into a .csv file from readimages.ipynb
    
    b) Calculates how many times a category appears and does not appear and stores this asymmetry
    
    c) The asymmetry between the time that it appears or does not appear decides how many times each image has to be rotated to have symmetric data. The programme rotates each image and stores the corresponding pixels as training data into separate .csv files for each category
    

* rainforest_tensorflow_CNN_Green_test.ipynb*: 

    a) Reads the initial (green) train data which has been stored as pixels into a .csv file from readimages.ipynb
    
    b) Reads the test data which has been stored as pixels in a .csv file in readimages_test.ipynb
    
    c) Reads the train data of the images which have been rotated and joins it with the initial train data
    
    d) Trains a tensorflow convolutional neural network for each category and calculates if the image corresponds to that category
    
    e) Writes the results into a DataFrame




*Note that there we are just taking the green color due to lack of computing memory.

The programme can be improved by:
    a) Not reducing the size of the images
    b) Rotating and resizing further images such that the training data becomes larger
    c) Creating a more complex neural network with further layers
    d) Using all of the colors to train the neural network
    e) Finding a better learning rate for each category
