cmake_minimum_required(VERSION 4.0)
project(OpenCVExample)

set(CMAKE_CXX_STANDARD 17)

find_package(OpenCV REQUIRED)

include_directories(${OpenCV_INCLUDE_DIRS})
include_directories(${CMAKE_SOURCE_DIR}/..)

add_executable(OpenCVExample main.cpp rasterizer.hpp rasterizer.cpp global.hpp Triangle.hpp Triangle.cpp)

target_link_libraries(OpenCVExample ${OpenCV_LIBS})