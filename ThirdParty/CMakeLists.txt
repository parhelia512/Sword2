
cmake_minimum_required(VERSION 3.6.0)

add_subdirectory(Lua)

add_subdirectory(zlib)

add_subdirectory(SDL2)

add_subdirectory(SDL2/src/hidapi)

link_directories(${CMAKE_CURRENT_BINARY_DIR}/zlib/Debug)

add_subdirectory(SDL2_image)


add_subdirectory(freetype)

if(WIN32)
    link_directories(${CMAKE_CURRENT_BINARY_DIR}/SDL2/Debug)
    link_directories(${CMAKE_CURRENT_BINARY_DIR}/freetype/Debug)
endif()

add_subdirectory(SDL2_ttf)