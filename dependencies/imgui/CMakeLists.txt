project(imgui)

file(GLOB SOURCE_FILES imgui/*.cpp)

#add_library(imgui STATIC ${SOURCE_FILES})

add_library(imgui STATIC
    ${SOURCE_FILES}
    imgui/backends/imgui_impl_glfw.cpp
    imgui/backends/imgui_impl_opengl3.cpp
)
target_link_libraries(imgui glfw)
target_include_directories(imgui PRIVATE
    imgui/
    imgui/backends/
)