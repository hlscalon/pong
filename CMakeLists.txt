cmake_minimum_required(VERSION 3.12.4)

project(pong)

include_directories(include)

file(GLOB SOURCES "src/glad.c" "src/*.cpp")

add_executable(pong ${SOURCES})

# to generate compile_commands.json file
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# C flags
set(CMAKE_CXX_FLAGS "-Wall -pedantic -Werror -std=c++17")

#TODO: improve this hardcoded libraries
target_link_libraries(pong glfw)
target_link_libraries(pong GL)
target_link_libraries(pong dl)
