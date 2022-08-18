# Kmnist_AutoEncoder_Project
Autoencoders performance on KMNIST Classification Problem and the effect of ITL-regularization on unsupervised classification

We investigate the use of Autoencoders for reducing the dimensionality of KMNIST digits data set to improve classification performance. We compare the classification performance to the use of Convolutional Neural Networks (CNNs). We further introduce an information theory regularizer on the autoencoder. We force the autoencoder to learn latents on a 3d swiss roll prior and decode the images. Lastly, we introduce a Gaussian and a Gaussian Mixture Model Prior to investigate its effect on unsupervised clustering of the latent space. This work is presented as the final project for EEL6814 – Deep Learning Course.

## ESPCN Model
The Efficient Sub-Pixel Convolutional Neural Network (ESPCN) upscales the resolution at the end of the network. In ESPCN, the upscaling step is applied in the last layer. For this reason, the low-resolution image can be fed to the network unlike the SRCNN and FSRCNN. With this benefit, the ESPCN does not need to use the interpolation method. Moreover, the reduced input image size can make the model use a smaller kernel size that is used to extract features.

- Paper: [Real-Time Single Image and Video Super-Resolution Using an Efficient Sub-Pixel Convolutional Neural Network](https://arxiv.org/pdf/1609.05158.pdf)

## Results
![result](/data/Picture1.png)
Prediction on the high-resolution test image with sliced inference. – Left: without super-resolution, Right: with super-resolution.

- Table1: Results on DOTA-v1.0 validation set with Fast RCNN. – without sliced images inference.

| Validation | mAP | mAP_50 | mAP_75 | mAP_S | mAP_M | mAP_L |
| ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| 1X - Image | 15.7% | 26.3% | 15.6% | 2.8% | 12.4% | 30.1% |
| 2X - Image | 10.9% | 18.3% | 10.8% | 0.1% | 3.9% | 14.4% |

- Table2: Results on DOTA-v1.0 validation set with Fast RCNN. – with sliced images inference.

| Validation | mAP | mAP_50 | mAP_75 | mAP_S | mAP_M | mAP_L |
| ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- |
| 1X - Image | 26.9% | 45.4% | 27.1% | 8.2% | 27.1% | 39.8% |
| 2X - Image | 27.5% | 46.4% | 28.0% | 3.4% | 21.7% | 32.2% |

## Dataset
- Kuzushiji-MNIST is a drop-in replacement for the MNIST dataset (28x28 grayscale, 70,000 images), provided in the original MNIST format as well as a NumPy format. Since MNIST restricts us to 10 classes, we chose one character to represent each of the 10 rows of Hiragana when creating Kuzushiji-MNIST
- Paper: [Deep Learning for Classical Japanese Literature](https://arxiv.org/pdf/1812.01718.pdf)
- Data: [The KMNIST dataset](http://codh.rois.ac.jp/kmnist/index.html.en)
