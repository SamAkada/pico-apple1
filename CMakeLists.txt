cmake_minimum_required(VERSION 3.13)
include(pico_sdk_import.cmake)
project(test_project)
pico_sdk_init()

add_executable(apple 
    cpu.c
)

pico_enable_stdio_usb(apple 1)
pico_enable_stdio_uart(apple 0)

pico_add_extra_outputs(apple)

target_link_libraries(apple pico_stdlib)
