cmake_minimum_required(VERSION 3.5.1)
project(dccomms_ros_msgs)

find_package(ament_cmake REQUIRED)
find_package(rosidl_default_generators REQUIRED)

rosidl_generate_interfaces(${PROJECT_NAME}
  srv/AddAcousticDevice.srv
  srv/CheckDevice.srv
  srv/CheckChannel.srv
  srv/RemoveDevice.srv
  srv/AddAcousticChannel.srv
  srv/LinkDeviceToChannel.srv
  srv/StartSimulation.srv
  srv/AddCustomDevice.srv
  srv/AddCustomChannel.srv
)

ament_export_dependencies(rosidl_default_runtime)

install(DIRECTORY include/${PROJECT_NAME}
  DESTINATION include
)

ament_package()
