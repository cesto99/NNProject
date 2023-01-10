# ZERO-SHOT IMAGE RESTORATION USING DENOISING DIFFUSION NULL-SPACE MODEL

In this project we have reimplemented the zero shot image restoration using DDNM and its enhanced version DDNM+.

We have selected four main tasks: Colorization, Inpainting, Super Resolution and Old Photo Restoration, while Deblurring is performed directly by the enhanced version of the algorithm.

We have used two pretrained models: CelebA trained on celebrities images and ImageNet trained on a mixed subset of images (especially animals and plants).

We have also implemented and trained a simple UNet model, but for testing and evaluation we have used only the two pretrained ones to get better result, since our model is trained on a reduced dataset.

We have applied the two algoritghms DDNM and DDNM+ on 7 images of CelebA (using the correspondent model) and on 5 images of ImageNet. We have evaluated the results using three metrics: PSNR,SSIM and FID

Code and details are in the Python Notebook.

## Instructions to run

To execute the code you have to run cells in the Python Notebook.

First install librariers for the computation of the metrics, then define the functions to load and transform to a tensor the images.
Run the sections about the implementation of the the matrix A and its pseudoinverse, the implementation of the two algorithms DDNM and DDNM and functions of evaluation metrics.

Then there are two section: one is for CelebA and the other is for ImageNet, now you can run one after the other (if you want interlap them you have to redifine the model executing the cell in which the pretrained model is loaded).
