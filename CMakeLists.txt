cmake_minimum_required(VERSION 3.23)
project(app)

set(CMAKE_CXX_STANDARD 14)

add_subdirectory(dependencies/glfw/)
add_subdirectory(dependencies/imgui/)

add_executable(app main.cpp)

target_link_libraries(app PRIVATE glfw)
target_include_directories(app PRIVATE dependencies/glfw/include/GLFW/)

target_link_libraries(app PRIVATE imgui)
target_include_directories(app PRIVATE dependencies/imgui/imgui/)
target_include_directories(app PRIVATE dependencies/imgui/imgui/backends/)

target_link_libraries(app PRIVATE opengl32)