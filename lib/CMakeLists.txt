set(appmenuapplet_SRCS
    appmenuapplet.cpp
    decorationpalette.cpp
)

add_library(org.kde.windowappmenu MODULE ${appmenuapplet_SRCS})

#kcoreaddons_desktop_to_json(org.kde.windowappmenu ../package/metadata.desktop)
add_custom_command(
    OUTPUT ${CMAKE_CURRENT_BINARY_DIR}/metadata.json
    COMMAND desktoptojson -i ${CMAKE_SOURCE_DIR}/package/metadata.desktop
    WORKING_DIRECTORY ${CMAKE_CURRENT_SOURCE_DIR}
)

set_property(TARGET org.kde.windowappmenu APPEND PROPERTY AUTOGEN_TARGET_DEPENDS ${CMAKE_CURRENT_BINARY_DIR}/metadata.json)

target_link_libraries(org.kde.windowappmenu
                      Qt6::Widgets
                      Qt6::Quick
                      Qt6::DBus
                      KF6::ConfigWidgets
                      Plasma::Plasma
                      KF6::WindowSystem
                      KDecoration2::KDecoration
                      KDecoration2::KDecoration2Private)

install(TARGETS org.kde.windowappmenu DESTINATION ${KDE_INSTALL_PLUGINDIR}/plasma/applets)
