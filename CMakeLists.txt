cmake_minimum_required(VERSION 2.8.3)
project(ark_msgs)

find_package(catkin REQUIRED COMPONENTS geometry_msgs message_generation std_msgs)

# include_directories(include)

add_message_files(
  DIRECTORY msg
  FILES
  PidErrors.msg  
)

# add_service_files(
#   DIRECTORY srv
#   FILES
#   CommandBool.srv
# )

# add_action_files(
#   DIRECTORY action
#   FILES
#   Action1.action
#   Action2.action
# )

generate_messages(DEPENDENCIES geometry_msgs std_msgs)

catkin_package(
#  INCLUDE_DIRS include
  CATKIN_DEPENDS geometry_msgs message_runtime std_msgs)

#install(DIRECTORY include/${PROJECT_NAME}/
#  DESTINATION ${CATKIN_PACKAGE_INCLUDE_DESTINATION}
#  FILES_MATCHING PATTERN "*.h")
