---
title: "Morphing Diffusion models"
excerpt: "Diffusion models for digits generation   <br/><img src='/images/CT_image.png'>"
collection: portfolio
---

Diffusion models are machine learning algorithms which generate medias (usually images) through progressively adding noise to a dataset (forward process) then learning the denoising (backward) process. Traditionally, Gaussian noise is used. However, in the [Cold Diffusion paper](https://arxiv.org/abs/2208.09392), the authors showed that identical levels of success can be achieved with arbitrary noise types (not necessarily limited to Gaussian noise). 

In this investigation, I experimented with generating digits in the convention of the MNIST dataset, using different types of diffusion models. First, I experimented with changing the noise type: instead of using Gaussian noise, images from another dataset were used as `noise' instead. Under such scheme, the original image would gradually be morphed into an image from another dataset at the end of the forward process. Mathematically, the forward process is as follows:

$$\mathbf{z_{t}} = \sqrt{\alpha_{t}} \mathbf{x} + \sqrt{1 - \alpha_{t}} \mathbf{z}$$

where $\mathbf{z}$ is a randomly sampled image from the morphing dataset and $\mathbf{x}$ is an image from the original dataset. 

Additionally, I have also experimented with changing the network architecture as well as noise schedulers, which resulted in different qualities in generated images.