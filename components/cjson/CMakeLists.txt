set(COMPONENT_SRCDIRS cJSON)
set(COMPONENT_ADD_INCLUDEDIRS cJSON)

set(COMPONENT_REQUIRES newlib)

register_component()

if(CONFIG_NEWLIB_LIBRARY_LEVEL_NORMAL)
target_compile_definitions(${COMPONENT_NAME} PRIVATE -D CJSON_SPRINTF_FLOAT=1)
endif()
