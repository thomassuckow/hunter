cmake_minimum_required(VERSION 3.0)

set(Boost_DEBUG ON CACHE BOOLEAN "")

# Emulate HunterGate:
# * https://github.com/hunter-packages/gate
include("../common.cmake")

project(download-boost)

hunter_add_package(Boost COMPONENTS contract)
find_package(Boost CONFIG REQUIRED contract)

add_executable(foo foo.cpp)
target_link_libraries(foo PUBLIC Boost::contract)
