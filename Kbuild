BT_ROOT := $(srctree)/techpack/bt

ifeq ($(CONFIG_ARCH_WAIPIO), y)
include $(BT_ROOT)/config/gki_waipiobt.conf
endif

ifeq ($(CONFIG_ARCH_KALAMA), y)
include $(BT_ROOT)/config/gki_kalamabt.conf
endif

ifneq (,$(filter $(CONFIG_MSM_BT_POWER),y m))
KBUILD_CPPFLAGS += -DCONFIG_MSM_BT_POWER
endif

ifneq (,$(filter $(CONFIG_BTFM_SLIM),y m))
KBUILD_CPPFLAGS += -DCONFIG_BTFM_SLIM
endif

ifneq (,$(filter $(CONFIG_I2C_RTC6226_QCA),y m))
KBUILD_CPPFLAGS += -DCONFIG_I2C_RTC6226_QCA
endif

ifneq (,$(filter $(CONFIG_BT_HW_SECURE_DISABLE),y m))
KBUILD_CPPFLAGS += -DCONFIG_BT_HW_SECURE_DISABLE
endif

ifneq (,$(filter $(CONFIG_SLIM_BTFM_CODEC),y m))
KBUILD_CPPFLAGS += -DCONFIG_SLIM_BTFM_CODEC
endif

obj-$(CONFIG_MSM_BT_POWER) += pwr/
obj-$(CONFIG_BTFM_SLIM) += slimbus/
obj-$(CONFIG_I2C_RTC6226_QCA) += rtc6226/
obj-$(CONFIG_BTFM_CODEC) += btfmcodec/
obj-$(CONFIG_SLIM_BTFM_CODEC) += slimbus/
