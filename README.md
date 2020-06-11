# Image Denosing with Multi-column Dilated CNNs

In this project, we used deep CNN networks to denoise images, which are noised by guassian noise with noise level of sigma =30. Our network output is a residual image, so we get the clean image by subtracting input from output. We used a VGG like architecture with batch normalization and relu activation function. We trained three model, In first model regular 3*3 cnn filters is used. In our second model in order to increase the receptive filed, which is an important factor in image denoising task, we used dilated filters with dilation = 2. Finally, in third model we used multi column dilated cnn whith dilation = 1 and dilation =2 and then merged them. We compared the three models with 20 epoch runs and got a better results with multi-scaled dilated model.


We write the code in Denoiser.ipynb notebook using Pytorch library and run it in Google Colab with GPU. each model took almost 2hrs to train.

Dataset

Train and test data is in folder BSD300. Dataset used for the project is borrowed form Berkeley Segmentation Dataset and Benchmark(BSDS). We used a subsection of this dataset for our project. It contains two sub-directories: train and test, which consist of 200 and 100 images, respectively, of either size 321 * 481 or 481 * 321.

## Group Members: Saeed Karimi, Arda Türkoğlu, Görkem Yılmaz
