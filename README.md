# Universal-Robot-Simulation-by-ROS-2-and-Gazebo
Simulate a UR5 Robot in ROS2 + Gazebo | From Official Repo to Custom Package (Step-by-Step Guide)
#### Prerequisite
Before implementing this project, you have to set your environment by installing following software:
1. Ubuntu 22.04 LTS
2. ROS 2 Humble
3. Gazebo
Remember to install these packages in your system:
```bash
sudo apt install ros-humble-ros2-control
sudo apt install ros-humble-ros2-controllers
sudo apt install ros-humble-gripper-controllers
sudo apt install ros-humble-gazebo-ros2-control
sudo apt install ros-humble-gazebo-ros-pkgs
sudo apt install ros-humble-xacro
sudo apt install ros-humble-rmw-cyclonedds-cpp
sudo apt install ros-humble-sensor-msgs
```
#### 1st step:
create a workstation in your terminator by run 
```bash
mkdir ur_yt_ws
cd ur_yt_ws/
colcon buil
```
Now, source your project from the Universal Robot official repo.
```bash
source install/setup.bash
cd src
git clone -b humble https://github.com/UniversalRobots/Universal_Robots_ROS2_Description.git
git clone -b humble https://github.com/UniversalRobots/Universal_Robots_ROS2_Gazebo_Simulation.git
rosdep update && rosdep install --ignore-src --from-paths . -y
cd ../ #back to main folder
colcon build
```
Now you can analyze the packages 
```bash
source install/setup.bash
cd src
ls
code ./
```
