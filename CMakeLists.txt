cmake_minimum_required (VERSION 3.8)

project(libutil)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_STATIC_LIBRARY_PREFIX "")

include(${CMAKE_SOURCE_DIR}/cmake/SetEnv.cmake)

include_directories($CMAKE_SOURCE_DIR/lib)

set(HEADERS
    ${CMAKE_SOURCE_DIR}/libutil/random/generator.hpp
    ${CMAKE_SOURCE_DIR}/libutil/random/entry.hpp
    ${CMAKE_SOURCE_DIR}/libutil/random/string.hpp
)

set(SOURCES
    ${CMAKE_SOURCE_DIR}/libutil/random/string.cpp
)

include(${CMAKE_SOURCE_DIR}/cmake/LibraryConfig.cmake)

include(${CMAKE_SOURCE_DIR}/cmake/InstallConfig.cmake)