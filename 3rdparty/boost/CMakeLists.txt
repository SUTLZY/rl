cmake_minimum_required(VERSION 2.8.11)

project(boost)

include(ExternalProject)
include(GNUInstallDirs)

ExternalProject_Add(
	boost
	URL https://dl.bintray.com/boostorg/release/1.71.0/source/boost_1_71_0.tar.bz2
	#URL ${CMAKE_CURRENT_SOURCE_DIR}/boost_1_71_0.tar.bz2
	URL_MD5 4cdf9b5c2dc01fb2b7b733d5af30e558
	CONFIGURE_COMMAND ""
	BUILD_COMMAND ""
	BUILD_IN_SOURCE 1
	INSTALL_COMMAND ${CMAKE_COMMAND} -E copy_directory <SOURCE_DIR>/boost ${CMAKE_INSTALL_FULL_INCLUDEDIR}/boost
)
