cmake_minimum_required(VERSION 3.8.2)

set(BOARD stm32_10g_primer)
set(BOARD_ROOT ${CMAKE_CURRENT_LIST_DIR})

include($ENV{ZENOS_BASE}/cmake/app.cmake)

project(rtfm)

target_sources(app PRIVATE src/main.c)
target_link_libraries(app PUBLIC micropython)