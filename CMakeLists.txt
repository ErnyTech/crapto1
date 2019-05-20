cmake_minimum_required(VERSION 2.8.12)
set (CMAKE_CXX_STANDARD 89)
set(CMAKE_C_FLAGS "-Wall -pedantic -Wextra -Werror")
project(crapto1)
include_directories(.)

file(GLOB SOURCES "*.c")
add_library(${PROJECT_NAME} SHARED ${SOURCES})

install(TARGETS ${PROJECT_NAME}
        LIBRARY DESTINATION lib
)

INSTALL(FILES ${HEADERS}
        DESTINATION include
)
