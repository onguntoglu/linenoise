cmake_minimum_required(VERSION 3.25)
project(linenoise VERSION 1.0 LANGUAGES C)

set(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR} ${CMAKE_MODULE_PATH})

include_directories("${PROJECT_SOURCE_DIR}")

add_library(linenoise INTERFACE)
target_sources(linenoise INTERFACE "linenoise.c" "linenoise.h")
target_link_libraries(linenoise INTERFACE c rt)
