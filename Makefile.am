
lib_LTLIBRARIES = libvcu_gst.la

AM_DEFAULT_SOURCE_EXT = .c

vcu_gst_lib_INC_DIR = ./include
vcu_gst_lib_SRC_DIR = ./src

#NOTE: In some build system, single $ character is not interpreted correctly and removed, so we have added $$ to overcome such issue.
VCU_GST_CFLAGS_PKG_CONFIG = $$(pkg-config --cflags gstreamer-1.0 gstreamer-plugins-base-1.0 vcu-video-lib)
VCU_GST_LIBS_PKG_CONFIG = $$(pkg-config --libs gstreamer-1.0 gstreamer-plugins-base-1.0 gstreamer-video-1.0 vcu-video-lib)

nodist_libvcu_gst_la_SOURCES = \
        $(vcu_gst_lib_INC_DIR)/vgst_err.h \
		$(vcu_gst_lib_INC_DIR)/vgst_lib.h \
		$(vcu_gst_lib_INC_DIR)/vgst_config.h \
		$(vcu_gst_lib_INC_DIR)/vgst_pipeline.h \
		$(vcu_gst_lib_INC_DIR)/vgst_split_pipeline.h \
		$(vcu_gst_lib_INC_DIR)/vgst_utils.h

libvcu_gst_la_SOURCES =  \
		$(vcu_gst_lib_SRC_DIR)/vgst_lib.c \
		$(vcu_gst_lib_SRC_DIR)/vgst_pipeline.c \
		$(vcu_gst_lib_SRC_DIR)/vgst_split_pipeline.c \
		$(vcu_gst_lib_SRC_DIR)/vgst_utils.c

libvcu_gst_la_includedir = /usr/include
libvcu_gst_la_include_HEADERS = \
		$(vcu_gst_lib_INC_DIR)/vgst_err.h \
		$(vcu_gst_lib_INC_DIR)/vgst_lib.h

libvcu_gst_la_CFLAGS = $(VCU_GST_CFLAGS_PKG_CONFIG) -I$(vcu_gst_lib_INC_DIR)
libvcu_gst_la_LDFLAGS = $(VCU_GST_LIBS_PKG_CONFIG)
