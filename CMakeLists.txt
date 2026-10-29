cmake_minimum_required(VERSION 3.16)
project(Minecraft-CPP CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

find_package(glfw3 REQUIRED)
find_package(glm REQUIRED)
find_package(OpenGL REQUIRED)

add_executable(minecraft-cpp src/main.cpp)

target_link_libraries(minecraft-cpp PRIVATE glfw glm::glm OpenGL::GL)
target_compile_options(minecraft-cpp PRIVATE -Wall -Wextra)