
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -DCDSUNIT_USE_URCU")

add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/delodd)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/del3)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/insdel_find)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/insdel_func)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/insdel_string)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/iteration)
add_subdirectory(${CMAKE_CURRENT_SOURCE_DIR}/iter_erase)

add_custom_target( stress-set
    DEPENDS
        stress-set-delodd
        stress-set-del3
        stress-set-insdelfind
        stress-set-insdel-func
        stress-set-insdel-string
        stress-set-iteration
        stress-set-iter-erase
)
