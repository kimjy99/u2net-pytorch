# U2-Net
A Pytorch implementation of [U2-Net: Going Deeper with Nested U−Structure for Salient Object Detection](https://arxiv.org/abs/2005.09007) trained with CelebAMask

<p align="center">
  <img src="./images/elon-combined.gif" width="400"/>
</p>

## Dataset: CelebAMask
I made a dataset and upload in Kaggle after pre-processing.  
1. Use only background for mask images
2. Downsize to [128x128](https://www.kaggle.com/datasets/kimjiyeop/celeba-128-onlybg) & [256x256](https://www.kaggle.com/datasets/kimjiyeop/celeba-256-onlybg)  

## Implementation Details
```
optimizer: Adam
 - learning rate = 1e-3
 - betas = (0.9, 0.999)
 - epsilon = 1e-8
 - weight decay = 0
 
epoch: 25
loss weight: all 1
batch size: 12

train loss: binary cross entrophy
validation & test loss: mean absolute error (L1 loss)
```

## Output of test dataset images
<p align="center">
  <img src="./images/result.png" style="width:500px;"/>
</p>

## Loss
### Train loss
<p align="center">
  <img src="./images/train_loss.png" style="width:500px;"/>
</p>

### Test loss
Mean absolute error for test images: 0.02649

## Convert GIFs
<p align="center">
  <img src="./images/iu-combined.gif" width="400"/>
  <img src="./images/elon-combined.gif" width="400"/>
</p>
