# this script adds all subprojects to a single build to allow IDEs understand the full project

cmake_minimum_required(VERSION 3.14...3.22)

project(BuildAll LANGUAGES CXX)

set_property(GLOBAL PROPERTY CTEST_TARGET_DIRECTORY ${CMAKE_BINARY_DIR}/test)

# add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/targets/all ${CMAKE_BINARY_DIR}/all)

project(BuildAll LANGUAGES CXX)

include(cmake/options.cmake)
include(cmake/tools.cmake)

# needed to generate test target
enable_testing()

add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/targets/cmds/greeter ${CMAKE_BINARY_DIR}/cmds/greeter)
add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/targets/tests/greeter ${CMAKE_BINARY_DIR}/tests/greeter)
add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/targets/docs/greeter ${CMAKE_BINARY_DIR}/docs/greeter)
