cmake_minimum_required(VERSION 3.4)

project(HelloWorld)

set(CMAKE_CXX_STANDARD 11)

set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_library(hello STATIC /home/touir/Touir/workspace/lab04/formatter_ex_lib/formatter_ex.cpp  /home/touir/Touir/workspace/lab04/formatter_lib/formatter.cpp)
include_directories(/home/touir/Touir/workspace/lab04/formatter_ex_lib /home/touir/Touir/workspace/lab04/formatter_lib)
add_executable(Hello /home/touir/Touir/workspace/lab04/hello_world_application/hello_world.cpp)
target_link_libraries(Hello hello)
