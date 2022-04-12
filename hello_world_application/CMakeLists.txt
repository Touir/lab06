cmake_minimum_required(VERSION 3.4)

project(HelloWorld)

set(CMAKE_CXX_STANDARD 11)

set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(hello STATIC ${CMAKE_CURRENT_SOURCE_DIR}/formatter_ex_lib/formatter_ex.cpp ${CMAKE_CURRENT_SOURCE_DIR}/formatter_lib/formatter.cpp)
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/formatter_ex_lib ${CMAKE_CURRENT_SOURCE_DIR}/formatter_lib)
add_executable(Hello ${CMAKE_CURRENT_SOURCE_DIR}/hello_world_application/hello_world.cpp)
target_link_libraries(Hello hello)
