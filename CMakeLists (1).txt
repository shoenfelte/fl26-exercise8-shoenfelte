cmake_minimum_required(VERSION 3.16)
project(Exercise8 CXX)

set(CMAKE_AUTOMOC ON)
set(CMAKE_INCLUDE_CURRENT_DIR ON)

# Find Qt6 Widgets module automatically
find_package(Qt6Widgets REQUIRED)

# --- hello_static target ---
add_executable(hello_static hello_static.cpp)
target_link_libraries(hello_static Qt6::Widgets)

# --- hello_label target ---
add_executable(hello_label
    hello_label.cpp
    label_printer.cpp
    label_printer.h
)
target_link_libraries(hello_label Qt6::Widgets)
