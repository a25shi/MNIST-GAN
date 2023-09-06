# MNIST-GAN
A Generative Adversarial Network (GAN) consists of two neural networks, the Generator and the Discriminator, that are trained together in a competitive setup. The goal of the Generator is to produce artificial images that resemble real ones, while the Discriminator tries to distinguish between real and fake images. Training continues in this adversarial manner until the Generator produces images that are indistinguishable from real images, at least from the perspective of the Discriminator.

In this specific implementation, the GAN is built using the deep learning framework PyTorch and is based off of the DCGAN network laid out in the paper "Unsupervised Representation Learning with Deep Convolutional Generative Adversarial Networks". It is trained on the MNIST dataset, a collection of handwritten digit images.

The result of training on this dataset is a Generator network that can produce high-quality images of handwritten digits that weren't originally part of the MNIST dataset but look as if they could have been.

# Issues with GAN

A common issue with with GANs is called mode collapse, when the generator discovers a particular output (or a small set of outputs) that is consistently deemed "realistic" by the discriminator, and then it excessively produces only that output. This problem is mitigated in our network by using batch norm layers, as well as the LeakyReLU activation function to promote healthy gradient flow.

# Sample of training images:

<img src="https://github.com/a25shi/MNIST-GAN/assets/64557388/0fa50bd4-4fdc-452b-bd90-34666abeadca" width="400" height="400"/>


# Sample of final generated images:

<img src="https://github.com/a25shi/MNIST-GAN/assets/64557388/44111be0-657d-4912-9182-5b8b59c8d4f8" width="400" height="400"/>

# Loss Graph
![Untitled](https://github.com/a25shi/MNIST-GAN/assets/64557388/9877a4cc-f593-4b6a-9c5f-3a86558bc2cc)


