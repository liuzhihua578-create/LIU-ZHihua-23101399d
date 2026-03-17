cmake_minimum_required(VERSION 3.0.2)
project(aae4011_vehicle_detection)

find_package(catkin REQUIRED)

catkin_package()

install(DIRECTORY launch/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

catkin_install_python(
  PROGRAMS
    scripts/extract_images.py
    scripts/vehicle_detector_node.py
    scripts/vehicle_detector_gui_node.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)