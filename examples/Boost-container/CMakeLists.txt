# Copyright (c)
# All rights reserved.

cmake_minimum_required(VERSION 3.2)

# Emulate HunterGate:
# * https://github.com/cpp-pm/gate
include("../common.cmake")

project(Boost-container)

# DOCUMENTATION_START {
hunter_add_package(Boost-container)
find_package(Boost-container CONFIG REQUIRED)

add_executable(boo boo.cpp)
target_link_libraries(boo PUBLIC PkgConfig::Boost-container)
# DOCUMENTATION_END }
