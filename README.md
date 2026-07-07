# DopRIO: Doppler Strengthened Tightly-Coupled 4D Millimeter-Wave Radar–Inertial Odometry

Our paper **_DopRIO: Doppler Strengthened Tightly-Coupled 4D Millimeter-Wave Radar–Inertial Odometry_** has been accepted by **_Robotics and Autonomous Systems_**. \[[paper](https://www.sciencedirect.com/science/article/pii/S0921889026002708)\]

## 1.Dependency
### 1.1 Ubuntu and Ros  
Ubuntu 20.04 and Ros Noetic
### 1.2 Required library
Eigen3, PCL, Sophus(fmt), Boost, OpenMP, TBB
### 1.3 Required ROS packages
pcl_ros, pcl_conversions, sensor_msgs, geometry_msgs, nav_msgs
## 2.Run the project
Download our project and put it into your workspace catkin

First you need to compile it

`catkin build`

`source devel/setup.bash`

Then you can run our launch file

`roslaunch rise rise_serial.launch`

## 3.Acknowlegement
[slam in autonomous driving](https://github.com/gaoxiang12/slam_in_autonomous_driving)
[slambook-en](https://github.com/gaoxiang12/slambook-en) , [slam in autonomous driving](https://github.com/gaoxiang12/slam_in_autonomous_driving) and [Dr. Gao Xiang](https://github.com/gaoxiang12). His SLAM tutorial and code are the starting point of our SLAM journey.

[Coloradar](https://arpg.github.io/coloradar/) and [NTU4DRADLM](https://github.com/junzhang2016/NTU4DRadLM). Many thanks to all the authors of the two public datasets.

## 4.Implementation Details
DopRIO is implemented as a tightly-coupled 4D millimeter-wave radar-inertial odometry system. The pipeline jointly uses radar point clouds, Doppler velocity measurements, and IMU measurements for robust state estimation under sparse and noisy radar observations. In particular, Doppler information is used to refine radar points, estimate point-wise uncertainty for registration, and construct a joint registration-Doppler residual in the filtering framework. Before running the system, please make sure that the radar-IMU extrinsic calibration, timestamp synchronization, Doppler sign convention, and dataset-specific parameters are correctly configured.


## 5.Demo
Demo in the Outdoors6 sequence of ColoRadar Dataset 
![Demo](apps/pic/ourdoors6.gif)
Demo in the 2nd sequence of Our collected real-world data 
![Demo](apps/pic/ours1.gif)

## 6.Citation
If you find this work useful for your research, please consider citing our paper:

```bibtex
@article{CHENG2026105598,
  title   = {DopRIO: Doppler strengthened tightly-coupled 4D millimeter-wave radar-inertial odometry},
  author  = {Ruiqi Cheng and Huijun Di and Jian Li and Feng Liu and Wei Liang},
  journal = {Robotics and Autonomous Systems},
  volume  = {205},
  pages   = {105598},
  year    = {2026},
  issn    = {0921-8890},
  doi     = {10.1016/j.robot.2026.105598},
  url     = {https://www.sciencedirect.com/science/article/pii/S0921889026002708}
}
```

