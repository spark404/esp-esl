idf_build_get_property(target IDF_TARGET)
if(NOT ${target} STREQUAL "esp32c6")
    message( FATAL_ERROR "Target ${target} not supported by esp-esl, CMake will exit." )
endif()

idf_component_register(SRCS "esp-esl.c"
                    INCLUDE_DIRS "include")
