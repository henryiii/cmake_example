cmake_minimum_required(VERSION 3.4)
project(cmake_example)

# EXAMPLE_VERSION_INFO will be defined by setup.py

add_subdirectory(pybind11)
pybind11_add_module(cmake_example src/main.cpp)

target_compile_definitions(cmake_example PRIVATE VERSION_INFO=${EXAMPLE_VERSION_INFO})
