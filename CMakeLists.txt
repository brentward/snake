cmake_minimum_required(VERSION 3.13)

project(MY-RP6502-PROJECT C ASM)

add_subdirectory(rp6502-sdk)

add_executable(snake)
target_sources(snake PRIVATE
    src/snake.c
    src/controller.s
)
target_link_libraries(snake PRIVATE
    rp6502
)
