cmake_minimum_required(VERSION 3.5)

set(PROJ_NAME SOLGame)
set(PROJ_SOURCE_ROOT ${PROJECT_SOURCE_DIR})

project(${PROJ_NAME} LANGUAGES C)

set(CMAKE_C_STANDARD 99)
set(CMAKE_FIND_FRAMEWORK LAST)

# Add include
include_directories(./libs)
include_directories(./libs/sokol)

# Config Sokol
add_definitions(-DSOKOL_IMPL)
# check if is windows
if(WIN32)
    add_definitions(-DSOKOL_D3D11)
else()
    add_definitions(-DSOKOL_GLCORE)
endif()


add_subdirectory(./src)