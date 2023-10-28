cmake_minimum_required(VERSION 3.22)

include(CheckSymbolExists)

add_library(vrEmu6502
    STATIC
    vrEmu6502.c
    vrEmu6502.h)

target_compile_definitions(vrEmu6502 PUBLIC VR_EMU_6502_STATIC)
target_include_directories (vrEmu6502 INTERFACE ${CMAKE_CURRENT_SOURCE_DIR})
target_compile_features(vrEmu6502 PUBLIC c_std_11)
