# Medical Image Generation Using Diffusion Model


 <div align="center">
    <a href="https://colab.research.google.com/github/reshalfahsi/medical-image-generation/blob/master/Medical_Image_Generation_Using_Diffusion_Model.ipynb"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="colab"></a>
    <br />
 </div>


Image synthesis on medical images can aid in generating more data for biomedical problems, which is hindered due to some legal and technical issues. Using the diffusion model, this problem can be solved. The diffusion model works by progressively adding noise, typically Gaussian, to an image until it is entirely undistinguishable from randomly generated pixels. Then, the noisy image is restored to its original appearance gradually. The forward process (noise addition) is guided by a noise scheduler, and the backward process (image restoration) is carried out by a U-Net model. In this project, the diffusion model is trained on the BloodMNIST dataset from the MedMNIST dataset.


## Experiment


To see the code under the hood, visit this [link](https://github.com/reshalfahsi/medical-image-generation/blob/master/Medical_Image_Generation_Using_Diffusion_Model.ipynb).


## Result

## Quantitative Result

Fréchet Inception Distance (FID) and Kernel Inception Distance (KID) are leveraged to quantitatively measure the performance of the diffusion model, which is presented below.

Evaluation metric | Score
------------ | -------------
FID |  5.039
KID | 4.141 ± 0.343


## Evaluation Metric Curve

<p align="center"> <img src="https://github.com/reshalfahsi/medical-image-generation/blob/master/assets/loss_curve.png" alt="loss_curve" > <br /> Loss of the model at the training stage. </p>
<p align="center"> <img src="https://github.com/reshalfahsi/medical-image-generation/blob/master/assets/fid_curve.png" alt="fid_curve" > <br /> FID on the training and validation sets. </p>
<p align="center"> <img src="https://github.com/reshalfahsi/medical-image-generation/blob/master/assets/kid_curve.png" alt="kid_curve" > <br /> KID on the training and validation sets. </p>


## Qualitative Result

Qualitatively, the generated images are shown in the following figure:

<p align="center"> <img src="https://github.com/reshalfahsi/medical-image-generation/blob/master/assets/qualitative_result.png" alt="qualitative_result" > <br /> Unconditional progressive generation on the BloodMNIST dataset (left) and a montage of the actual BloodMNIST dataset (right). </p>


## Credit

- [A Diffusion Model from Scratch in Pytorch](https://colab.research.google.com/drive/1sjy9odlSSy0RBVgMTgP7s99NXsqglsUL)
- [MedMNIST](https://medmnist.com/)
- [Denoising Diffusion Probabilistic Models](https://arxiv.org/pdf/2006.11239.pdf)
- [Diffusion Models Beat GANs on Image Synthesis](https://arxiv.org/pdf/2105.05233.pdf)
- [PyTorch Lightning](https://lightning.ai/docs/pytorch/latest/)
