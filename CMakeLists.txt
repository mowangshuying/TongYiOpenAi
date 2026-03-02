cmake_minimum_required(VERSION 3.12)
project(TongYiOpenai VERSION 1.0.0)

# set dirs
set(INCDIR include)
set(SRCDIR src)
set(LIBDIR lib)
set(BINDIR bin)

set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${LIBDIR})
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${LIBDIR})
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/${BINDIR})

set(BUILD_EXAMPLES OFF) # disable libhv examples

# src
add_subdirectory(src)
# demo
add_subdirectory(demo)
# 3rd party
add_subdirectory(3rdparty/libhv)


