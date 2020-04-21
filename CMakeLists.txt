cmake_minimum_required(VERSION 3.14)

project(stb)

set(STB_CORE_PATH ${PROJECT_SOURCE_DIR})

set(STB_SOURCES
    ${STB_CORE_PATH}/stb_image.h
    ${STB_CORE_PATH}/stb_image_write.h
    ${STB_CORE_PATH}/stb.c
)

add_library(stb STATIC ${STB_SOURCES})
target_include_directories(stb PUBLIC ${STB_CORE_PATH})