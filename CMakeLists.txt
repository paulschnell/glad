cmake_minimum_required(VERSION 3.27.0 FATAL_ERROR)

project(glad VERSION 0.1.36 LANGUAGES C)

set(CMAKE_C_STANDARD 17)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_C_STANDARD_REQUIRED ON)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

file(GLOB SOURCE_FILES include/glad/glad.h include/KHR/khrplatform.h src/glad.c)

add_library(glad ${SOURCE_FILES})

target_include_directories(glad PUBLIC include/)
