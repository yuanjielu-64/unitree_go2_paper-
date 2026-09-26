# unitree_go2_barn_challenge

# install ros2
Humble : https://docs.ros.org/en/humble/Installation/Ubuntu-Install-Debs.html

# install gazebo
sudo apt install ros-foxy-gazebo-ros-pkgs
sudo apt install ros-foxy-gazebo-plugins

# install simulation to go2

https://github.com/Zhefan-Xu/isaac-go2-ros2

https://github.com/anujjain-dev/unitree-go2-ros2/tree/humble

https://github.com/Unitree-Go2-Robot/go2_robot

https://github.com/abizovnuralem/go2_ros2_sdk

https://github.com/jizhang-cmu/autonomy_stack_go2/tree/foxy-humble

https://github.com/arjun-sadananda/go2_nav2_ros2

https://github.com/jkk-research/pointcloud_to_grid

https://github.com/abizovnuralem/go2_omniverse

https://github.com/dfloreaa/point_lio_ros2
SLAM 用于地图

https://github.com/leggedrobotics/terrain-generator terrain generator

https://github.com/ANYbotics/elevation_mapping

https://github.com/Teddy-Liao/walk-these-ways-go2/tree/main

https://developer.nvidia.com/blog/closing-the-sim-to-real-gap-training-spot-quadruped-locomotion-with-nvidia-isaac-lab/

https://www.youtube.com/watch?v=z62oU4hM1xM

https://github.com/marmotlab/SATA

https://github.com/leggedrobotics/legged_gym

# install unitree go2

Need to read 
https://github.com/unitreerobotics/unitree_ros2

git clone https://github.com/unitreerobotics/unitree_ros2

# install unitree go2 sdk in system

https://github.com/unitreerobotics/unitree_sdk2

# 关于真实机器人的理解

https://github.com/unitreerobotics/unitree_sdk2
该SDK主要用于控制真实机器人。在gazebo中写好的算法需要进行一定转换到sdk2然后进行真实控制
Jackal等一系列小车就不需要

# how to generate the map
Issac gym https://github.com/leggedrobotics/terrain-generator

# Fix the problem for 
```
[spawner-33] [ERROR] [1706000264.234976868] [rmw_cyclonedds_cpp]: rmw_create_node: failed to create domain, error Error
[spawner-33] 
[spawner-33] >>> [rcutils|error_handling.c:108] rcutils_set_error_state()
[spawner-33] This error state is being overwritten:
[spawner-33] 
[spawner-33]   'error not set, at ./src/rcl/node.c:262'
[spawner-33] 
[spawner-33] with this new error message:
[spawner-33] 
[spawner-33]   'rcl node's rmw handle is invalid, at ./src/rcl/node.c:433'
[spawner-33] 
[spawner-33] rcutils_reset_error() should be called after error handling to avoid this.
[spawner-33] <<<
[spawner-33] [ERROR] [1706000264.235045107] [rcl]: Failed to fini publisher for node: 1
```
https://github.com/ros2/rmw_cyclonedds/issues/458

https://github.com/lupinjia/LeggedGym-Ex


[x,y,yaw]  -->   [x, y, yaw, height]
在奖励函数中，  去 贴近  他的身体高度，
测试的最低高度 是 0.1- 0.35 

