cmake_minimum_required(VERSION 3.10)

# Set the project name
project(VecTest)

# Add Google Test (installed via Homebrew)
find_package(GTest REQUIRED)
include_directories(${GTEST_INCLUDE_DIRS})

# Add source files
set(SOURCE_FILES main.cpp)  # Replace with your actual source files

# Add the test executable
add_executable(VecTest ${SOURCE_FILES} vec_tests.cpp)

# Link Google Test and pthread
target_link_libraries(VecTest ${GTEST_LIBRARIES} pthread)