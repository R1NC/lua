cmake_minimum_required(VERSION 3.6.0)

if(IOS)
    add_definitions(-DLUA_USE_IOS)
endif()

set(LUA_SOURCES
        lapi.c
        lauxlib.c
        lbaselib.c
        lcode.c
        lcorolib.c
        lctype.c
        ldblib.c
        ldebug.c
        ldo.c
        ldump.c
        lfunc.c
        lgc.c
        linit.c
        liolib.c
        llex.c
        lmathlib.c
        lmem.c
        loadlib.c
        lobject.c
        lopcodes.c
        loslib.c
        lparser.c
        lstate.c
        lstring.c
        lstrlib.c
        ltable.c
        ltablib.c
        ltm.c
        lua.c
        lundump.c
        lutf8lib.c
        lvm.c
        lzio.c
)

add_library(lua STATIC ${LUA_SOURCES})

set_target_properties(
        lua
        PROPERTIES
        LIBRARY_OUTPUT_DIRECTORY
        "${CMAKE_RUNTIME_OUTPUT_DIRECTORY}"
)
