cmake_minimum_required(VERSION 3.1)
project(example)

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_CURRENT_SOURCE_DIR}/cmake)

# libigl

find_package(LIBIGL REQUIRED QUIET)

# Add your project files
file(GLOB SRCFILES *.cpp)
add_executable(${PROJECT_NAME}_bin ${SRCFILES})
target_link_libraries(${PROJECT_NAME}_bin igl::core)
