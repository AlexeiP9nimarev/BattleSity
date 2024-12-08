cmake_minimum_required(VERSION 3.31.2 FATAL_ERROR)

set(PROJECT_NAME BattleSity)

project(${PROJECT_NAME})
add_executable(${PROJECT_NAME} src/main.cpp)
set(GLEW_BUILD_DOCS OFF CACHE BOOL "" FORECE)
set(GLEW_BUILD_TESTS OFF CACHE BOOL "" FORECE)
set(GLEW_BUILD_EXAMPLES OFF CACHE BOOL "" FORECE)
set(GLEW_INSTALL OFF CACHE BOOL "" FORECE)

add_subdirectory(external/glfw)
target_link_libraries(${PROJECT_NAME} glfw)

add_subdirectory(external/glad)
target_link_libraries(${PROJECT_NAME} glad)