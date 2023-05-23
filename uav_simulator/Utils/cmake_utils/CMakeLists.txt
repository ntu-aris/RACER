cmake_minimum_required(VERSION 2.8.3)
project(cmake_utils)

set(CMAKE_BUILD_TYPE "Release")
set(CMAKE_CXX_FLAGS "-std=c++17")
set(CMAKE_CXX_FLAGS "-O3 -Wall")

find_package(catkin REQUIRED COMPONENTS roscpp)

set(CMAKE_MODULE_PATH ${CMAKE_CURRENT_LIST_DIR}/cmake)

file(GLOB CMAKE_UILTS_FILES cmake/*.cmake)

catkin_package(
  CFG_EXTRAS ${CMAKE_UILTS_FILES}
)

