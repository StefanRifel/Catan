cmake_minimum_required(VERSION 3.27)
project(Catan)

set(CMAKE_CXX_STANDARD 11)

include(FetchContent)
set(BUILD_SHARED_LIBS OFF)
FetchContent_Declare(SFML GIT_REPOSITORY https://github.com/SFML/SFML.git GIT_TAG 2.5.1)
FetchContent_MakeAvailable(SFML)

add_executable(Catan src/main.cpp)

target_link_libraries(Catan sfml-graphics)
