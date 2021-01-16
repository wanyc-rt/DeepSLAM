## 科研笔记
## 1.16
[Every pixel counts++:Joint learning of geometry and motion with 3d holistic understanding](https://blog.csdn.net/qq_42518956/article/details/103402408)

## 1.15
DeepLiDAR: Deep Surface Normal Guided Depth Prediction for Outdoor Scene from Sparse LiDAR Data and Single Color Image

## 1.12 
[Mono-SF: Multi-View Geometry Meets Single-View Depth for Monocular Scene Flow Estimation of Dynamic Traffic Scenes](https://arxiv.org/pdf/1908.06316.pdf)

单目场景流估计在动态的traffic scenes

[Self-Supervised Deep Visual Odometry with Online Adaptation](https://arxiv.org/pdf/2005.06136.pdf)

Occlusions, Motion and Depth Boundaries with a Generic Network for Disparity, Optical Flow or Scene Flow Estimation


## 1.10
[FlowFusion: Dynamic Dense RGB-D SLAM Based on Optical Flow](https://arxiv.org/pdf/2003.05102.pdf)

[StaticFusion: Background Reconstruction for Dense RGB-D SLAM in Dynamic Environments](https://www.robots.ox.ac.uk/~mobile/Papers/2018ICRA_scona.pdf)
## 1.8

Metrically-Scaled Monocular SLAM using Learned Scale Factors

12.30
[Learning Rigidity in Dynamic Scenes with a Moving Camera for 3D Motion Field Estimation (ECCV 2018)](https://github.com/NVlabs/learningrigidity)

[GeoNet](https://github.com/yzcjtr/GeoNet)

## 12.19 
[Robust Dense Mapping for Large-Scale Dynamic Environments](https://arxiv.org/pdf/1905.02781.pdf) 双目重建代码
[Code](http://andreibarsan.github.io/dynslam) 

[Exploiting Semantic and Public Prior Information in MonoSLAM](https://ras.papercept.net/proceedings/IROS20/1418.pdf)使用一个预先训练过的开源语义分割网络(DeepLabV3+)扩展了ORB-SLAM2，以结合来自开放街道地图构建轨迹数据的先验信息。.

[PL-VINS Real-Time Monocular Visual-Inertial SLAM with Point and Line Features](http://arxiv.org/pdf/2009.07462v2.pdf) [Code]( https://github.com/cnqiangfu/PL-VINS)基于点和线的实时VINS

[Depth Estimation from Monocular Images and Sparse Radar Data](https://arxiv.org/pdf/2010.00058.pdf) radar data 补全



## 12.13
Unsupervised Depth Completion From Visual Inertial Odometry[!重要] (用VIO稀疏深度提高单目深度估计结果)
从这篇文章风格出发对其进行改进

## 12.11 
双目无监督连续深度光流ego-motion和3D object 6DoF 估计

## 12.9 
### 无监督object 6DOF estimation 
https://patrick-llgc.github.io/Learning-Deep-Learning/paper_notes/obj_motion_net.html
Learning Independent Object Motion from Unlabelled Stereoscopic Videos (ICAR19)本文从深度位姿估计开始借助光流,用ROI的2D特帧自动生成该目标的mask并将它对应到3D Motion中,实现估计场景中独立运动物体的运动速度和方向.
[基于图像的动态物体估计总结](https://blog.csdn.net/qq_26623879/article/details/106085106)

[Semantically-Guided Representation Learning for Self-Supervised Monocular Depth语义引导深度](https://adriengaidon.com/publication/2020-04-26-Semantically-Guided-Representation-Learning-for-Self-Supervised-Monocular-Depth) 
### 用光流去判断mask的物体是否运动，在深度估计中是否去除




## 12.8 
[ DetectoRS: Detecting Objects with Recursive Feature Pyramid and Switchable Atrous Convolution](https://github.com/joe-siyuan-qiao/DetectoRS)实例分割

[Self-Supervised Scene De-occlusion](https://www.cnblogs.com/luckforefforts/p/13665484.html)自监督去遮挡

### 深度联合语义分割，可不可以改为实例，并用实例提高深度和语义，并且实现动态物体分割。并用光流网络估计位姿
### 光流和深度在非结构运动中的估计（非刚体区域去除）
- 论文[GeoNet: Unsupervised Learning of Dense Depth, Optical Flow and Camera Pose](https://arxiv.org/pdf/1803.02276.pdf)
  - rigid structure reconstructor
  - nonrigid motion localizer respectively
- [Unsupervised Scale-consistent Depth and Ego-motion Learning from Monocular Video](https://arxiv.org/pdf/1908.10553.pdf) 光流与深度的关联
   用光流估计网络来约束，前后帧之间深度的训练
- [UnOS: Unified Unsupervised Optical-flow and Stereo-depth Estimation by](https://openaccess.thecvf.com/content_CVPR_2019/papers/Wang_UnOS_Unified_Unsupervised_Optical-Flow_and_Stereo-Depth_Estimation_by_Watching_Videos_CVPR_2019_paper.pdf)
Watching Videos
## 用self-scene estimation 进行无3Dbox运动估计
- [Self-supervised Object Motion and Depth Estimation from Video](https://arxiv.org/pdf/1912.04250.pdf)
![image1](https://github.com/alluserman/DeepSLAM/blob/main/image/typora_picture/Screenshot%20from%202020-12-11%2011-03-21.png)
- [Robust Ego and Object 6-DoF Motion Estimation and Tracking](https://arxiv.org/pdf/2007.13993.pdf)

## 12.4
深度估计和光流联合估计，然后用orb-slam来监督并在test过程中Refine网络
深度网络和光流估计出场景流+位姿，然后用实例mask作为边界去对动态物体进行6dof估计和重建（在DF网络上加入实例分割网络）
DF-Net: Unsupervised Joint Learning of Depth and Flow using Cross-Task Consistency
Fully Convolutional Geometric Features 特征提取

## 12.2
1.ME(Minkowski Enginge)Sparse Convelution 原理与用法
1.1 3D稀疏卷积原理与应用
- 4D-SpatioTemporal ConvNets: Minkowski Convolutional Neural Networks, CVPR'19
- Fully Convolutional Geometric Features, ICCV, 2019
- Generative Sparse Detection Networks for 3D Single-shot Object Detection

2.TensorRT Tenfei的depthe fusion DSO

3.语义分割



## 11.30 
室内语义分割
sparse convolution[MinkowskiEngine](https://github.com/NVIDIA/MinkowskiEngine)

## 11.29 
[github pull request](https://www.cnblogs.com/momo798/p/11599679.html)
Video Depth Estimation by Fusing Flow-to-Depth Proposals 从Flow预测depth方法

## 11.27

[VITAMIN-E: VIsual Tracking And MappINg with Extremely Dense Feature Points](https://arxiv.org/pdf/1904.10324.pdf)[code](https://github.com/eowjd0512/VITAMIN-E)稠密特征重建
Deep Depth Estimation from Visual-Inertial SLAM
Depth Prediction Without the Sensors: Leveraging Structure for Unsupervised Learning from Monocular Videos
Learning Monocular 3D Vehicle Detection without 3D Bounding Box Labels
D3VO: Deep Depth, Deep Pose and Deep Uncertainty for Monocular Visual Odometry


## 11.26
#突发奇想1  可以用融合IMU估计位姿的方法来约束深度估计
#突发奇想2  在深度补全网络中，加入光流的3Dloss(IROS20)
#突发奇想3  可以将光流和深度组成一个多任务实时网络进行位姿和深度估计联合网络并在TX2实验（self scene flow estimation)


今天关注深度特征提取的方法,可不可以提出一种能够端到端的深度检测方法，类VO中的提取方法，这样就可以实现端到端深度SLAM了。
从这篇文章出发[Deep Keypoint-Based Camera Pose Estimation with Geometric constraist](https://ras.papercept.net/proceedings/IROS20/0463.pdf)从特征提取，描述，匹配用学习方法代替传统方法，作者借用了superPoint([SuperPoint: Self-Supervised Interest Point Detection and Description](https://arxiv.org/pdf/1712.07629.pdf)特征提取方法以及改进的[Deep Fundamental Matrix Estimation](http://vladlen.info/papers/deep-fundamental.pdf)基础矩阵求解方法结合，改进DFE求出F矩阵。度估计中可以用这种方法代替Pointnet试试效果
## 11.12 
[IROS2020]DeepLiDARFlow: A Deep Learning Architecture For Scene Flow Estimation Using Monocular Camera and Sparse LiDAR
光流和深度 与下面文章有相似之处
[IROS2020]Monocular Depth Prediction through Continuous 3D Loss
这两篇论文可以用3D loss 来约束稀疏雷达深度补全

也可以考虑使用联合估计的方法 Self-Supervised Monocular Scene Flow Estimation



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
