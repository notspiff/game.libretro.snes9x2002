cmake_minimum_required(VERSION 3.1)
project(game.libretro.snes9x2002)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-snes9x2002 REQUIRED)

set(SNES9X2002_CUSTOM_BINARY ${SNES9X2002_LIB}
    ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} SNES9X2002 "")
