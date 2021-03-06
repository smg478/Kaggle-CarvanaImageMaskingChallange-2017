## Kaggle Carvana Image Masking Challenge 2017 solution on keras

This repository contains the keras solution files of the challenge.
Results produced from this architecture scored 0.9967 in the private leaderboard of the competition. 

The solution is based on [Peter's](https://github.com/petrosgk/Kaggle-Carvana-Image-Masking-Challenge) starter code with keras. I thank him for his clean work! Usage of the code is mostly similar to his one. However, the main contribution of this work is a modified version of the u-net.

The file 'u_net_models.py' contains definitions of one basic and two modified u-nets. 

## Features of modified u-net

Resudual blocks and inception blocks

Skip connections

High resolution training

You can experiment with your own idea also!


## Requirements

Keras 2.0 w/ TF backend
sklearn
cv2
tqdm
h5py

## Usage

### Data

Place 'train', 'train_masks' and 'test' data folders in the 'input' folder.

Convert training masks to .png format. You can do this with:

mogrify -format png *.gif

in the 'train_masks' data folder.

### Train

Run python train.py to train the model. 

### Test and submit

Run python test_submit_multithreaded.py to make predictions on test data and generate submission.

Run python test_submit_ensemble.py to make weighted average ensemble from submission files.

### Tools

'tools' folder contains some useful codes for fast experiment and result analysis.


