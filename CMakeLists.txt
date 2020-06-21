cmake_minimum_required(VERSION 3.17)

project(no-runtime
    VERSION 1.0
    DESCRIPTION "Example CMakeLists.txt file for building C++ projects/files without MSVC C++ runtime."
    HOMEPAGE_URL "https://github.com/RIscRIpt/no-runtime"
)

add_executable(no-runtime main.cpp)

target_compile_options(
    no-runtime PRIVATE
    "/GS-"
)

target_link_options(
    no-runtime PRIVATE
    "/ENTRY:main" "/NODEFAULTLIB"
)
