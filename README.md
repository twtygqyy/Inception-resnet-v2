# Inception-resnet-v2 Test
============================

Original Paper: "Inception-v4, Inception-ResNet and the Impact of Residual Connections on Learning"(https://arxiv.org/abs/1602.07261) from Google

## Notes
### Data augmentation applied (please find the data augmentation fork in https://github.com/twtygqyy/caffe-augmentation): 
```
max_color_shift = 5

contrast_variation = 0.8 ~ 1.2

max_brightness_shift = 5 

mirror = true

min_side = 328 ~ 380 and crop by 299x299 for training, min_side = 328 and crop by 299x299 for testing

init learning rate = 0.072 with RMSProp optimizer (rms_decay = 0.9 delta = 0.9)

max_iter = 666221

stepsize = 6663

gamma = 0.94

weight_decay = 0.0004

clip_gradients = 80

4 Geforce 1080 GPU are used for training and batch size = 5 x 4 (Very huge memory required for training)
```

## Result

Test net output #0: accuracy_top1 = 0.692693

Test net output #1: accuracy_top5 = 0.88327

The result is far from the performance of original paper, different solver with more iterations is under training right now

