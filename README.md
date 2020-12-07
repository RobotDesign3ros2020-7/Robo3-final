# Robo3-final


### build

https://github.com/IntelRealSense/realsense-ros

```

export ROS_VER=noetic

sudo apt-get install ros-$ROS_VER-realsense2-camera

cd ~/catkin_ws/src/

git clone https://github.com/IntelRealSense/realsense-ros.git

cd realsense-ros/

git checkout `git tag | sort -V | grep -P "^2.\d+\.\d+" | tail -1`

cd ..

catkin_init_workspace

cd ..

catkin_make clean

catkin_make -DCATKIN_ENABLE_TESTING=False -DCMAKE_BUILD_TYPE=Release

catkin_make install

```
