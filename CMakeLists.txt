cmake_minimum_required(VERSION 3.0.2)
project(line_trace_tracer)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES line_trace_tracer
#  CATKIN_DEPENDS roscpp rospy
#  DEPENDS system_lib
)

include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

catkin_install_python(PROGRAMS src/linetrace_realsense.py src/linetrace_webcam.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)



install(DIRECTORY
   launch
   src
   DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
 )

