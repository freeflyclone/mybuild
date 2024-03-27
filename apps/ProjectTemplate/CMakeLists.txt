cmake_minimum_required(VERSION 3.22)
set(APP ProjectTemplate)

set(SRCS ${CMAKE_CURRENT_SOURCE_DIR}/src)
set(INCS ${CMAKE_CURRENT_SOURCE_DIR}/inc)

set(SOURCES
	${SRCS}/ProjectTemplate.cpp
)

# declare a target named ${LIB} with ${SRCS}
# (must be done before setting properties on the target)
add_executable(${APP} ${SOURCES})

set_target_properties(${APP} PROPERTIES LINKER_LANGUAGE CXX)
target_include_directories(${APP} PUBLIC ${INCS} ${XCLASS_INCLUDE_DIRECTORIES})
target_link_libraries(${APP} xclass)
