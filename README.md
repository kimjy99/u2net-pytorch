# U2-Net
A Pytorch implementation of [U2-Net: Going Deeper with Nested U−Structure for Salient Object Detection](https://arxiv.org/abs/2005.09007) trained with CelebAMask

<p align="center">
  <img src="./images/karina6-combined.gif" width="400"/>
  <img src="./images/iu-combined_mh.gif" width="400"/>
</p>

## 1. Train with Matting Human Dataset (2022.08.01)
I made a dataset and upload in Kaggle after pre-processing. ([288x384](https://www.kaggle.com/datasets/kimjiyeop/matting-human-288x384) & [216x288](https://www.kaggle.com/datasets/kimjiyeop/matting-human-216x288))  

### Implementation Details
```
augmentation: 288x384 → RandomHorizontalFlip → RandomCrop → 256x256
optimizer: Adam (learning rate = 1e-4) 
epoch: 25
loss weight: all 1
batch size: 12

train loss: binary cross entrophy
validation & test loss: mean absolute error (L1 loss)
```

### Output of test dataset images
<p align="center">
  <img src="./images/result_mh.png" style="width:700px;"/>
</p>

### Convert GIFs
<p align="center">
  <img src="./images/karina1-combined.gif" width="400"/>
  <img src="./images/karina2-combined.gif" width="400"/>
</p>
<p align="center">
  <img src="./images/karina3-combined.gif" width="400"/>
  <img src="./images/karina4-combined.gif" width="400"/>
</p>
<p align="center">
  <img src="./images/karina5-combined.gif" width="400"/>
  <img src="./images/karina6-combined.gif" width="400"/>
</p>

### Loss
#### Train loss
<p align="center">
  <img src="./images/train_loss_mh.png" style="width:500px;"/>
</p>

#### Valid loss
<p align="center">
  <img src="./images/valid_loss_mh.png" style="width:500px;"/>
</p>
- minimum: 0.0077

#### Test loss
Mean absolute error for test images: 0.00806

## 2. Train with CelebAMask (2022.06.24)
I made a dataset and upload in Kaggle after pre-processing. ([128x128](https://www.kaggle.com/datasets/kimjiyeop/celeba-128-onlybg) & [256x256](https://www.kaggle.com/datasets/kimjiyeop/celeba-256-onlybg))  

### Implementation Details
```
image size: 128x128
optimizer: Adam (learning rate = 1e-3)
epoch: 25
loss weight: all 1
batch size: 12

train loss: binary cross entrophy
validation & test loss: mean absolute error (L1 loss)
```

### Output of test dataset images
<p align="center">
  <img src="./images/result.png" style="width:500px;"/>
</p>

### Convert GIFs
<p align="center">
  <img src="./images/iu-combined.gif" width="400"/>
  <img src="./images/elon-combined.gif" width="400"/>
</p>

### Loss
#### Train loss
<p align="center">
  <img src="./images/train_loss.png" style="width:500px;"/>
</p>

#### Test loss
Mean absolute error for test images: 0.02649
