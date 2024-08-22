cmake_minimum_required(VERSION 3.20)
project(solver VERSION 0.0.1)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(solver STATIC ${CMAKE_CURRENT_SOURCE_DIR}/solver.cpp)
include_directories(${CMAKE_CURRENT_SOURCE_DIR})
