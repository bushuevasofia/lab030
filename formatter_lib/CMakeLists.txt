cmake_minimum_required(VERSION 3.5)

# Указываем на подпроект
project(formatter LANGUAGES CXX VERSION 1.0)

if(NOT TARGET formatter)
    add_library(formatter STATIC formatter.cpp)
    target_include_directories(formatter PUBLIC 
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}>
    )
endif()
