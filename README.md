# ros2_ws_tutorial
This project follows a Humble distro ROS2 tutorial as documented on [Read the Docs](https://ros2course.readthedocs.io/en/latest/index.html). The aim is to gain a comprehensive understanding of ROS2 concepts, tools, and best practices. The repository will include example code, exercises, and notes based on the tutorial.

## Containers
Command to create container: 
```bash
docker run --name ros2_container -e DISPLAY=host.docker.internal:0.0 -v $pwd/ros2_ws/:/ros2_ws -it ros2_humble_image
```
Alternatively build the image with the command:
```bash
docker build -t ros2_humble_image:Dockerfile”
```
Command to run the container from different terminals: 
```bash
docker exec -it ros2_container bash
```

## ROS2 Setup
Set up the ROS 2 environment variables and its core functionalities
```bash
source /opt/ros/humble/setup.bash
```
Source the overlay by executing:
```bash
source install/setup.bash
```

## Packages
Command to create sample exec my_node inside my_package
```
ros2 pkg create --build-type ament_python --license Apache-2.0 --node-name my_node my_package
```
Same as
```bash
ros2 pkg create --build-type ament_cmake --license Apache-2.0 --node-name my_node my_package_cpp
```