# my-cv-project

## Overview

In this project, I use a YOLOv4 model with 2 detection heads (tiny-yolo) and 20 anchor boxes to detect 3 types of parking signs/classes: EV, Accessible, and Charger. The labeled dataset has been obtained from MathWorks.

## Required Files

The codebase consists of 3 files: 
1. AnalyzingLabeledData.mlx
2. ModelTraining.mlx
3. ModelEvaluation.mlx

## How the Code Works

In AnalyzingLabeledData.mlx, I perform analysis on the dataset by analyzing the area and aspect ratio of the bounding boxes, creating box plots of both classes and investigating any outliers, using helper functions.

In ModelTraining.mlx, I create datastores of the train data, estimate the number of anchor boxes (since YOLOv4 requires them), and perform test-train split on the dataset (80-20 split). After analysis of the anchor boxes vs Mean IoU plot, 20 anchor boxes are chosen for the model and the model is trained with Learning Rate = 0.001 and Max Epochs = 50, among other hyperparameters. 


## Credits
