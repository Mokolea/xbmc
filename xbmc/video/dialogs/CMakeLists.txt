set(SOURCES GUIDialogAudioSettings.cpp
            GUIDialogFullScreenInfo.cpp
            GUIDialogSubtitles.cpp
            GUIDialogSubtitleSettings.cpp
            GUIDialogTeletext.cpp
            GUIDialogVideoBookmarks.cpp
            GUIDialogVideoInfo.cpp
            GUIDialogVideoManager.cpp
            GUIDialogVideoManagerExtras.cpp
            GUIDialogVideoManagerVersions.cpp
            GUIDialogVideoOSD.cpp
            GUIDialogVideoSettings.cpp)

set(HEADERS GUIDialogAudioSettings.h
            GUIDialogFullScreenInfo.h
            GUIDialogSubtitles.h
            GUIDialogSubtitleSettings.h
            GUIDialogTeletext.h
            GUIDialogVideoBookmarks.h
            GUIDialogVideoInfo.h
            GUIDialogVideoManager.h
            GUIDialogVideoManagerExtras.h
            GUIDialogVideoManagerVersions.h
            GUIDialogVideoOSD.h
            GUIDialogVideoSettings.h)

if(TARGET ${APP_NAME_LC}::OpenGl OR CORE_SYSTEM_NAME STREQUAL windows OR CORE_SYSTEM_NAME STREQUAL windowsstore)
  list(APPEND SOURCES GUIDialogCMSSettings.cpp)
  list(APPEND HEADERS GUIDialogCMSSettings.h)
endif()

core_add_library(video_dialogs)
