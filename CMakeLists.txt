cmake_minimum_required(VERSION 2.8.3)
project(dr_msgs)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  roscpp
)

add_service_files(
  FILES
  SendInt.srv
  GetBool.srv
  SendBool.srv
)

generate_messages(
  DEPENDENCIES
  std_msgs  # Or other packages containing msgs
)

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES dr_msgs
   CATKIN_DEPENDS message_runtime
#  DEPENDS system_lib
)


include_directories(
  ${catkin_INCLUDE_DIRS}
)
