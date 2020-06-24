# Image-Inpainting
Globally and locally consistent image completion

![title images](https://user-images.githubusercontent.com/59387983/85526497-07517900-b645-11ea-932f-4d98d1f32c0a.PNG)


# Architecture
![Architecture](https://user-images.githubusercontent.com/59387983/85526508-091b3c80-b645-11ea-974a-cb6b9afbf769.PNG)


# patch-based approach
the patch-based approaches [Barnes et al. 2009, 2010; Darabi et al. 2012; Huang et al. 2014; Wexler et al. 2007] show high quality reconstructions for arbitrary image sizes and masks; however, they are unable to provide novel image fragments not found elsewhere in the image nor have a high level semantic understanding of the image: they only local at similarity on a local patch level.
# cnn-based approach
CNN-based image inpainting approaches were limited to very small and thin masks [Köhler et al. 2014; Ren et al. 2015; Xie et al. 2012]. Similar approaches have also beenappliedtoMRIandPETimagesforcompletingmissingdata[Li et al. 2014]. More recently, and concurrently to this work, Yang et al. [2017] also proposed a CNN based optimization approach for inpainting.
# context encoder
the context encoder-based approach [Pathak et al. 2016] can generate novel objects, but are limited to fixed low resolution images. Furthermore, the approach can lack local consistency as the continuity of the completed region with the surrounding area is not taken into account.
# GAN-based approach
 CNN-based inpainting to large masks, and proposed a context encoder to learn features by inpainting, based on Generative Adversarial Networks (GAN) [Goodfellow et al. 2014]. The original purpose of GAN is to train generative models using convolutional neural networks. These generator networks are trained by using an auxiliary network, called discriminator, which serves to distinguish whether an image is generated by a network or is real. The generator network is trained to fool the discriminator network, while the discriminator network is updated in parallel. By
using a Mean Squared Error (MSE) loss in combination with a GAN loss, Pathak et al. [2016] were able to train an inpainting network to complete a 64 × 64 pixel area in the center of 128 × 128 pixel images, avoiding the blurring common with using only MSE losses. We extend their work to handle arbitrary resolutions by using a fully convolutional network, and significantly improve the visual quality by employing both a global and local discriminator. 
