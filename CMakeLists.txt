cmake_minimum_required(VERSION 3.0.2)
project(realsense_description)


find_package(catkin REQUIRED xacro)


catkin_package( CATKIN_DEPENDS xacro
#  INCLUDE_DIRS include
#  LIBRARIES realsense_description
#  CATKIN_DEPENDS other_catkin_pkg
#  DEPENDS system_lib
)


set(xacro_files
  ${CMAKE_CURRENT_SOURCE_DIR}/urdf/realsense_standalone.urdf.xacro
)

install(DIRECTORY config launch urdf
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)