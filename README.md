# Academic Performance Prediction System
# Based on data from Kerala Technical University (KTU) 
# Abstract
I was given a task of predicting the grades a student under KTU would get for final university exam for all subjects in a semester, using the marks and grades from previous semester that student studied. :sunglasses:
# Dataset
  Dataset used contained grade points of students studying in the civil enggineering department of PRS college.

*Total Number of students : 59 (after cleaning and preprocessing of data)*  (ik yeah it's too small!!! :cry:)

*Validation holdout contained 10% of whole dataset.* (damn... way too small. :sob:)

I am trying to get my hands on more data! :thumbsup:
# Network Architecture
I am using just 3 layer network with dropout layers sandwiched between,this small network was pretty good enough to perform in this dataset.The grades of students were converted to grade points according to KTU website and made the problem to a regression type rather than multi-class,multi-label classification.Now the predicted grade points can be converted back to grades for use. :sunglasses:

Dataset was converted and made the grades points between 0 and 1 and fed into the network.All the layers used the tanh activation function, dropout rate of 0.8 and loss function used was mean_squared_error

# Results
:relieved:
I was able to achieve a RMSE(Root Mean Squared Error) of 1.33 on validation set which is pretty good :satisfied: considering the fact we are predicting on a cross domain situation. **(subjects in input has no direct relation for subjects in output rather than both are from same branch of engg.)**
Training on more data will lead to more performance.

# Notes
**Trials and Failures**

1. Increasing layers and Neurons 
2. Using more complex RNN-LSTM ,RNN-GRU models ( had comparatively less performance and it was obvious it can't be considered sequence data)
3. Using Conv1D convolutions to get input encoded before passing to dense 

Tried these 3 major variations and it's variations but the performance didn't increase.