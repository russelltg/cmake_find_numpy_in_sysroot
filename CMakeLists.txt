cmake_minimum_required(VERSION 3.21)
project(findnumpyinsysroot C)


# set(Python3_NumPy_INCLUDE_DIR "${CMAKE_SYSROOT}/lib/python3/dist-packages/numpy/core/include")
set(Python3_ROOT_DIR ${CMAKE_SYSROOT})
find_package(Python3 3.8 COMPONENTS Development NumPy REQUIRED)

message("python include dir ${Python3_INCLUDE_DIRS}")
message("NumPy include dir: ${Python3_NumPy_INCLUDE_DIRS}")

add_executable(test main.c)
