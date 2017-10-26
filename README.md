# Directional Self-Attention Network
* This repo is the code of paper *DiSAN: Directional Self-Attention Network for RNN/CNN-free Language Understanding*, <http://>
* This is python based codes implementation under tensorflow 1.2 frameword for Directionnal Self-Attention Network (DiSAN)
* The leaderboard of Stanford Natural Language Inference is available [here](https://nlp.stanford.edu/projects/snli/)
* Please contact [xxx] for questions and suggestions

## Overall Requirements
* Python3 (verified on 3.5.2, or Anaconda3 4.2.0) 
* tensorflow>=1.2

#### Python Packages:

* numpy


-------
### This repo includes three part as follows:
1. Directionnal Self-Attention Network independent file -> file disan.py
2. DiSAN implementation for Stanford Natural Language Inference -> dir SNLI_disan
3. DiSAN implementation for Stanford Sentiment Classification -> dir SST_disan

__The Usage of *disan.py* will be introduced below, and as for the implementation of SNLI and SST, please enter corresponding folder for further introduction.__

-------
## Usage of disan.py

### Parameters:

* param **rep\_tensor**: 3D tensorflow dense float tensor [batch\_size, max\_len, dim]
* param **rep\_mask**: 2D tensorflow bool tensor as mask for rep\_tensor, [batch\_size, max\_len]
* param **scope**: tensorflow variable scope
* param **keep\_prob**: float, dropout keep probability
* param **is\_train**: tensorflow bool scalar
* param **wd**: if wd>0, add related tensor to tf collectoion "weight_decay" for further l2 decay
* param **activation**: disan activation function [elu|relu|selu]
* param **tensor\_dict**: a dict to record disan internal attention result (insignificance)
* param **name**: record name suffix (insignificance)

### Output:
2D tensorflow dense float tensor, which shape is [batch\_size, dim] as the encoding result for each sentence.

------
## Acknowledgements
* Some basic neural networks are copied from [Minjoon's Repo](https://github.com/allenai/bi-att-flow), including RNN cell, dropout-able dynamic RNN etc.

