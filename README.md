# ZERO-SHOT IMAGE RESTORATION USING DENOISING DIFFUSION NULL-SPACE MODEL

In this project we have reimplemented the zero shot image restoration using DDNM and its enhanced version DDNM+.

We have selected four main tasks: Colorization, Inpainting, Super Resolution and Old Photo Restoration, while Deblurring is performed directly by the enhanced version of the algorithm.

We have used two pretrained models: CelebA trained on celebrities images and ImageNet trained on a mixed subset of images (especially animals and plants).

We have also implemented and trained a simple UNet model, but for testing and evaluation we have used only the two pretrained ones to get better result, since our model is trained on a reduced dataset.

We have applied the two algoritghms DDNM and DDNM+ on 7 images of CelebA (using the correspondent model) and on 5 images of ImageNet. We have evaluated the results using three metrics: PSNR,SSIM and FID

Code and details are in the Python Notebook.

## Instructions to run

To execute the code you have to run cells in the Python Notebook.

First install librariers for the computation of the metrics, then define the functions to load the images and transform them to a tensor (sections: "Libraries to install" and "Load the original image").
Run the sections: "Implementation of the the matrix A and its pseudoinverse", "DDNM" (definne the function of the DDNM algorithm), "DDNM+" (definne the function of the DDNM+ algorithm) and "Evaluation metrics" (define the function to perform the metrics).

Then there are two section: one is for "CelebA" and the other one is for "ImageNet", now you can run one after the other (if you want interleave them you have to redifine the model executing the cell in which the pretrained model is loaded).

By running the last two sections you can perform all the task defined above on the choosen image for CelebA and on the one chosen for ImageNet (in the ImageNet section there is implemented at the end also the mask shift trick). 
The images used by default are "NNProject/images_for_evaluation/woman3.png" for CelebA and NNProject/images_for_evaluation/squirrel.png" for ImageNet, but you can use also the other images we used for the evaluation by just changing the path passed to the function "load_image" at the beginning of the section "CelebA" or "ImageNet".

If you want to try also our simple model, run the section "Our simple model".
