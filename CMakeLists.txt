cmake_minimum_required(VERSION 3.24)
project(signalsmith-dsp VERSION 1.6.2)
set(CMAKE_CXX_STANDARD 20)

add_library(signalsmith-dsp STATIC
        ${CMAKE_CURRENT_SOURCE_DIR}/source/common.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/source/curves.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/source/delay.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/source/envelopes.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/source/fft.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/source/filters.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/source/mix.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/source/perf.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/source/rates.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/source/spectral.cpp
        ${CMAKE_CURRENT_SOURCE_DIR}/source/windows.cpp
)

add_library(signalsmith::signalsmith-dsp ALIAS signalsmith-dsp)

target_include_directories(signalsmith-dsp PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include)
