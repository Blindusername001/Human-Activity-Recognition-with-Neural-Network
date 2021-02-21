Ever wondered how your smartphone/smartwatch identifies the activity you are doing. It knows when you walk, run or climb stairs. That is what is called HAR (Human Activity Recognition) in the scientific world.

This project was taken as part of one of the module assignments in my Data Science Masters course.

We will build a neural network that can identify three activities we do using data recorded by mobile sensors.




# Human-Activity-Recognition-with-Neural-Network
End to end project from collecting human activity data and building a neural network to classify activities

#Steps involved in creating a Neural Netowrk predictive model:
1. Data collection
2. Detrmine if the problem at hand is a regreeion or classificaiton problem
3. Data exploration and pre-processing
4. Split data into testing, validation and training datasets
5. Split each dataset into input(X) and output(y) - convert them into numpy arrays
6. Develop a simple NN sequential model 
7. Tune hyperparameters (using a modeule like GridSearchCV)
8. Compile and Fit the tunes model with training and validation datasets
9. Predict the testing data with the model
10. Depending on the problem (regression/ classification) compute performance metrics


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
The code for this is [https://github.com/karthikkumar001/Human-Activity-Recognition-with-Neural-Network/blob/main/Sensor_timetable_to_excel_files.txt]


# Data Exploration and Preparation
Once data is collected, the next step is to explore and visulaize the raw data to get an idea of what processing steps are required to be performed on the data.
The jupyter notebook for this along with the visualizations are in [https://github.com/karthikkumar001/Human-Activity-Recognition-with-Neural-Network/blob/main/Data%20preparation%20and%20exploration.ipynb]

# Neural Network Modelling
Human Activity Recognition is a multiclass classification problem.
We create a simple ANN (Artificial Neural Network) and then optimizing the hyperparameters to improve the model.
We use Keras for neural network modelling and GridSearchCV for hyperparameter tuning.
The jupyter notebook for this is in [https://github.com/karthikkumar001/Human-Activity-Recognition-with-Neural-Network/blob/main/ANN-Model.ipynb]
