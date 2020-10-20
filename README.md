# Fingerprint_Indoor_Localization_Tensor_GAN
  
  This repository contains the Python and MATLAB codes for the paper **Real-time indoor localization for smartphones using tensor-generative adversarial nets. IEEE Transactions on Neural Networks and Learning Systems**, 2020, by X.-Y. Liu and X. Wang. [https://ieeexplore.ieee.org/document/9159909]
  

# Datasets: 

1. A 20 m × 80 m floor (located in a research institute building). 

There are in total 30 randomly deployed APs;  fingerprints are sampled at grid size: 0.3m x 0.3m.

On the fourthe floor, it can receive 21 APs, and an orginal 63 x 268 x 21 tensor was collected.

We preprocess it into a fingerprint tensor: 64 x 256 x 21 (copied the 63th row to a 64th row; deleted the 257th to 268th columns).

2. We also include a synthetic fingerprint dataset of size: 476 x 598 x 15, used in a previous project: **Adaptive sampling of RF fingerprints for fine-grained indoor localization. IEEE Transactions on Mobile Computing, 2016. By X.-Y. Liu, S. Aeron, V. Aggarwal, X. Wang, M.-Y. Wu.**

# MATLAB codes for kNN and Direct Neural Networks

  We used MATLAB for kNN and Direct neural networks
 
1. kNN_performance implements the kNN algorithm
    
   Test_kNN_Plot.m tested the localization performance and dras CDF curve of localization error.

2. Direct neural networks (it split the data into training set and testing set, we also include the data in the MATLAB folder).
   
   It is a regressor, and we used the matlab deep learning toolbox with GUI, at link: https://www.mathworks.com/products/deep-learning.html
   
   The file RF_regression_net.m is saved from this toolbox, for a reference.


# Python Codes for GAN (regressor and discriminator)
> tensorflow 1.8.0
> python 3.5.3
> numpy 1.14.2
> pillow 5.0.0
> pickle 0.7.4

A code for the original GAN.py with a generator and a discriminator, tested at link: https://github.com/hust512/Tensor-GAN

A code for a TGAN.py with a regressor and a discriminator.
