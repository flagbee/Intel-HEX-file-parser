cmake_minimum_required(VERSION 3.26)
project(ihex_parser C CXX)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 17)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH};${PROJECT_SOURCE_DIR}/cmake)
set(BUILD_EXAMPLE ON CACHE BOOL "Build examples")

include_directories(include)
add_subdirectory(src)

if(BUILD_EXAMPLE)
  add_subdirectory(example)
endif()

