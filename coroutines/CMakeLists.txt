cmake_minimum_required(VERSION 3.22)
project(coroutines)

find_package(fmt)
find_package(spdlog)
# find_package(http_parser)

# add_library(coroutines STATIC)
# add_library(aifs STATIC src/event_loop.cpp src/http/response.cpp)
# target_include_directories(aifs PUBLIC include)
# target_link_libraries(coroutines PUBLIC fmt::fmt spdlog::spdlog)
# target_compile_features(coroutines PUBLIC cxx_std_20)

add_executable(simple_example examples/main.cpp)
target_link_libraries(simple_example PUBLIC fmt::fmt spdlog::spdlog)
# target_link_libraries(simple_example PRIVATE coroutines)