# CIFAR-10 #
---
Pytorch implementation for cifar-10 datasets.
# Background #
---
Homework for ZJU-CST Artificial Intelligence Safety
# Usage #
---
**Requirements**
> timm==0.4.12
> 
> torchvision==0.9.1+cu111
> 
> vit_pytorch==0.20.7
> 
> torch==1.8.1+cu111
> 
> torchsummary==1.5.1
## Training ##
**train**

`python train.py --model_name resnet50 --batch_size 64 --epoch_num 200 --worker_num 16 --learning_rate 0.01 --optimizer sgd --momentum 0.9 --datasets_path ./dataset/ --pth_path ./model_pth/`

**tensorboard**
    
`tensorboard --logdir runs`
 
## Testing ##
**test**
`python test.py --model_name resnet50 --batch_size 64 --worker_num 16 --datasets_path ./dataset/ --pth_path ./model_pth/`
# Results #
---
**model list**

- self_net: customsize cnn
- resnet50: based on imagenet pretrained resnet50
- vision_transformer: patch_size=4 depth=6
- vit_soat: ViT base (timm transfer)

|  Model Name   | Accuracy  |
|:----:|:----:|
| Self Net  | 50% |
| resnet50  | 87% |
| vision transformer| 80% |
| vit soat	| 95% |
---

**resnet50**

x-aixs:epoch 0~200 

learning_rate:1e-2,1e-3

|  y-axis:train_acc   | y-axis:train_loss  |
|:----:|:----:|
| ![train_acc](acc_train_resnet50.svg ''resnet50'')| ![train_loss](loss_train_resnet50.svg ''resnet50'') |



