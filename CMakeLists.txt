cmake_minimum_required(VERSION 3.15)
project(minimal_cpp_conan)

# Set C++ standard
set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)

# Find dependencies from Conan
find_package(fmt REQUIRED)

# Add source
add_executable(main src/main.cpp)

# Link libraries
target_link_libraries(main PRIVATE fmt::fmt)
