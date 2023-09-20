cmake_minimum_required(VERSION 3.8)
project(stretch_msgs)

add_compile_options(-std=c++14)

find_package(ament_cmake REQUIRED)
find_package(rclcpp REQUIRED)
find_package(std_msgs REQUIRED)
find_package(rosidl_default_generators REQUIRED)

#######################################
## Declare ROS messages and services ##
#######################################

rosidl_generate_interfaces(${PROJECT_NAME}
  "srv/Float64.srv"
  DEPENDENCIES std_msgs
)

ament_export_dependencies(rosidl_default_runtime)

ament_package()
