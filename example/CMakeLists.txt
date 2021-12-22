cmake_minimum_required(VERSION 3.0.0)
project(example C)

# variables
set(SRCS example.c)
set(TARGET example)
set(HEADER_DIRS ../include)
set(LIB_DIRS ../build/lib)
set(LIBS getoptnano)


set(EXECUTABLE_OUTPUT_PATH ${CMAKE_BINARY_DIR}/example)

# add include directory
include_directories(${HEADERS})

# add library directory
link_directories(${HEADERS})

# target
add_executable(${TARGET} ${SRCS})

# link target (write after 'add_executable')
target_link_libraries(${TARGET} ${LIBS})
