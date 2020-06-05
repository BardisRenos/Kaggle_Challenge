# Kaggle_Challenge

This repo demonstrates a Kaggle challenge ragarding cancer prostate [link](https://www.kaggle.com/c/prostate-cancer-grade-assessment). In this challenge has purpose to predict each patient the grade of the cancer. In order to achieved that, I created a transfer learning model by using ResNet50. However, image pre-processing is needed first, before "feeding" the neural network. 



### Data set

The data set is constructed through 10.616 images which each image corrensponds to a single patient. The images are in .TIFF format, which contains three different images with different sizes into one image file. Each image belongs to ISUP grade. That grade demonstrates the cancer grade. 

<p align="center"> 
<img src="https://github.com/BardisRenos/Kaggle_Challenge/blob/master/img.JPG" width="450" height="250" style=centerme>
</p>

### Data process 

This block shows how should the images be processed. Each image is in **.TIFF** format which consists 3 different dimension images of the same pantient. In order to process the images to work with a deep learning model, it is necessary to retrieve the median image out the 3 ones. Another worth mentioning is that to split each image into small tiles and converting them into **.jpg**. Namely, each cancer image is splited into many more small pieces which are focussed mainly on the cancer part. After creating N number of tiles there is a need to exclude the images that are below of a dimension threshold. The remaining tiles are reshaped into same dimension. 

### Choosing Deep Learing Model

To train the images I choose a pre trained model. That has prove that produce high percentage of accuracy. Therefore ResNet50 is that I choose. 
