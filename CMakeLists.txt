# This file was generated by FRUT's Jucer2CMake from "BespokeSynth.jucer"
cmake_minimum_required(VERSION 3.16)

project("BespokeSynth")




# link to the FRUT Project cmake files
list(APPEND CMAKE_MODULE_PATH "${CMAKE_SOURCE_DIR}\\cmake")
include(Reprojucer)

# contains settings from the projucer
#set(BespokeSynth_jucer_FILE "${CMAKE_CURRENT_LIST_DIR}/BespokeSynth.jucer")

IF (WIN32)
    # may adapt path to JUCE: TODO: FindJUCE.cmake
    set(JUCE_MODULES_GLOBAL_PATH "C:\\SDKs\\JUCE\\modules")
ELSE()
  # set stuff for other systems
ENDIF()

jucer_project_begin(
  JUCER_FORMAT_VERSION "1"
  PROJECT_FILE "${BespokeSynth_jucer_FILE}"
  PROJECT_ID "vxkFwd"
)

jucer_project_settings(
  PROJECT_NAME "BespokeSynth"
  PROJECT_VERSION "1.0.0"
  # COMPANY_COPYRIGHT
  REPORT_JUCE_APP_USAGE ON # Required for closed source applications without an Indie or Pro JUCE license
  DISPLAY_THE_JUCE_SPLASH_SCREEN ON # Required for closed source applications without an Indie or Pro JUCE license
  SPLASH_SCREEN_COLOUR "Dark"
  PROJECT_TYPE "GUI Application"
  BUNDLE_IDENTIFIER "com.ryanchallinor.Bespoke"
  INCLUDE_BINARYDATA ON
  CXX_LANGUAGE_STANDARD "C++14"
  HEADER_SEARCH_PATHS "C:\\Python39\\include"
)

add_subdirectory(src)
add_subdirectory(libs)

jucer_project_module(
  juce_audio_basics
  PATH "${JUCE_MODULES_GLOBAL_PATH}"
)

jucer_project_module(
  juce_audio_devices
  PATH "${JUCE_MODULES_GLOBAL_PATH}"
  # JUCE_USE_WINRT_MIDI
  # JUCE_ASIO
  # JUCE_WASAPI
  # JUCE_WASAPI_EXCLUSIVE
  # JUCE_DIRECTSOUND
  # JUCE_ALSA
  # JUCE_JACK
  # JUCE_BELA
  # JUCE_USE_ANDROID_OBOE
  # JUCE_USE_OBOE_STABILIZED_CALLBACK
  # JUCE_USE_ANDROID_OPENSLES
  # JUCE_DISABLE_AUDIO_MIXING_WITH_OTHER_APPS
)

jucer_project_module(
  juce_audio_formats
  PATH "${JUCE_MODULES_GLOBAL_PATH}"
  # JUCE_USE_FLAC
  # JUCE_USE_OGGVORBIS
  # JUCE_USE_MP3AUDIOFORMAT
  # JUCE_USE_LAME_AUDIO_FORMAT
  # JUCE_USE_WINDOWS_MEDIA_FORMAT
)

jucer_project_module(
  juce_audio_processors
  PATH "${JUCE_MODULES_GLOBAL_PATH}"
  #JUCE_PLUGINHOST_VST ON
  JUCE_PLUGINHOST_VST3 ON
  # JUCE_PLUGINHOST_AU
  # JUCE_PLUGINHOST_LADSPA
  # JUCE_CUSTOM_VST3_SDK
)

jucer_project_module(
  juce_audio_utils
  PATH "${JUCE_MODULES_GLOBAL_PATH}"
  # JUCE_USE_CDREADER
  # JUCE_USE_CDBURNER
)

jucer_project_module(
  juce_core
  PATH "${JUCE_MODULES_GLOBAL_PATH}"
  # JUCE_FORCE_DEBUG
  # JUCE_LOG_ASSERTIONS
  # JUCE_CHECK_MEMORY_LEAKS
  # JUCE_DONT_AUTOLINK_TO_WIN32_LIBRARIES
  # JUCE_INCLUDE_ZLIB_CODE
  # JUCE_USE_CURL
  # JUCE_LOAD_CURL_SYMBOLS_LAZILY
  # JUCE_CATCH_UNHANDLED_EXCEPTIONS
  # JUCE_ALLOW_STATIC_NULL_VARIABLES
  # JUCE_STRICT_REFCOUNTEDPOINTER
  # JUCE_ENABLE_ALLOCATION_HOOKS
)

jucer_project_module(
  juce_cryptography
  PATH "${JUCE_MODULES_GLOBAL_PATH}"
)

jucer_project_module(
  juce_data_structures
  PATH "${JUCE_MODULES_GLOBAL_PATH}"
)

jucer_project_module(
  juce_events
  PATH "${JUCE_MODULES_GLOBAL_PATH}"
  # JUCE_EXECUTE_APP_SUSPEND_ON_BACKGROUND_TASK
)

jucer_project_module(
  juce_graphics
  PATH "${JUCE_MODULES_GLOBAL_PATH}"
  # JUCE_USE_COREIMAGE_LOADER
  # JUCE_USE_DIRECTWRITE
  # JUCE_DISABLE_COREGRAPHICS_FONT_SMOOTHING
)

jucer_project_module(
  juce_gui_basics
  PATH "${JUCE_MODULES_GLOBAL_PATH}"
  # JUCE_ENABLE_REPAINT_DEBUGGING
  # JUCE_USE_XRANDR
  # JUCE_USE_XINERAMA
  # JUCE_USE_XSHM
  # JUCE_USE_XRENDER
  # JUCE_USE_XCURSOR
  # JUCE_WIN_PER_MONITOR_DPI_AWARE
)

jucer_project_module(
  juce_gui_extra
  PATH "${JUCE_MODULES_GLOBAL_PATH}"
  # JUCE_WEB_BROWSER
  # JUCE_USE_WIN_WEBVIEW2
  # JUCE_ENABLE_LIVE_CONSTANT_EDITOR
)

jucer_project_module(
  juce_opengl
  PATH "${JUCE_MODULES_GLOBAL_PATH}"
)

jucer_project_module(
  juce_osc
  PATH "${JUCE_MODULES_GLOBAL_PATH}"
)

jucer_project_module(
  juce_video
  PATH "${JUCE_MODULES_GLOBAL_PATH}"
  # JUCE_USE_CAMERA
  # JUCE_SYNC_VIDEO_VOLUME_WITH_OS_MEDIA_VOLUME
)


jucer_export_target(
  "Visual Studio 2019"
  VST3_SDK_FOLDER "C:\\SDKs\\VST_SDK\\VST3_SDK"
  EXTRA_PREPROCESSOR_DEFINITIONS
    "GLEW_STATIC"
    "BESPOKE_WINDOWS"
    "POLL_WINDOWS"
    "THREADS_WINDOWS"
    "HAVE_STRUCT_TIMESPEC"
  EXTRA_COMPILER_FLAGS
    "/bigobj"
)

jucer_export_target_configuration(
  "Visual Studio 2019"
  NAME "Debug"
  DEBUG_MODE ON
  BINARY_NAME "BespokeSynth"
  HEADER_SEARCH_PATHS
    "libs\\json\\include"
    "libs\\glew\\include"
    "libs\\push2"
    "libs\\push2\\libusb"
    "libs\\push2\\modules\\libusb"
    "C:\\Python39\\include"
  EXTRA_LIBRARY_SEARCH_PATHS
    "C:\\Python39\\libs"
  OPTIMISATION "No optimisation"
  ENABLE_PLUGIN_COPY_STEP OFF
  WARNING_LEVEL "Low"
  GENERATE_MANIFEST ON
  # ARCHITECTURE "x64"
  DEBUG_INFORMATION_FORMAT "Program Database (/Zi)"
  RELAX_IEEE_COMPLIANCE OFF
)

jucer_export_target_configuration(
  "Visual Studio 2019"
  NAME "Release"
  DEBUG_MODE OFF
  BINARY_NAME "BespokeSynth"
  HEADER_SEARCH_PATHS
    "libs\\json\\include"
    "libs\\glew\\include"
    "libs\\push2"
    "libs\\push2\\libusb"
    "libs\\push2\\modules\\libusb"
    "C:\\Python39\\include"
  EXTRA_LIBRARY_SEARCH_PATHS
    "C:\\Python39\\libs"
  LINK_TIME_OPTIMISATION ON
  OPTIMISATION "Maximise speed"
  ENABLE_PLUGIN_COPY_STEP OFF
  WARNING_LEVEL "Low"
  GENERATE_MANIFEST ON
  # ARCHITECTURE "x64"
  DEBUG_INFORMATION_FORMAT "Program Database (/Zi)"
)




jucer_project_end()
