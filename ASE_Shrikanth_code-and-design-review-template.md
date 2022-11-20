# Render Image Denoiser

## Abstract

Many of the 3D rendering engines for example Arnold which use raytracing methods to render 3D graphics confront the issue of noises in the final rendered images. These noises are generated as result of low sample values used on the light rays from the 3D lights. Increasing the sample values, however, will lead to longer render times. Rendered Image denoiser is a type of Artificial Intelligence algorithm which aims to reduce noise in the computer-generated images after they are rendered. The goal is to obtain cleaner images using lower sample values which in turn will enable artists to deliver their product much faster.

## Detailed Description

Computer-generated content plays a vital role in bringing life and realism to visual medias such as movies, commercials and video games. 3-dimensional images have undergone various improvements from their earliest stages in terms of quality and efficiency. This also improved the realism in the 3D images. It can be said that most of the realism was achieved through implementation of algorithms which brought in real world like features inside the 3D lighting environment. One of those features is called raytracing. Raytracing involves emitting thousands of light rays on a 3D model which then reflects, refracts or scatters with the model depending upon its material property. Computational calculation of these rays bouncing takes a lot of time depending upon the hardware being used. The number of rays being emitted and its behaviour after interacting with a 3D object or scene is decided by sample values Many of the 3D rendering engines for example Arnold which use raytracing methods to render 3D graphics confront the issue of noises in the rendered images. These noises are generated as result of low sample values used on the light rays from the 3D lights. Increasing the sample values, however, will lead to longer render times. Rendered Image denoiser is a type of Artificial Intelligence algorithm which aims to reduce noise in the computer-generated images after they are rendered. The goal is to obtain cleaner images without increasing the sample values.

 <img src="https://github.com/ShrikanthX/AIM_ASE_project_Shrikanth/blob/main/Noise_sample_comparison.png" width="500"><p>
    <em>Figure 1 : Samples per pixel comparison of noise in render images[1] (Joss Whittle 2012) </em>
</p>

### Datasets

The datasets which will be used for this model will be from Public Domain and Creative commons 3D artwork available on the internet. The 3D content creation software Maya by Autodesk will used to render images of these 3D models with the help of rendering engine Arnold. These datasets will be split into training and testing sets. Ground truth image will be created by rendering just enough samples for an image so that there is no visible noise. The input noisy renders will be created by dividing the total number of samples used in ground truth image by 20 and re-rendering.

### Arcitecture Proposal

The approach which will be followed for this model is Monte Carlo denoising. This is based on supervised machine learning framework where the model will be pre-trained with noisy and clean image pairs and then applied to the actual noisy image to be rendered.[2]

## References

[1] Joss Whittle, 2012. Dissertation Update: Path Tracing in action - l2program.co.uk - 1355621166.png [image]. Available from: http://l2program.co.uk/wp-content/uploads/2013/06/1355621166.png [Accessed 18 November 2022].

[2] Gwangju Institute of Science and Technology, September 2022, available at https://techxplore.com/news/2022-09-method-denoising-images.html (Accessed on 17 November 2022)



