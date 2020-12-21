cmake_minimum_required(VERSION 3.5...3.18)
project(2048
        VERSION 0.1.0
        LANGUAGES CXX)

set(CMAKE_CXX_COMPILER_VERSION 17)

add_executable(2048 2048.cpp)
add_executable(2048_rp 2048_rp.cpp)

if ("${CMAKE_BUILD_TYPE}" STREQUAL "Debug")
    target_compile_options(2048 PRIVATE -Wall -Wextra -pedantic -fsanitize=address,leak,undefined)
    target_link_options(2048 PRIVATE -fsanitize=address,leak,undefined)

    target_compile_options(2048_rp PRIVATE -Wall -Wextra -pedantic -fsanitize=address,leak,undefined)
    target_link_options(2048_rp PRIVATE -fsanitize=address,leak,undefined)
endif ()
