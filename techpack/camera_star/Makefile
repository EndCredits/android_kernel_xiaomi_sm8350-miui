# SPDX-License-Identifier: GPL-2.0-only

ifeq ($(CONFIG_BOARD_XIAOMI_STAR), y)
$(info Building for Xiaomi Mi 11 Ultra)
# auto-detect subdirs
ifneq ($(CONFIG_ARCH_QTI_VM), y)
ifeq ($(CONFIG_ARCH_KONA), y)
include $(srctree)/techpack/camera_star/config/konacamera.conf
endif

ifeq ($(CONFIG_ARCH_LITO), y)
include $(srctree)/techpack/camera_star/config/litocamera.conf
endif

ifeq ($(CONFIG_ARCH_BENGAL), y)
include $(srctree)/techpack/camera_star/config/bengalcamera.conf
endif

ifeq ($(CONFIG_ARCH_LAHAINA), y)
include $(srctree)/techpack/camera_star/config/lahainacamera.conf
endif

ifeq ($(CONFIG_ARCH_HOLI), y)
include $(srctree)/techpack/camera_star/config/holicamera.conf
endif

ifeq ($(CONFIG_ARCH_SHIMA), y)
include $(srctree)/techpack/camera_star/config/shimacamera.conf
endif

ifeq ($(CONFIG_ARCH_KONA), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera_star/config/konacameraconf.h
endif

ifeq ($(CONFIG_ARCH_LITO), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera_star/config/litocameraconf.h
endif

ifeq ($(CONFIG_ARCH_BENGAL), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera_star/config/bengalcameraconf.h
endif

ifeq ($(CONFIG_ARCH_LAHAINA), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera_star/config/lahainacameraconf.h
endif

ifeq ($(CONFIG_ARCH_HOLI), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera_star/config/holicameraconf.h
endif

ifeq ($(CONFIG_ARCH_SHIMA), y)
LINUXINCLUDE    += \
		-include $(srctree)/techpack/camera_star/config/shimacameraconf.h
endif

endif

ifneq (,$(filter $(CONFIG_SPECTRA_CAMERA), y m))
# Use USERINCLUDE when you must reference the UAPI directories only.
USERINCLUDE     += \
                -I$(srctree)/techpack/camera_star/include/uapi

# Use LINUXINCLUDE when you must reference the include/ directory.
# Needed to be compatible with the O= option
LINUXINCLUDE    += \
                -I$(srctree)/techpack/camera_star/include/uapi \
                -I$(srctree)/techpack/camera_star/include
obj-y += drivers/
else
$(info Target not found)
endif
endif