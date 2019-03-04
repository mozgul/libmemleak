cmake_minimum_required(VERSION 3.13)
project(libmemleak C)

set(CMAKE_C_STANDARD 11)

include_directories(.)
include_directories(src/include)
include_directories(src/rb_tree)

add_executable(libmemleak
        src/include/addr2line.h
        src/include/BacktraceEntry.h
        src/include/Header.h
        src/include/Interval.h
        src/include/sort.h
        src/rb_tree/misc.c
        src/rb_tree/misc.h
        src/rb_tree/red_black_tree.c
        src/rb_tree/red_black_tree.h
        src/rb_tree/stack.c
        src/rb_tree/stack.h
        src/rb_tree/test_red_black_tree.c
        src/addr2line.c
        src/memleak.c
        src/memleak_control.c
        src/sort.c
        config.h)
