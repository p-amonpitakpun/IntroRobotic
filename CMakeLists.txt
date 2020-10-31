cmake_minimum_required (VERSION 3.0.0)
project (IntroRobotic)

include_directories ("opencv/build/install/include")
add_executable (IntroRobotic ${CMAKE_CURRENT_SOURCE_DIR}/src/main.cpp)

set_property (DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR} PROPERTY VS_STARTUP_PROJECT IntroRobotic)