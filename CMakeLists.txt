cmake_minimum_required(VERSION 3.5)

project(kostka LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(kostka src/main.cpp)
add_library(glad extern/glad/src/glad.cpp)

include_directories(extern/glad/include extern/glm)

target_link_libraries(kostka glad glfw)
