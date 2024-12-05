# Image Restoration Using CSNet


>Image restoration focuses on improving degraded images to produce high-quality images. CSNet is a framework for image restoration introduced in this paper that uses channel and spatial hybrid frequency modulation approaches. There are different methods for image restoration like Traditional methods which struggle with differing degradation patterns across feature channels, resulting in less effective restoration. CSNet framework addresses this issue by adding a frequency-based channel feature modulation module that uses Fourier transforms to improve channel interactions in addition to that a multi-scale spatial feature modulation module is introduced to refine the directcurrent component by using lightweight learnable parameters within a coarse-to-fine framework for improved multiscale representation learning. A frequency-inspired loss function improves omni-frequency learning, allowing CSNet to achieve advanced results in image restoration tasks. Validated tasks such as image
dehazing, defocus deblurring, and desnowing demonstrate the model’s effectiveness.


## DataSets Used For Image Restoration

Image Dehazing:
[SOTS,](https://www.kaggle.com/datasets/balraj98/synthetic-objective-testing-set-sots-reside/data)
[Dense-Haze,](https://www.kaggle.com/datasets/rajat95gupta/hazing-images-dataset-cvpr-2019)
[NHR](https://wuminye.github.io/NHR/datasets.html#downloads)

Defocus deblurring:
[DPDD](https://github.com/Abdullah-Abuolaim/defocus-deblurring-dual-pixel/blob/master/README.md)

Image Desnowing:
[Snow 100K](https://github.com/c-yn/CSNet/tree/main/Desnowing)

Underwater Image Restoration:
[HICRD](https://data.csiro.au/collection/csiro:49488)

## Installation
The project is built with PyTorch 3.8, PyTorch 1.8.1. CUDA 10.2, cuDNN 7.6.5 
For installing, follow these instructions:
~~~
conda install pytorch=1.8.1 torchvision=0.9.1 -c pytorch
pip install tensorboard einops scikit-image pytorch_msssim opencv-python
~~~
Install warmup scheduler:
~~~
cd pytorch-gradual-warmup-lr/
python setup.py install
cd ..
~~~
## Training and Evaluation Results

|Task|Dataset|PSNR|SSIM|
|----|------|-----|----|
|**Image Dehazing**|SOTS|41.79|0.996|
||Dense-Haze|17.2|0.650|
||NHR|26.54|0.986|
|**Defocus Deblurring**|DPDD<sub></sub>|29.35|0.883|
|**Image Desnowing**|Snow100K|33.77|0.950|
|**Underwater Image Dehazing**|HICRD<sub></sub>|31.23|0.950|



