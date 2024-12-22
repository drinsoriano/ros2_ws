Project Overview

ROS2 workspace that integrates:

DDSM115: Controlled via RS485 for motor control without encoder feedback.
LiDAR: For mapping and obstacle detection (e.g., RPLIDAR or Hokuyo).
Nav2 (Navigation2): For path planning and navigation.
Since the motor lacks encoders, odometry will be approximated using motor speed commands and supplemented with LiDAR and/or IMU data.
