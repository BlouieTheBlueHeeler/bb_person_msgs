cmake_minimum_required(VERSION 3.0.2)
project(bb_person_msgs)

find_package(catkin REQUIRED COMPONENTS
  sensor_msgs
  std_msgs
  message_generation
)

################################################
## Declare ROS messages, services and actions ##
################################################

## Generate messages in the 'msg' folder
add_message_files(
  FILES
  BodySegment.msg
  Person.msg
  Persons.msg
  TrackingStates.msg
)

generate_messages(
   DEPENDENCIES
   std_msgs
   sensor_msgs
)

###################################
## catkin specific configuration ##
###################################
catkin_package()

###########
## Build ##
###########

## Specify additional locations of header files
## Your package locations should be listed before other locations
include_directories(
  ${catkin_INCLUDE_DIRS}
)
