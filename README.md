# DCGAN in PyTorch

Generative Adverserial Networks are actually two networks in one, competing against eachother. The Discriminator a Convolutional Neural Network, whose job is to diffentiate between real and fake images. The Generator is Deconvolutional Neural Network, that will generate the actual images to feed to the discriminator in training (real images are also fed to discriminator at training time). It's crucial that these networks are mirror images of eachother.

And yes; I know this project is a mess right now but I plan on cleaning it up eventually... (story of my life).

I would also like to apologize to the 4 random people who cloned this repo in such bad shape.

# Results for CelebA
Since the network is mapping a vector of random numbers to a complete image we can easily interpolate between faces by interpolating between latent vector spaces.

![Inter](/imgs/inter.gif)

Generated celebrities
![Celeb](/imgs/Celeb.png)

A look at how these images are being generated by looking inside the generator. You can see the feature maps start off as just abstract features that slowly make their way to forming a face. By the last layer of the Generator you can start to see a face in some of the feature maps.

![Celeb1](/imgs/Celeb1.png)
![Celeb2](/imgs/Celeb2.png)
![Celeb3](/imgs/Celeb3.png)
![Celeb4](/imgs/Celeb4.png)

The final output
![Celeb5](/imgs/Celeb5.png)

# Interactive Board

![board](/imgs/board.gif)

# Results on MNIST dataset
Results after 2 epoch:

![GAN-Output](/imgs/GAN-Output.png)

And here's a look inside the Generator! Each picture contains each channel at a layer. The images start at 4x4 pixels and double in size until they are 64x64.

![GAN-Deconv1](/imgs/GAN-Deconv1.png)

![GAN-Deconv2](/imgs/GAN-Deconv2.png)

![GAN-Deconv3](/imgs/GAN-Deconv3.png)

![GAN-Deconv4](/imgs/GAN-Deconv4.png)

![GAN-Deconv5](/imgs/GAN-Deconv5.png)

# More Deep Learning

More to come soon! I'm currently working on progressively growing GAN's as described in this paper from NVIDIA: https://arxiv.org/abs/1710.10196

Also check out my school project which takes a very Natural Language Processing approach to bug detection: Deep Learning to Decet Logical Bugs in Software: https://github.com/MNaplesDevelopment/deep-learning-software-defects
