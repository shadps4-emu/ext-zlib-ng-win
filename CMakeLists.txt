add_library(zlib SHARED IMPORTED GLOBAL)

if(CMAKE_BUILD_TYPE STREQUAL "Debug")
    set_target_properties(zlib PROPERTIES IMPORTED_IMPLIB "${CMAKE_CURRENT_SOURCE_DIR}/lib/zlib-ngd.lib")
else()
    set_target_properties(zlib PROPERTIES IMPORTED_IMPLIB "${CMAKE_CURRENT_SOURCE_DIR}/lib/zlib-ng.lib")
endif()