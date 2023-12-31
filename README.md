# NeRF
### NeRF: Neural Radiance Fields Implementation in PyTorch
[![Open Tiny-NeRF in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shreyasr-upenn/NeRF/blob/main/NeRF.ipynb)<br>

[NeRF](https://www.matthewtancik.com/nerf) (Neural Radiance Fields) is a method for synthesizing photo-realistic images of complex 3D scenes by modeling the volumetric scene as a continuous 3D function. Here is an animation generated by this repository:


<img src=data/motion2.gif height="300" width="300" >


## Results

![enter image description here](https://github.com/shreyasr-upenn/NeRF/blob/main/data/nerf_results.png)


Iteration 3000  Loss: 0.0035  PSNR: 24.52  Time: 1.00 secs per iter,  51.94 mins in total


Generated image (left), target image (middle) and PSNR vs. iterations graph spanning over 3000 iterations. The model is able to reach 25 PSNR (Peak Signal to Noise Ratio) after 3000 iterations, and is able to perfectly learn the parameters of the 3D model.
## Method


[NeRF: Representing Scenes as Neural Radiance Fields for View Synthesis](http://tancik.com/nerf)  
 [Ben Mildenhall](https://people.eecs.berkeley.edu/~bmild/)\*<sup>1</sup>,
 [Pratul P. Srinivasan](https://people.eecs.berkeley.edu/~pratul/)\*<sup>1</sup>,
 [Matthew Tancik](http://tancik.com/)\*<sup>1</sup>,
 [Jonathan T. Barron](http://jonbarron.info/)<sup>2</sup>,
 [Ravi Ramamoorthi](http://cseweb.ucsd.edu/~ravir/)<sup>3</sup>,
 [Ren Ng](https://www2.eecs.berkeley.edu/Faculty/Homepages/yirenng.html)<sup>1</sup> <br>
 <sup>1</sup>UC Berkeley, <sup>2</sup>Google Research, <sup>3</sup>UC San Diego  
  \*denotes equal contribution  
in ECCV 2020 (Oral Presentation, Best Paper Honorable Mention)

> A neural radiance field is a simple fully connected network (weights are ~5MB) trained to reproduce input views of a single scene using a rendering loss. The network directly maps from spatial location and viewing direction (5D input) to color and opacity (4D output), acting as the "volume" so we can use volume rendering to differentiably render new views
