# Human-Activity-Recognition-with-Neural-Network
End to end project from collecting human activity data and building a neural network to classify activities

# Data Collection
Data collection is done through smartphones with the help of MATLAB application.
There is a section called 'sensors' in the application where all the sensors availabe on a smartphone can be switched on.
The record button can be pressed after selecting the sensor and each activity can be performed for the desired number of minutes.

It is not necessary to perform each activity in a single go. 
For example, if jumping is a chosen activity, it might be difficult to jump for 10 minutes without any breaks.
Everytime an activity is paused, the recording has to be stopped and saved with the desired filename. 
Once again, recording has to be started and the activity continued - this time saving as a new file. 
We will merge all the files during data processing step.

Public datasets for HAR (Human Activity Recognition) can be downloaded from the internet if one does not want to perform data collection on their own.
[Example:https://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones]

# Format change
MATLAB records the data in its own format (.mat files). 
These have to be convered into excel files so that they can be consumed by a python program and additional proceesing can be done on the data before feeding to a neural network.


# Data Exploration and Preparation
Once data is collected, the next step is to explore and visulaize the raw data to get an idea of what processing steps are required to be performed on the data.
