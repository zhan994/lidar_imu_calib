# lidar_imu_calib

**This repo. works on the calibration of rotation between lidar and imu.** Because rotation is more important than translation for registration like icp, ndt and etc.

## compile

```
mkdir -p catkin_ws/src   
cd catkin_ws/src
git clone git@github.com:zhan994/lidar_imu_calib.git
cd ..
catkin_make
```

## run

1. record imu and lidar data

   ```
   rosbag record /imu /lidar_points
   ```

2. config launch file

   ```
   lidar_topic: lidar data topic name
   imu_topic: imu data topic name
   bag_file: *.bag file record imu and lidar data topic
   ```


3. start

   ```
   roslaunch lidar_imu_calib calib_exR_lidar2imu.launch
   ```

## reference

https://github.com/chennuo0125-HIT/lidar_imu_calib