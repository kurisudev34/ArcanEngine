cmake_minimum_required(VERSION 3.30)
project(ArcanEngine)

set(CMAKE_CXX_STANDARD 20)

find_package(SFML 2.6 COMPONENTS graphics window system REQUIRED)

file(GLOB_RECURSE SOURCES "src/*.cpp")

add_library(ArcanEngine SHARED ${SOURCES})

target_include_directories(ArcanEngine PUBLIC ${CMAKE_SOURCE_DIR}/include)
target_link_libraries(ArcanEngine sfml-graphics sfml-window sfml-system)
