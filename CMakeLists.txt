cmake_minimum_required(VERSION 3.14...3.22)

project(BuildAll LANGUAGES CXX)

set_property(GLOBAL PROPERTY CTEST_TARGET_DIRECTORY ${CMAKE_BINARY_DIR}/test)

# add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/targets/all ${CMAKE_BINARY_DIR}/all)

project(BuildAll LANGUAGES CXX)

include(cmake/options.cmake)
include(cmake/tools.cmake)

# needed to generate test target
enable_testing()

add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/targets/bin ${CMAKE_BINARY_DIR}/bin)
add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/targets/test ${CMAKE_BINARY_DIR}/test)
add_subdirectory(${CMAKE_CURRENT_LIST_DIR}/targets/doc ${CMAKE_BINARY_DIR}/doc)
