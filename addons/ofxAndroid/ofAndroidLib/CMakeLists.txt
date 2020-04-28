cmake_minimum_required(VERSION 3.6.0)

project(ofAndroidLibNative VERSION 1.0)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED True)


set(ofSrcDir ../../../libs/openFrameworksCompiled/project/android)
set(ofBuildDir build/outputs/of)
file(MAKE_DIRECTORY ${ofBuildDir})

add_subdirectory(${ofSrcDir} ${ofBuildDir})

add_library(ofAndroidLibNative SHARED)


target_link_libraries( # Specifies the target library.
        ofAndroidLibNative
        # openFrameworks
        # Links the log library to the target library.
        ${log-lib} )

find_library( # Defines the name of the path variable that stores the
        # location of the NDK library.
        log-lib
        # atomic
        # android
        # OpenSLES
        # z
        # GLESv1_CM
        # GLESv2
        log
        )