add_executable(main Main.cpp)
set_target_properties(main PROPERTIES OUTPUT_NAME CityBuilder)
set_target_properties(main PROPERTIES RUNTIME_OUTPUT_DIRECTORY "${CB_BIN_DIR}")
target_include_directories(main PRIVATE ${STB_SOURCE_DIR} ${DXC_INCLUDE_DIR})
target_link_directories(main PRIVATE ${DXC_LIB_DIR})
target_link_libraries(main PRIVATE core gfx glfw imgui vulkangfx dxcompiler)