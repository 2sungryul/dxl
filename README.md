# dxl

ros2 test package for dynamixel on Jetson nano

dependency : ros2 foxy, dynamixel C++ SDK, cmake 3.16

Publisher node receives a motion command from keyboard and publishes velocity commands of dynamixel using a ros2 interface geometry_msgs/msg/Vector3.

Subscriber node subscribes the velocity command topic and sends it to dynamixel.

# run subscriber on Jetson nano

$ cd ~/ros2_ws/src

$ git clone https://github.com/2sungryul/dxl.git

$ cd ~/ros2_ws

$ colcon build --symlink-install --packages-select dxl

$ source install/local_setup.bash

$ sudo chmod a+rw /dev/ttyUSB0

$ ros2 run dxl sub

# run publisher on Jetson nano

$ ros2 run dxl pub

command) f: forward, b: backword, s: stop, l : ccw rotate, r : cw rotate

