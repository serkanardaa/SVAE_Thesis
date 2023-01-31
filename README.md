# SVAE_Thesis

This repository contains the files that have been used SVAE training for the thesis project.

1-models folder contains codes for structure of SVAEs and their components such as encoder, decoder, and classifier.
2-utils folder contains loss_fn.py file that includes code regarding the calculation of different loss values.
3-custom_reg_dataset.py file is used for converting data to tensors to be used in dataloaders.
4-pytorchtools.py contains EarlyStopping class used for early stopping during the training.
5-training_methods.py contains 3 main functions that have been used throughout the training process.
  
  5 a)cv_fold_maker:Function for converting validation training data into folds. 
    Converted folds are later on prepared for using in dataloaders. 
    prepared dataloaders are going to be used in SVAE Training.
  
  5 b)hyperparameter_tuner:Function for hyperparameter tuning SVAE. By using dataloaders and validation folds generated by cv_fold_maker function,
    different settings are used and the loss value on validation fold is calculated.
   
  5 c)model_test:Function for testing a SVAE model with specific hyperparameter settings on provided test data. 
    In contrast to hyperparameter_tuner function, no cross validation is done in this function. Only 1 training is done with whole provided training data.
    Then the performance metrics are calculated on provided test data.
