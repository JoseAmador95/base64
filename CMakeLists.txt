project(
    base64
    LANGUAGES C CXX
    DESCRIPTION "Base64 module from APR Util"
)

cmake_minimum_required(VERSION 3.22.1)

set(SRC_DIR ${CMAKE_CURRENT_SOURCE_DIR}/src)
set(INC_DIR ${CMAKE_CURRENT_SOURCE_DIR}/inc)

add_library(${PROJECT_NAME} ${SRC_DIR}/base64.c)
target_include_directories(${PROJECT_NAME} PUBLIC ${INC_DIR})
target_compile_options(${PROJECT_NAME}
    PUBLIC
    -Wall
    -O3
)