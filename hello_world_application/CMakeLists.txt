cmake_minimum_required(VERSION 3.20)
project(hello_world VERSION 0.0.1)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(hello_world ${CMAKE_CURRENT_SOURCE_DIR}/hello_world.cpp)
add_library(formatter STATIC ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib/formatter.cpp)
add_library(formatter_ex STATIC ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib/formatter_ex.cpp)

include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib)

target_link_libraries(${PROJECT_NAME} ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_ex_lib/libformatter_ex.a)
target_link_libraries(${PROJECT_NAME} ${CMAKE_CURRENT_SOURCE_DIR}/../formatter_lib/libformatter.a)
