set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)

# If MS Visual Studio build with no command prompt
if (CMAKE_CXX_COMPILER_ID MATCHES "MSVC")
	set(CMAKE_EXE_LINKER_FLAGS "${CMAKE_EXE_LINKER_FLAGS} /ENTRY:mainCRTStartup /SUBSYSTEM:WINDOWS")
endif()

add_executable(myapp main.cpp)

target_link_libraries(myapp
    PRIVATE
    SDL3::SDL3
    imgui
)