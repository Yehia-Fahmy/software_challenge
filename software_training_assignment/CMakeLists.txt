cmake_minimum_required(VERSION 3.5)
project(software_training_assignment)

find_package(ament_cmake REQUIRED)
find_package(rclcpp REQUIRED)
find_package(turtlesim REQUIRED)
find_package(rclcpp_components REQUIRED)
find_package(std_msgs REQUIRED)
find_package(rcutils REQUIRED)
find_package(rcl REQUIRED)
find_package(rclcpp_action REQUIRED)
find_package(geometry_msgs REQUIRED)
find_package(builtin_interfaces REQUIRED)
find_package(rosidl_default_generators REQUIRED)

include_directories(include)

# my custom created msg, srv and action
rosidl_generate_interfaces(${PROJECT_NAME}
  "msg/message.msg"
  "srv/return_success.srv"
  "action/move_command.action"
  dependencies std_msgs geometry_msgs builtin_interfaces
)
ament_export_dependencies(rosidl_default_runtime)

set(node_plugins "")

ament_package()
