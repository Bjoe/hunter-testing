# Copyright (c) 2016-2018, Ruslan Baratov
# All rights reserved.

cmake_minimum_required(VERSION 3.2)

# Emulate HunterGate:
# * https://github.com/hunter-packages/gate
include("../common.cmake")

project(tiny-process-library)

# DOCUMENTATION_START {
find_package(Threads REQUIRED)
hunter_add_package(tiny-process-library)
find_package(tiny-process-library REQUIRED)

add_executable(boo boo.cpp)
target_link_libraries(boo PUBLIC tiny-process-library::tiny-process-library ${CMAKE_THREAD_LIBS_INIT})
# DOCUMENTATION_END }
