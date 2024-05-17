cmake_minimum_required(VERSION 3.5)

set(PROJ_NAME solgame)
project(${PROJ_NAME} LANGUAGES C)

set(CMAKE_C_STANDARD 99)

include_directories(.)

file(GLOB_RECURSE HEADERS "./**.h")
file(GLOB_RECURSE SRC_FILES "./**.c")

source_group("Headers" FILES ${HEADERS})
source_group("Sources" FILES ${SRC_FILES})

add_executable(
    ${PROJ_NAME}
    ${SRC_FILES}
)