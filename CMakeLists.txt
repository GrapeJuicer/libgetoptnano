cmake_minimum_required(VERSION 3.0.0)
project(libgetoptnano C)

# sources
set(SRCS
    src/libgetoptnano.c
)

# target
set(TARGET getoptnano)

# set output lib output dir to '[build]/lib'
set(LIBRARY_OUTPUT_PATH "${CMAKE_BINARY_DIR}/lib")

# target
add_library(${TARGET} ${SRCS})

# header location
target_include_directories(${TARGET} PUBLIC ${PROJECT_SOURCE_DIR}/include)

add_subdirectory(example)
