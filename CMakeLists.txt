cmake_minimum_required(VERSION 3.1)
project(game.libretro.pocketsnes)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-pocketsnes REQUIRED)

set(DEPLIBS pocketsnes)
set(POCKETSNES_CUSTOM_BINARY ${POCKETSNES_LIB}
                             ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} POCKETSNES DEPLIBS)
