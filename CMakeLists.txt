project(FoundationTimer)
cmake_minimum_required(VERSION 2.8.12)

add_definitions("-std=c++11")

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
# See See https://github.com/conan-io/conan/issues/1448 for why I use NO_OUTPUT_DIRS
conan_basic_setup(NO_OUTPUT_DIRS)

add_executable(timer timer.cpp)
target_link_libraries(timer ${CONAN_LIBS})
