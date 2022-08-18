# Kmnist_AutoEncoder_Project
Autoencoders performance on KMNIST Classification Problem and the effect of ITL-regularization on unsupervised classification

We investigate the use of Autoencoders for reducing the dimensionality of KMNIST digits data set to improve classification performance. We compare the classification performance to the use of Convolutional Neural Networks (CNNs). We further introduce an information theory regularizer on the autoencoder. We force the autoencoder to learn latents on a 3d swiss roll prior and decode the images. Lastly, we introduce a Gaussian and a Gaussian Mixture Model Prior to investigate its effect on unsupervised clustering of the latent space. This work is presented as the final project for EEL6814 – Deep Learning Course.

## Results
We enforce the model to maximize the entropy of the latent code distribution which helps in spreading out the latent while at the same time minimizing the cross-entropy between the latent code and the prior distributions which makes latent codes fit the prior distribution better.

- Swiss Roll

![img1](/data/Picture1.png)

- Gaussian

![img2](/data/Picture2.png)


![img3](/data/Picture3.png)

Samples from a linear walk over the swiss-roll. Right to left is going along the linear direction of the manifold. Top to bottom is going along the rotating direction of the manifold.

## Dataset
- Kuzushiji-MNIST is a drop-in replacement for the MNIST dataset (28x28 grayscale, 70,000 images), provided in the original MNIST format as well as a NumPy format. Since MNIST restricts us to 10 classes, we chose one character to represent each of the 10 rows of Hiragana when creating Kuzushiji-MNIST
- Paper: [Deep Learning for Classical Japanese Literature](https://arxiv.org/pdf/1812.01718.pdf)
- Data: [The KMNIST dataset](http://codh.rois.ac.jp/kmnist/index.html.en)
