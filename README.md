# Image Restoration Using CSNet



>Image restoration focuses on improving degraded images to produce high-quality images. CSNet is a framework for image restoration introduced in this paper that uses channel and spatial hybrid frequency modulation approaches. There are different methods for image restoration like Traditional methods which struggle with differing degradation patterns across feature channels, resulting in less effective restoration. CSNet framework addresses this issue by adding a frequency-based channel feature modulation module that uses Fourier transforms to improve channel interactions in addition to that a multi-scale spatial feature modulation module is introduced to refine the directcurrent component by using lightweight learnable parameters within a coarse-to-fine framework for improved multiscale representation learning. A frequency-inspired loss function improves omni-frequency learning, allowing CSNet to achieve advanced results in image restoration tasks. Validated tasks such as image
dehazing, defocus deblurring, and desnowing demonstrate the model’s effectiveness.

[DataSets used ](https://www.kaggle.com/datasets/balraj98/synthetic-objective-testing-set-sots-reside/data)

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
## Training and Evaluation
Please refer to respective directories.

|Task|Dataset|PSNR|SSIM|
|----|------|-----|----|
|**Motion Deblurring**|GoPro|33.29|0.963|
||HIDE|31.05|0.941|
||RSBlur|34.31|0.872|
||RealBlur-R|35.84|0.952|
|**Image Dehazing**|SOTS-Indoor|42.45|0.997|
||SOTS-Outdoor|40.40|0.997|
||Dense-Haze|17.13|0.65|
||NH-HAZE|20.55|0.81|
||NHR|26.30|0.976|
||Haze4K|34.12|0.99|
|**Image Desnowing**|CSD|38.37|0.99|
||SRRS|32.33|0.98|
||Snow100K|33.76|0.95|
|**Image Deraining**|Average|33.51|0.916|
|**Defocus Deblurring**|DPDD<sub>*single*</sub>|26.22|0.811|

|Task Dataset PSNR↑ SSIM↑|
|Image Dehazing SOTS 41.79 | 0.996|
|Image Dehazing Dense-Haze 17.2 | 0.650|
|Night time Dehazing NHR 26.54 | 0.986|
|Image Desnowing Snow 100K 33.77 | 0.950|
|Underwater Image Dehazing HICRD 31.23 | 0.950|


