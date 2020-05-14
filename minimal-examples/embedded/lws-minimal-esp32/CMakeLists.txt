cmake_minimum_required(VERSION 3.5)

if (ESP_PLATFORM)
	include($ENV{IDF_PATH}/tools/cmake/project.cmake)
	project(lws-minimal-esp32)

	target_link_libraries(lws-minimal-esp32.elf websockets)
	add_subdirectory(libwebsockets)
endif()
