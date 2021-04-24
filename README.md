# D2Net

Code for this paper [An LED Detection and Recognition Method Based on Deep Learning in Vehicle Optical Camera Communication]

XU SUN,  QING CHENG


## Training

#### Command

```python train.py```

This configuration file is core/config.py



## Testing

To test on a single image,

```python predict.py IMAGE_NAME.jpg```

By default, the name of the pretrained model used by Predictor is 'best_fpn.h5'. One can change it in the code ('weights_path' argument). It assumes that the fpn_inception backbone is used. If you want to try it with different backbone pretrain, please specify it also under ['model']['g_name'] in config/config.yaml.

## Pre-trained models

<table align="center">
    <tr>
        <th>Dataset</th>
        <th>G Model</th>
        <th>D Model</th>
        <th>Loss Type</th>
        <th>PSNR/ SSIM</th>
        <th>Link</th>
    </tr>
    <tr>
        <td rowspan="3">GoPro Test Dataset</td>
        <td>InceptionResNet-v2</td>
        <td>double_gan</td>
        <td>ragan-ls</td>
        <td>29.55/ 0.934</td>
        <td><a href="https://drive.google.com/uc?export=view&id=1UXcsRVW-6KF23_TNzxw-xC0SzaMfXOaR">fpn_inception.h5</a></td>
    </tr>
    <tr>
        <td>MobileNet</td>
        <td>double_gan</td>
        <td>ragan-ls</td>
        <td>28.17/ 0.925</td>
        <td><a href="https://drive.google.com/uc?export=view&id=1JhnT4BBeKBBSLqTo6UsJ13HeBXevarrU">fpn_mobilenet.h5</a></td>
    </tr>
    <tr>
        <td>MobileNet-DSC</td>
        <td>double_gan</td>
        <td>ragan-ls</td>
        <td>28.03/ 0.922</td>
        <td><a href=""></a></td>
    </tr>
</table>

## Parent Repository

The code was taken from <a href="">https://github.com/KupynOrest/RestoreGAN</a> . This repository contains flexible pipelines for different Image Restoration tasks.

## Citation

If you use this code for your research, please cite our paper.

```
​```
@InProceedings{Kupyn_2019_ICCV,
author = {Orest Kupyn and Tetiana Martyniuk and Junru Wu and Zhangyang Wang},
title = {DeblurGAN-v2: Deblurring (Orders-of-Magnitude) Faster and Better},
booktitle = {The IEEE International Conference on Computer Vision (ICCV)},
month = {Oct},
year = {2019}
}
​```
```

