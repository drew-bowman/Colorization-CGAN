# Colorization CGAN
A Conditional Generative Adversarial Network (CGAN) to colorize grayscale images.

This project was coded in Jupyter Notebooks using Python. More details about colorization theory,
implementation, tests, etc. can be found in [this undergraduate research thesis](https://drive.google.com/file/d/10PYoKT_YwOIlvwnCFpDo6Mz5gK7t0GaC/view?usp=sharing) completed at Elon University

## Goal
The aim of this project was to develop a model that could be trained on color images and then 
be used to colorize historical black and white images. Below is a table of several images taken by
William Henry Jackson in the 19th century which have been colorized by the places2 model.

|Image Name|Original|Colorized||Image Name|Original|Colorized|
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
|*Cameron's Cone*, 1879| ![](Images/Cameron's%20Cone%20orig.png) | ![](Images/Cameron's%20Cone%20color.png) ||*Cumbres Mountain*, 1880| ![](Images/Cumbres%20Mountain%20orig.png) | ![](Images/Cumbres%20Mountain%20color.png) |
|*Fremont's Peak*, 1878| ![](Images/Fremont's%20Peak%20orig.png) | ![](Images/Fremont's%20Peak%20color.png) ||*Georgetown*, 1873| ![](Images/Georgetown%20orig.png) | ![](Images/Georgetown%20color.png) |
|*Shadow Lake*, 1871| ![](Images/Shadow%20Lake%20orig.png) | ![](Images/Shadow%20Lake%20color.png) ||*Sierra San Juan*, 1874| ![](Images/Sierra%20San%20Juan%20orig.png) | ![](Images/Sierra%20San%20Juan%20color.png) |

## Code
### Training the CGAN
CGAN code can be found in [colorization_pix2pix.ipynb](colorization_pix2pix.ipynb).

Load a dataset to train, set training parameters, and let your computer fume for the next couple days. Below are a couple
features of the code.

As the model trains, it will output predictions on the training set after each epoch. This way, you can see the model converge (or fail spectacularly) in real time.
**TODO: Add picture here**

It will also output a loss curve after epoch.
**TODO: Add picture here**

Once the model's done training, it will output predictions on the test set.
**TODO: Add picture here**

### Testing the CGAN
Code to test an already-trained model can be found in [colorization_test_model.ipynb](colorization_test_model.ipynb).

Do you want to saved model and produce more predictions? This is the code for you!

This program allows you to save each prediction from a model individually ([colorization_pix2pix.ipynb](colorization_pix2pix.ipynb) saves them all in one figure). It is also able to randomly save ground truth
(original) images and colorizations from your test set, perfect for generating data for a user study to measure
the realism of your output. (Check out pg. 44 in [our paper](https://drive.google.com/file/d/10PYoKT_YwOIlvwnCFpDo6Mz5gK7t0GaC/view?usp=sharing) to see how students at Elon University faired at discriminating between the two)

Below are some randomly selected ground truths and colorized images. Can you tell which are which?
**TODO: Add images here**


### Various Helper Programs
This project required several programs to test features, generate artificial datasets, scale images to 256x256, etc.
All extraneous code can be found in the [Helper Programs](https://github.com/drew-bowman/Colorization/tree/master/Helper%20Programs) folder.


**Enjoy!**