
# Galactic Deep Vision

IMPORTANT NOTE: I could not fit the original full dataset on github, so I provided a smaller but still viable train/test set for functionality. Highly reccomend using SDSS image library via SQL querying if you would like to attempt similar tests at higher sizes.

GDV is a deep learning project based on the subject of galaxy morphology, which is a field of astronomy. This entails categorizing galaxies into Hubble-TF classes.

A key difference in our project is that we use real categories accepted by astronomers, namely (Lenticular, Spiral, Barred-Sprial, and Elliptical), rather than arbitrary shapes such as "round", "foggy", or "cigar-shaped".

The model achieves exceptional results, with 98.2% on 3-Way and 93.17% on 4-Way categorization.
 
## Code Summary

GDV is a simple project that aims to effectively categorize galaxies into hubble-tuning-fork categories. 

The program code first takes in data and applies preprocessing techniques to make notable features of galaxy images easier for the model to interpret, before feeding it into the model.

You can also print example images of each category to see the result of preprocessing.

This is then run through a pretrained model of ResNet-34 that utilizes learning rate scheduling, early stopping, and model saving to get the best result.

After training, you can print graph results of accuracy and loss.

Once your training run is finished, you can test the model accuracy on an unseen set of data, on multiple runs that can be determined by the user.

Once all testing runs finish, the program will print out the best run, and its confusion matrix, along with a report on all notable datapoints.

This can also be printed onto seaborn heatmaps and report.

## Running the Code

Setting up the ipynb file is fairly simple, make sure to use correct libraries with installs on your terminal.

It is also reccomended to run this program in **anaconda Jupyter notebook** for ease of use.

Depending on where you have your dataset located, make sure to change the directories in each dataset block to where you have unzipped it.

## Requirements

* PyTorch Library **2.3.0**
* Seaborn **0.13.2** (Using this version prevents problems with certain values not appearing.)
* Numpy **1.24.3**
* OPTIONAL: CUDA **12.1** (This is not necessary as you can use your CPU, but if your workstation has a higher-tier 30-40 series GPU, this greatly improves speed of the program.)

This was run with anaconda, but can be run with other methods, the install statements can be found on PyTorch's website:

https://pytorch.org/



