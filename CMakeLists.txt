cmake_minimum_required(VERSION 3.10)

# Project name and version
project(CEForth VERSION 1.0)

# Set C++ standard
set(CMAKE_CXX_STANDARD 23)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Compilation flags
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -O2 -Wall -fomit-frame-pointer -fno-stack-check -fno-stack-protector")

# Include directories
include_directories(src)

# Source files
set(SOURCES
    platform/main.cpp
    src/ceforth.cpp
)

# Executable targets
add_executable(cppforth ${SOURCES})
