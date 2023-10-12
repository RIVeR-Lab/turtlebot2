# Turtlebot_on_Noetic

The Turtlebot2 packages installation on ROS noetic

References: 
- [Turtlebot2-On-Melodic](https://github.com/gaunthan/Turtlebot2-On-Melodic)
- [turtlebot2-on-noetic](https://github.com/Aoi-hosizora/turtlebot2-on-noetic)

## Environment

Ubuntu 20.04

ROS Noetic

## Installation

### Dependencies:
```
sudo apt-get install ros-noetic-sophus ros-noetic-joy libusb-dev libftdi-dev ros-noetic-base-local-planner ros-noetic-move-base-msgs
```

### Compiling from source:
```
mkdir ~/catkin_ws/src -p
cd ~/catkin_ws/src
git clone git@github.com:RIVeR-Lab/turtlebot2.git
cd turtlebot2
git checkout noetic-river-v0
sh turtlebot_noetic.sh
cd ~/catkin_ws
catkin build
source devel/setup.bash
```

## Test

Simulation

```
roslaunch turtlebot_gazebo turtlebot_world.launch
```

Teleop control

```
roslaunch turtlebot_teleop keyboard_teleop.launch
```
