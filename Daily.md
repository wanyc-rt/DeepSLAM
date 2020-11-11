## 科研笔记





## 11.11

Deep Depth Estimation from Visual-Inertial SLAM

这篇文章在深度不全之前，利用稀疏的深度将场景中的平面和法向量估计出来，为了估计平面先用mesh方法生成平面，然后通过Mask-rcnn进行提取预测。

——————————————————————————————————————————————————————————

### 9.4

[CVPR2020 感知论文](https://zhuanlan.zhihu.com/p/151596272)



9.6

0：23 mappoint 生成地图点

9.14

mmdetection 中的registry类

https://zhuanlan.zhihu.com/p/100210452



语义分割综述

https://github.com/kingqiuol/semseg

单目图像和稀疏激光点云融合

[DeepLiDARFlow: A Deep Learning Architecture For Scene Flow Estimation Using Monocular Camera and Sparse LiDAR](https://arxiv.org/pdf/2008.08136.pdf)

Self-Supervised Deep Pose Corrections for Robust Visual Odometry

https://github.com/utiasSTARS/ss-dpc-net

https://www.computerrobotvision.org/proceedings/pdfs/CRV2020-1ugoWdlO2rSdvYvbAocrmh/989100a190/989100a190.pdf

https://ieeexplore.ieee.org/abstract/document/9091036

## 9.15

### VOLDOR Visual Odometry from Log logistic Dense Optical flow Residual CVPR2020



9.25

[深度估计伪激光雷达生成](https://mp.weixin.qq.com/s?__biz=MzU1MjY4MTA1MQ==&mid=2247519962&idx=2&sn=29edb0416d3309910794581c61acf850&chksm=fbfca5eecc8b2cf8c1222d34d1e218d97291adb3e71f9ca7b8312ed657ac2ca2eb4d29b42c48&mpshare=1&scene=1&srcid=09242wFjTNBPbqd4fje1KDnA&sharer_sharetime=1600941883433&sharer_shareid=08a5efa40af25b6a57bd07cf52cdcd42&exportkey=AbI8%2Bx2%2BY5jamQUoE22X%2FlA%3D&pass_ticket=%2Fy11TTNTny7Rw0RZ30U13Th%2FwI%2F3qnxTo1p%2BHXVK14y0ff44ImS3D2rpizrQn5JJ&wx_header=0#rd)

[Auto-Depth codo](https://github.com/MankaranSingh/Auto-Depth)

#### Real Time Dense Depth Estimation by Fusing Stereo with Sparse Depth Measurements 融合稀疏深度测量的双目实时稠密深度估计 本文通过对现有的stereo match 估计中的3D cost volume改进，降低3d cost volume的计算量同时融合稀疏的深度测量值。 可以用双目匹配的稀疏深度提升整体深度估计。

#### DeepLiDAR: Deep Surface Normal Guided Depth Prediction for Outdoor Scene from Sparse LiDAR Data and Single Color Image

深度法线引导

## 9.30

### 3D-Reconstruction through Monocular images

https://medium.com/swlh/making-a-pseudo-lidar-with-cameras-and-deep-learning-e8f03f939c5f



## 10.26

[Enhancing self-supervised monocular depth estimation with traditional visual odometry](https://arxiv.org/pdf/1908.03127.pdf)

[On the uncertainty of self-supervised monocular depth estimation](https://arxiv.org/pdf/2005.06209.pdf)

## 10.27

目前情况总结

深度估计联合SLAM的思路：

**单目VIO深度估计**

用SLAM估计的pose融合光流估计的pose得出一个带有特征点绝对尺度的深度图，然后将该深度图用于融合monodepth的深度估计中。在测试阶段，用VIO的深度refine深度估计结果，用深度估计的dense depth，使得ORB-SLAM，能够表现更好

**双目VIO深度估计**

用双目匹配的深度估计方法，左右匹配，估计深度，然后融合双目SLAM的深度图以及前后帧之间的pose估计，来训练深度估计，在此可以假设一个双目基线内参，形成伪双目的深度估计。。

## 11.11

Deep Depth Estimation from Visual-Inertial SLAM
