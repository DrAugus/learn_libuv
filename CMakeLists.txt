cmake_minimum_required(VERSION 3.21)
project(learn_libuv LANGUAGES C)

set(CMAKE_C_STANDARD 99)

include_directories(
        ${CMAKE_SOURCE_DIR}/include
)

link_directories(.)

link_libraries(uv)

add_executable(${PROJECT_NAME} main.c)

target_link_libraries(${PROJECT_NAME} uv)
