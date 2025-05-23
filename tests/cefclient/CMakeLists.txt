# Copyright (c) 2014 The Chromium Embedded Framework Authors. All rights
# reserved. Use of this source code is governed by a BSD-style license that
# can be found in the LICENSE file.

#
# Source files.
#

# cefclient browser sources.
set(CEFCLIENT_BROWSER_BROWSER_SRCS
  browser/binding_test.cc
  browser/binding_test.h
  browser/browser_window.cc
  browser/browser_window.h
  browser/bytes_write_handler.cc
  browser/bytes_write_handler.h
  browser/client_app_delegates_browser.cc
  browser/client_browser.cc
  browser/client_browser.h
  browser/client_handler.cc
  browser/client_handler.h
  browser/client_handler_osr.cc
  browser/client_handler_osr.h
  browser/client_handler_std.cc
  browser/client_handler_std.h
  browser/client_types.h
  browser/dialog_test.cc
  browser/dialog_test.h
  browser/drm_test.cc
  browser/drm_test.h
  browser/image_cache.cc
  browser/image_cache.h
  browser/main_context.cc
  browser/main_context.h
  browser/main_context_impl.cc
  browser/main_context_impl.h
  browser/media_router_test.cc
  browser/media_router_test.h
  browser/osr_dragdrop_events.h
  browser/osr_renderer.cc
  browser/osr_renderer.h
  browser/osr_renderer_settings.h
  browser/preferences_test.cc
  browser/preferences_test.h
  browser/resource.h
  browser/response_filter_test.cc
  browser/response_filter_test.h
  browser/root_window.cc
  browser/root_window.h
  browser/root_window_create.cc
  browser/root_window_manager.cc
  browser/root_window_manager.h
  browser/scheme_test.cc
  browser/scheme_test.h
  browser/server_test.cc
  browser/server_test.h
  browser/temp_window.h
  browser/test_runner.cc
  browser/test_runner.h
  browser/urlrequest_test.cc
  browser/urlrequest_test.h
  browser/window_test.cc
  browser/window_test.h
  browser/window_test_runner.cc
  browser/window_test_runner.h
  )
source_group(cefclient\\\\browser FILES ${CEFCLIENT_BROWSER_BROWSER_SRCS})

set(CEFCLIENT_BROWSER_SHARED_BROWSER_SRCS
  ../shared/browser/client_app_browser.cc
  ../shared/browser/client_app_browser.h
  ../shared/browser/extension_util.cc
  ../shared/browser/extension_util.h
  ../shared/browser/file_util.cc
  ../shared/browser/file_util.h
  ../shared/browser/geometry_util.cc
  ../shared/browser/geometry_util.h
  ../shared/browser/main_message_loop.cc
  ../shared/browser/main_message_loop.h
  ../shared/browser/main_message_loop_external_pump.cc
  ../shared/browser/main_message_loop_external_pump.h
  ../shared/browser/main_message_loop_std.cc
  ../shared/browser/main_message_loop_std.h
  ../shared/browser/resource_util.h
  )
source_group(shared\\\\browser FILES ${CEFCLIENT_BROWSER_SHARED_BROWSER_SRCS})

set(CEFCLIENT_BROWSER_SRCS
  ${CEFCLIENT_BROWSER_BROWSER_SRCS}
  ${CEFCLIENT_BROWSER_SHARED_BROWSER_SRCS}
  )

# cefclient common sources.
set(CEFCLIENT_COMMON_COMMON_SRCS
  common/client_app_delegates_common.cc
  common/scheme_test_common.cc
  common/scheme_test_common.h
  )
source_group(cefclient\\\\common FILES ${CEFCLIENT_COMMON_COMMON_SRCS})

set(CEFCLIENT_COMMON_SHARED_COMMON_SRCS
  ../shared/common/client_app.cc
  ../shared/common/client_app.h
  ../shared/common/client_app_other.cc
  ../shared/common/client_app_other.h
  ../shared/common/client_switches.cc
  ../shared/common/client_switches.h
  )
source_group(shared\\\\common FILES ${CEFCLIENT_COMMON_SHARED_COMMON_SRCS})

set(CEFCLIENT_COMMON_SRCS
  ${CEFCLIENT_COMMON_COMMON_SRCS}
  ${CEFCLIENT_COMMON_SHARED_COMMON_SRCS}
  )

# cefclient renderer sources.
set(CEFCLIENT_RENDERER_RENDERER_SRCS
  renderer/client_app_delegates_renderer.cc
  renderer/client_renderer.cc
  renderer/client_renderer.h
  renderer/performance_test.cc
  renderer/performance_test.h
  renderer/performance_test_setup.h
  renderer/performance_test_tests.cc
  )
source_group(cefclient\\\\renderer FILES ${CEFCLIENT_RENDERER_RENDERER_SRCS})

set(CEFCLIENT_RENDERER_SHARED_RENDERER_SRCS
  ../shared/renderer/client_app_renderer.cc
  ../shared/renderer/client_app_renderer.h
  )
source_group(shared\\\\renderer FILES ${CEFCLIENT_RENDERER_SHARED_RENDERER_SRCS})

set(CEFCLIENT_RENDERER_SRCS
  ${CEFCLIENT_RENDERER_RENDERER_SRCS}
  ${CEFCLIENT_RENDERER_SHARED_RENDERER_SRCS}
  )

#cefclient Linux sources
set(CEFCLIENT_LINUX_SRCS
  cefclient_gtk.cc
  )
source_group(cefclient FILES ${CEFCLIENT_LINUX_SRCS})

set(CEFCLIENT_LINUX_BROWSER_SRCS
  browser/browser_window_osr_gtk.cc
  browser/browser_window_osr_gtk.h
  browser/browser_window_std_gtk.cc
  browser/browser_window_std_gtk.h
  browser/dialog_handler_gtk.cc
  browser/dialog_handler_gtk.h
  browser/main_context_impl_posix.cc
  browser/main_message_loop_multithreaded_gtk.cc
  browser/main_message_loop_multithreaded_gtk.h
  browser/print_handler_gtk.cc
  browser/print_handler_gtk.h
  browser/resource_util_linux.cc
  browser/root_window_gtk.cc
  browser/root_window_gtk.h
  browser/root_window_views.cc
  browser/root_window_views.h
  browser/temp_window_x11.cc
  browser/temp_window_x11.h
  browser/util_gtk.cc
  browser/util_gtk.h
  browser/views_menu_bar.cc
  browser/views_menu_bar.h
  browser/views_style.cc
  browser/views_style.h
  browser/views_window.cc
  browser/views_window.h
  browser/window_test_runner_gtk.cc
  browser/window_test_runner_gtk.h
  browser/window_test_runner_views.cc
  browser/window_test_runner_views.h
  )
source_group(cefclient\\\\browser FILES ${CEFCLIENT_LINUX_BROWSER_SRCS})

set(CEFCLIENT_LINUX_SHARED_BROWSER_SRCS
  ../shared/browser/main_message_loop_external_pump_linux.cc
  ../shared/browser/resource_util_posix.cc
  )
source_group(shared\\\\browser FILES ${CEFCLIENT_LINUX_SHARED_BROWSER_SRCS})

set(CEFCLIENT_LINUX_SRCS
  ${CEFCLIENT_LINUX_SRCS}
  ${CEFCLIENT_LINUX_BROWSER_SRCS}
  ${CEFCLIENT_LINUX_SHARED_BROWSER_SRCS}
  )

#cefclient Mac OS X sources
set(CEFCLIENT_MACOSX_SRCS
  cefclient_mac.mm
  )
source_group(cefclient FILES ${CEFCLIENT_MACOSX_SRCS})

set(CEFCLIENT_MACOSX_BROWSER_SRCS
  browser/browser_window_osr_mac.h
  browser/browser_window_osr_mac.mm
  browser/browser_window_std_mac.h
  browser/browser_window_std_mac.mm
  browser/main_context_impl_posix.cc
  browser/osr_accessibility_helper.cc
  browser/osr_accessibility_helper.h
  browser/osr_accessibility_node.cc
  browser/osr_accessibility_node.h
  browser/osr_accessibility_node_mac.mm
  browser/root_window_mac.h
  browser/root_window_mac.mm
  browser/temp_window_mac.h
  browser/temp_window_mac.mm
  browser/text_input_client_osr_mac.h
  browser/text_input_client_osr_mac.mm
  browser/window_test_runner_mac.h
  browser/window_test_runner_mac.mm
  )
source_group(cefclient\\\\browser FILES ${CEFCLIENT_MACOSX_BROWSER_SRCS})

set(CEFCLIENT_MACOSX_SHARED_BROWSER_SRCS
  ../shared/browser/main_message_loop_external_pump_mac.mm
  ../shared/browser/resource_util_mac.mm
  ../shared/browser/resource_util_posix.cc
  )
source_group(shared\\\\browser FILES ${CEFCLIENT_MACOSX_SHARED_BROWSER_SRCS})

set(CEFCLIENT_MAC_SRCS
  ${CEFCLIENT_MACOSX_SRCS}
  ${CEFCLIENT_MACOSX_BROWSER_SRCS}
  ${CEFCLIENT_MACOSX_SHARED_BROWSER_SRCS}
  )

# cefclient Mac OS X helper sources.
set(CEFCLIENT_HELPER_SHARED_SRCS
  ../shared/process_helper_mac.cc
  )
source_group(shared FILES ${CEFCLIENT_HELPER_SHARED_SRCS})

set(CEFCLIENT_MAC_HELPER_SRCS
  ${CEFCLIENT_HELPER_SHARED_SRCS}
  )

#cefclient Windows sources
set(CEFCLIENT_WINDOWS_SRCS
  cefclient_win.cc
  )
source_group(cefclient FILES ${CEFCLIENT_WINDOWS_SRCS})

set(CEFCLIENT_WINDOWS_BROWSER_SRCS
  browser/browser_window_osr_win.cc
  browser/browser_window_osr_win.h
  browser/browser_window_std_win.cc
  browser/browser_window_std_win.h
  browser/main_context_impl_win.cc
  browser/main_message_loop_multithreaded_win.cc
  browser/main_message_loop_multithreaded_win.h
  browser/osr_accessibility_helper.cc
  browser/osr_accessibility_helper.h
  browser/osr_accessibility_node.cc
  browser/osr_accessibility_node.h
  browser/osr_accessibility_node_win.cc
  browser/osr_d3d11_win.cc
  browser/osr_d3d11_win.h
  browser/osr_dragdrop_win.cc
  browser/osr_dragdrop_win.h
  browser/osr_ime_handler_win.cc
  browser/osr_ime_handler_win.h
  browser/osr_render_handler_win.cc
  browser/osr_render_handler_win.h
  browser/osr_render_handler_win_d3d11.cc
  browser/osr_render_handler_win_d3d11.h
  browser/osr_render_handler_win_gl.cc
  browser/osr_render_handler_win_gl.h
  browser/osr_window_win.cc
  browser/osr_window_win.h
  browser/resource_util_win_idmap.cc
  browser/root_window_views.cc
  browser/root_window_views.h
  browser/root_window_win.cc
  browser/root_window_win.h
  browser/temp_window_win.cc
  browser/temp_window_win.h
  browser/views_menu_bar.cc
  browser/views_menu_bar.h
  browser/views_style.cc
  browser/views_style.h
  browser/views_window.cc
  browser/views_window.h
  browser/window_test_runner_views.cc
  browser/window_test_runner_views.h
  browser/window_test_runner_win.cc
  browser/window_test_runner_win.h
  )
source_group(cefclient\\\\browser FILES ${CEFCLIENT_WINDOWS_BROWSER_SRCS})

set(CEFCLIENT_WINDOWS_RESOURCES_WIN_SRCS
  resources/win/cefclient.rc
  )
source_group(cefclient\\\\resources\\\\win FILES ${CEFCLIENT_WINDOWS_RESOURCES_WIN_SRCS})

set(CEFCLIENT_WINDOWS_SHARED_BROWSER_SRCS
  ../shared/browser/main_message_loop_external_pump_win.cc
  ../shared/browser/resource_util_win.cc
  ../shared/browser/util_win.cc
  ../shared/browser/util_win.h
  )
source_group(shared\\\\browser FILES ${CEFCLIENT_WINDOWS_SHARED_BROWSER_SRCS})

set(CEFCLIENT_WINDOWS_SRCS
  ${CEFCLIENT_WINDOWS_SRCS}
  ${CEFCLIENT_WINDOWS_BROWSER_SRCS}
  ${CEFCLIENT_WINDOWS_RESOURCES_WIN_SRCS}
  ${CEFCLIENT_WINDOWS_SHARED_BROWSER_SRCS}
  )

# cefclient resources.
set(CEFCLIENT_RESOURCES_RESOURCES_SRCS
  resources/binding.html
  resources/dialogs.html
  resources/draggable.html
  resources/drm.html
  resources/localstorage.html
  resources/logo.png
  resources/media_router.html
  resources/menu_icon.1x.png
  resources/menu_icon.2x.png
  resources/other_tests.html
  resources/performance.html
  resources/performance2.html
  resources/preferences.html
  resources/response_filter.html
  resources/server.html
  resources/transparency.html
  resources/urlrequest.html
  resources/websocket.html
  resources/window.html
  resources/xmlhttprequest.html
  )
source_group(cefclient\\\\resources FILES ${CEFCLIENT_RESOURCES_RESOURCES_SRCS})

set(CEFCLIENT_RESOURCES_RESOURCES_EXTENSIONS_SET_PAGE_COLOR_SRCS
  resources/extensions/set_page_color/README.md
  resources/extensions/set_page_color/icon.png
  resources/extensions/set_page_color/manifest.json
  resources/extensions/set_page_color/popup.html
  resources/extensions/set_page_color/popup.js
  )
source_group(cefclient\\\\resources\\\\extensions\\\\set_page_color FILES ${CEFCLIENT_RESOURCES_RESOURCES_EXTENSIONS_SET_PAGE_COLOR_SRCS})

set(CEFCLIENT_RESOURCES_RESOURCES_MAC_SRCS_MAC
  resources/mac/Info.plist
  resources/mac/cefclient.icns
  )
APPEND_PLATFORM_SOURCES(CEFCLIENT_RESOURCES_RESOURCES_MAC_SRCS)
source_group(cefclient\\\\resources\\\\mac FILES ${CEFCLIENT_RESOURCES_RESOURCES_MAC_SRCS})

set(CEFCLIENT_RESOURCES_RESOURCES_MAC_ENGLISH_LPROJ_SRCS_MAC
  resources/mac/English.lproj/InfoPlist.strings
  resources/mac/English.lproj/MainMenu.xib
  )
APPEND_PLATFORM_SOURCES(CEFCLIENT_RESOURCES_RESOURCES_MAC_ENGLISH_LPROJ_SRCS)
source_group(cefclient\\\\resources\\\\mac\\\\English.lproj FILES ${CEFCLIENT_RESOURCES_RESOURCES_MAC_ENGLISH_LPROJ_SRCS})

set(CEFCLIENT_RESOURCES_SHARED_RESOURCES_SRCS
  ../shared/resources/osr_test.html
  ../shared/resources/pdf.html
  ../shared/resources/pdf.pdf
  ../shared/resources/window_icon.1x.png
  ../shared/resources/window_icon.2x.png
  )
source_group(shared\\\\resources FILES ${CEFCLIENT_RESOURCES_SHARED_RESOURCES_SRCS})

set(CEFCLIENT_RESOURCES_SRCS
  ${CEFCLIENT_RESOURCES_RESOURCES_SRCS}
  ${CEFCLIENT_RESOURCES_RESOURCES_EXTENSIONS_SET_PAGE_COLOR_SRCS}
  ${CEFCLIENT_RESOURCES_RESOURCES_MAC_SRCS}
  ${CEFCLIENT_RESOURCES_RESOURCES_MAC_ENGLISH_LPROJ_SRCS}
  ${CEFCLIENT_RESOURCES_SHARED_RESOURCES_SRCS}
  )


#
# Shared configuration.
#

# Target executable names.
set(CEF_TARGET "cefclient")
if(OS_MAC)
  set(CEF_HELPER_TARGET "cefclient_Helper")
  set(CEF_HELPER_OUTPUT_NAME "cefclient Helper")
else()
  # Logical target used to link the libcef library.
  ADD_LOGICAL_TARGET("libcef_lib" "${CEF_LIB_DEBUG}" "${CEF_LIB_RELEASE}")
endif()

# Determine the target output directory.
SET_CEF_TARGET_OUT_DIR()


#
# Linux configuration.
#

if(OS_LINUX)
  # All sources required by the "cefclient" target. Generates an executable that
  # is used for all processes.
  set(CEFCLIENT_SRCS
    ${CEFCLIENT_BROWSER_SRCS}
    ${CEFCLIENT_COMMON_SRCS}
    ${CEFCLIENT_RENDERER_SRCS}
    ${CEFCLIENT_RESOURCES_SRCS}
    ${CEFCLIENT_LINUX_SRCS}
    )

  # Find required libraries and update compiler/linker variables.
  FIND_LINUX_LIBRARIES("gmodule-2.0 gtk+-2.0 gthread-2.0 gtk+-unix-print-2.0 gtkglext-1.0 xi")

  # Executable target.
  add_executable(${CEF_TARGET} ${CEFCLIENT_SRCS})
  SET_EXECUTABLE_TARGET_PROPERTIES(${CEF_TARGET})
  add_dependencies(${CEF_TARGET} libcef_dll_wrapper)
  target_link_libraries(${CEF_TARGET} libcef_lib libcef_dll_wrapper ${CEF_STANDARD_LIBS})

  # Set rpath so that libraries can be placed next to the executable.
  set_target_properties(${CEF_TARGET} PROPERTIES INSTALL_RPATH "$ORIGIN")
  set_target_properties(${CEF_TARGET} PROPERTIES BUILD_WITH_INSTALL_RPATH TRUE)
  set_target_properties(${CEF_TARGET} PROPERTIES RUNTIME_OUTPUT_DIRECTORY ${CEF_TARGET_OUT_DIR})

  # We don't call deprecated GTK functions, and they can cause build failures, so disable them.
  add_definitions("-DGTK_DISABLE_DEPRECATED")

  # Copy CEF binary and resource files to the target output directory.
  COPY_FILES("${CEF_TARGET}" "${CEF_BINARY_FILES}" "${CEF_BINARY_DIR}" "${CEF_TARGET_OUT_DIR}")
  COPY_FILES("${CEF_TARGET}" "${CEF_RESOURCE_FILES}" "${CEF_RESOURCE_DIR}" "${CEF_TARGET_OUT_DIR}")

  # Copy cefclient resource files to the target output directory.
  COPY_FILES("${CEF_TARGET}" "${CEFCLIENT_RESOURCES_SRCS}" "${CMAKE_CURRENT_SOURCE_DIR}" "${CEF_TARGET_OUT_DIR}/cefclient_files")

  # Set SUID permissions on the chrome-sandbox target.
  SET_LINUX_SUID_PERMISSIONS("${CEF_TARGET}" "${CEF_TARGET_OUT_DIR}/chrome-sandbox")
endif()


#
# Mac OS X configuration.
#

if(OS_MAC)
  option(OPTION_USE_ARC "Build with ARC (automatic Reference Counting) on macOS." ON)
  if(OPTION_USE_ARC)
    list(APPEND CEF_COMPILER_FLAGS
      -fobjc-arc
      )
    set_target_properties(${target} PROPERTIES
      CLANG_ENABLE_OBJC_ARC "YES"
      )
  endif()

  # All sources required by the "cefclient" target. Generates an app bundle that
  # is used only for the browser process.
  set(CEFCLIENT_SRCS
    ${CEFCLIENT_BROWSER_SRCS}
    ${CEFCLIENT_COMMON_SRCS}
    ${CEFCLIENT_RESOURCES_SRCS}
    ${CEFCLIENT_MAC_SRCS}
    )

  # All sources required by the "cefclient Helper" target. Generates an app
  # bundle that is used only for non-browser processes.
  set(CEFCLIENT_HELPER_SRCS
    ${CEFCLIENT_COMMON_SRCS}
    ${CEFCLIENT_RENDERER_SRCS}
    ${CEFCLIENT_MAC_HELPER_SRCS}
    )

  # Output path for the main app bundle.
  set(CEF_APP "${CEF_TARGET_OUT_DIR}/${CEF_TARGET}.app")

  # Variables referenced from the main Info.plist file.
  set(EXECUTABLE_NAME "${CEF_TARGET}")
  set(PRODUCT_NAME "${CEF_TARGET}")

  if(USE_SANDBOX)
    # Logical target used to link the cef_sandbox library.
    ADD_LOGICAL_TARGET("cef_sandbox_lib" "${CEF_SANDBOX_LIB_DEBUG}" "${CEF_SANDBOX_LIB_RELEASE}")
  endif()

  # Main app bundle target.
  add_executable(${CEF_TARGET} MACOSX_BUNDLE ${CEFCLIENT_RESOURCES_SRCS} ${CEFCLIENT_SRCS})
  SET_EXECUTABLE_TARGET_PROPERTIES(${CEF_TARGET})
  add_dependencies(${CEF_TARGET} libcef_dll_wrapper)
  target_link_libraries(${CEF_TARGET} libcef_dll_wrapper ${CEF_STANDARD_LIBS} "-framework OpenGL")
  set_target_properties(${CEF_TARGET} PROPERTIES
    MACOSX_BUNDLE_INFO_PLIST ${CMAKE_CURRENT_SOURCE_DIR}/resources/mac/Info.plist
    )

  # Copy the CEF framework into the Frameworks directory.
  add_custom_command(
    TARGET ${CEF_TARGET}
    POST_BUILD
    COMMAND ${CMAKE_COMMAND} -E copy_directory
            "${CEF_BINARY_DIR}/Chromium Embedded Framework.framework"
            "${CEF_APP}/Contents/Frameworks/Chromium Embedded Framework.framework"
    VERBATIM
    )

  # Create the multiple Helper app bundle targets.
  foreach(_suffix_list ${CEF_HELPER_APP_SUFFIXES})
    # Convert to a list and extract the suffix values.
    string(REPLACE ":" ";" _suffix_list ${_suffix_list})
    list(GET _suffix_list 0 _name_suffix)
    list(GET _suffix_list 1 _target_suffix)
    list(GET _suffix_list 2 _plist_suffix)

    # Define Helper target and output names.
    set(_helper_target "${CEF_HELPER_TARGET}${_target_suffix}")
    set(_helper_output_name "${CEF_HELPER_OUTPUT_NAME}${_name_suffix}")

    # Create Helper-specific variants of the helper-Info.plist file. Do this
    # manually because the configure_file command (which is executed as part of
    # MACOSX_BUNDLE_INFO_PLIST) uses global env variables and would insert the
    # wrong values with multiple targets.
    set(_helper_info_plist "${CMAKE_CURRENT_BINARY_DIR}/helper-Info${_target_suffix}.plist")
    file(READ "${CMAKE_CURRENT_SOURCE_DIR}/resources/mac/helper-Info.plist" _plist_contents)
    string(REPLACE "\${EXECUTABLE_NAME}" "${_helper_output_name}" _plist_contents ${_plist_contents})
    string(REPLACE "\${PRODUCT_NAME}" "${_helper_output_name}" _plist_contents ${_plist_contents})
    string(REPLACE "\${BUNDLE_ID_SUFFIX}" "${_plist_suffix}" _plist_contents ${_plist_contents})
    file(WRITE ${_helper_info_plist} ${_plist_contents})

    # Create Helper executable target.
    add_executable(${_helper_target} MACOSX_BUNDLE ${CEFCLIENT_HELPER_SRCS})
    SET_EXECUTABLE_TARGET_PROPERTIES(${_helper_target})
    add_dependencies(${_helper_target} libcef_dll_wrapper)
    target_link_libraries(${_helper_target} libcef_dll_wrapper ${CEF_STANDARD_LIBS})
    set_target_properties(${_helper_target} PROPERTIES
      MACOSX_BUNDLE_INFO_PLIST ${_helper_info_plist}
      OUTPUT_NAME ${_helper_output_name}
      )

    if(USE_SANDBOX)
      target_link_libraries(${_helper_target} cef_sandbox_lib)
    endif()

    # Add the Helper as a dependency of the main executable target.
    add_dependencies(${CEF_TARGET} "${_helper_target}")

    # Copy the Helper app bundle into the Frameworks directory.
    add_custom_command(
      TARGET ${CEF_TARGET}
      POST_BUILD
      COMMAND ${CMAKE_COMMAND} -E copy_directory
              "${CEF_TARGET_OUT_DIR}/${_helper_output_name}.app"
              "${CEF_APP}/Contents/Frameworks/${_helper_output_name}.app"
      VERBATIM
      )
  endforeach()

  # Manually process and copy over resource files.
  # The Xcode generator can support this via the set_target_properties RESOURCE
  # directive but that doesn't properly handle nested resource directories.
  # Remove these prefixes from input file paths.
  set(PREFIXES
    "resources/mac/"
    "resources/"
    "../shared/resources/"
    )
  COPY_MAC_RESOURCES("${CEFCLIENT_RESOURCES_SRCS}" "${PREFIXES}" "${CEF_TARGET}" "${CMAKE_CURRENT_SOURCE_DIR}" "${CEF_APP}")
endif()


#
# Windows configuration.
#

if(OS_WINDOWS)
  # All sources required by the "cefclient" target. Generates an executable that
  # is used for all processes.
  set(CEFCLIENT_SRCS
    ${CEFCLIENT_BROWSER_SRCS}
    ${CEFCLIENT_COMMON_SRCS}
    ${CEFCLIENT_RENDERER_SRCS}
    ${CEFCLIENT_RESOURCES_SRCS}
    ${CEFCLIENT_WINDOWS_SRCS}
    )

  # Executable target.
  add_executable(${CEF_TARGET} WIN32 ${CEFCLIENT_SRCS})
  SET_EXECUTABLE_TARGET_PROPERTIES(${CEF_TARGET})
  add_dependencies(${CEF_TARGET} libcef_dll_wrapper)
  target_link_libraries(${CEF_TARGET} libcef_lib libcef_dll_wrapper ${CEF_STANDARD_LIBS} d3d11.lib glu32.lib imm32.lib opengl32.lib)

  if(USE_ATL)
    # Required by VS2013 to link accessibility API functions.
    target_link_libraries(${CEF_TARGET} oleacc.lib)
  endif()

  if(USE_SANDBOX)
    # Logical target used to link the cef_sandbox library.
    ADD_LOGICAL_TARGET("cef_sandbox_lib" "${CEF_SANDBOX_LIB_DEBUG}" "${CEF_SANDBOX_LIB_RELEASE}")
    target_link_libraries(${CEF_TARGET} cef_sandbox_lib ${CEF_SANDBOX_STANDARD_LIBS})
  endif()

  # Add the custom manifest files to the executable.
  ADD_WINDOWS_MANIFEST("${CMAKE_CURRENT_SOURCE_DIR}/resources/win" "${CEF_TARGET}" "exe")

  # Copy CEF binary and resource files to the target output directory.
  COPY_FILES("${CEF_TARGET}" "${CEF_BINARY_FILES}" "${CEF_BINARY_DIR}" "${CEF_TARGET_OUT_DIR}")
  COPY_FILES("${CEF_TARGET}" "${CEF_RESOURCE_FILES}" "${CEF_RESOURCE_DIR}" "${CEF_TARGET_OUT_DIR}")
  
  # Copy Flash dll binary files to the target output directory
  COPY_FILES("${CEF_TARGET}" "pepflashplayer.dll" "${CMAKE_CURRENT_SOURCE_DIR}/resources/win" "${CEF_TARGET_OUT_DIR}")
endif()
