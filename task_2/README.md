# Model Training Report

## Overview

This document outlines the results of training a U-Net-based model for semantic segmentation tasks. The training process, key metrics, and significant milestones are highlighted below.

## Key Results

* **Final Validation Loss**: `0.6369`
* **Best Validation IoU**: `0.3876`
* **SiBaTrAcc Final Value**: `0.8040`
* **Model Checkpoints**: Best weights saved at `/kaggle/working/weights_best.weights.h5`.

## Training Logs Summary

The training process spanned **19 epochs** out of a maximum of 50, with early stopping employed to prevent overfitting. Below are the key milestones from the training logs:

### Training Highlights

#### Epoch 1
* **IoU**: `0.0035`
* **Loss**: `1.1536`
* **Validation IoU**: `0.0014`
* **Validation Loss**: `1.0390`
* **Learning Rate**: `4e-4`
* **Best model weights saved**.

#### Epoch 6
* **IoU**: `0.2935`
* **Loss**: `0.7345`
* **Validation IoU**: `0.2014`
* **Validation Loss**: `0.8257`
* **Learning Rate**: `2e-4`
* **Best model weights saved**.

#### Epoch 8
* **IoU**: `0.3287`
* **Loss**: `0.6975`
* **Validation IoU**: `0.3493`
* **Validation Loss**: `0.6767`
* **Learning Rate**: `2e-4`
* **Best model weights saved**.

#### Epoch 14
* **IoU**: `0.3466`
* **Loss**: `0.6781`
* **Validation IoU**: `0.3876`
* **Validation Loss**: `0.6369`
* **Learning Rate**: `2e-4`
* **Best model weights saved**.

#### Final Epoch (Epoch 19)
* **IoU**: `0.3708`
* **Loss**: `0.6525`
* **Validation IoU**: `0.0053`
* **Validation Loss**: `1.0179`
* **Learning Rate**: `1e-4`

# Labels and Their Description

- **#LBL1**: Implementation of model validation on a part of the training dataset.  
  The `val_data` parameter in the `train` method is used to calculate the loss function and metrics on the validation set.

- **#LBL3**: Automatic model saving during training.  
  `ModelCheckpoint` is used to save model weights with the lowest loss function.

- **#LBL4**: Loading a model from a specific training iteration.  
  The `load_model` method loads the model weights from the file `weights_best.weights.h5`.

- **#LBL5**: Displaying various metrics during training.  
  During the training process, values for the loss function and the IoU metric are printed for each epoch.

- **#LBL6**: Plotting training graphs.  
  Graphs show the dependency of the loss function and metrics on the epoch number.

- **#LBL7**: Automatic testing on the test dataset.  
  The `test` method evaluates the model's performance on the test set using the SIBATRACC metric.

- **#LBL13**: Using BatchNormalization and Dropout to improve training and reduce overfitting.  
  These techniques are applied in the model's layers.

