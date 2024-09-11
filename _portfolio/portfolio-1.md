---
title: "Learned Primal Dual Reconstruction for CT imaging"
excerpt: "Master's thesis investigating deep learning models for image reconstruction in Computed Tomography   1<br/><img src='/images/CT_image.png'>"
collection: portfolio
---

Computed Tomoraphy (CT) is one of the most commonly used medical imaging techniques. It involves using emission of X-rays to infer the internal structures of patients, which can then be used to detect abnormalities and thus lead to more accurate diagnosis. Normally,
to ensure high quality of reconstructions, intensities of emitted X-rays need to be high, otherwise noisy artefacts will emerge in the reconstructions. However, X-rays are known to have cancer inducing effects, making extensive exposure to them undesirable. Therefore, current active research areas revolve around using machine learning approaches to obtain good quality reconstructions whilst maintaining amount of dosage low.

In this project, I worked with Image Analysis group in Department of Applied Mathematics on reproducing and extending the results from the paper "[Learned Primal Dual (LPD) Algorithm](https://arxiv.org/abs/1707.06474)", which blends ideas from convex optimisation and modern machine learning to reconstruct images for Computed Tomography.

During the investigation, I developed code repository that implements the proposed architecture and trained the networks on University's supercomputer (CSD3). Performances of trained models were benchmarked against traditional methods used for image reconstruction in Computed Tomography, such as Filtered Backprojection, Total Variation Regularisation, U-Net postprocessing. Docker containerisation was used to ensure consistency across different operating systems. 

On top of implementing the models mentioned in the original paper, I also experimented with two additional models: the Total-Variation Learned Primal Dual model (TV-LPD) and the Continuous Learned Primal Dual model (cLPD). The former incorporates additional regularisation on top of the original LPD algorithm, whilst the latter replaces the convolution blocks in the original network with neural ODEs [Continuous Learned Primal Dual](https://arxiv.org/abs/2405.02478).
