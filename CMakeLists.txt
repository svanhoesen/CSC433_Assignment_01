cmake_minimum_required(VERSION 2.8.11)
project(basic_sdl)

set(CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/cmake)
find_package(SDL2)

set(basic_sdl_sources
  main.cpp 
)

include_directories (${SDL2_INCLUDE_DIR})
add_executable (${PROJECT_NAME} ${basic_sdl_sources})
target_link_libraries(${PROJECT_NAME} ${SDL2_LIBRARY})

