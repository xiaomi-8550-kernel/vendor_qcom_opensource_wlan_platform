ifeq ($(CONFIG_CNSS_OUT_OF_TREE),y)
KBUILD_CPPFLAGS += -DCONFIG_CNSS_OUT_OF_TREE
endif

ifeq ($(CONFIG_CNSS2_DEBUG),y)
KBUILD_CPPFLAGS += -DCONFIG_CNSS2_DEBUG
endif

ifeq ($(CONFIG_CNSS2_QMI),y)
KBUILD_CPPFLAGS += -DCONFIG_CNSS2_QMI
endif

ifeq ($(CONFIG_ONE_MSI_VECTOR),y)
KBUILD_CPPFLAGS += -DCONFIG_ONE_MSI_VECTOR
endif

ifeq ($(CONFIG_ICNSS2_DEBUG),y)
KBUILD_CPPFLAGS += -DCONFIG_ICNSS2_DEBUG
endif

ifeq ($(CONFIG_ICNSS2_QMI),y)
KBUILD_CPPFLAGS += -DCONFIG_ICNSS2_QMI
endif

# CONFIG_WCNSS_MEM_PRE_ALLOC should never be "y" here since it
# can be only compiled as a module from out-of-kernel-tree source.
ifeq ($(CONFIG_WCNSS_MEM_PRE_ALLOC),m)
KBUILD_CPPFLAGS += -DCONFIG_WCNSS_MEM_PRE_ALLOC
endif

# CONFIG_CNSS_PLAT_IPC_QMI_SVC should never be "y" here since it
# can be only compiled as a module from out-of-kernel-tree source.
ifeq ($(CONFIG_CNSS_PLAT_IPC_QMI_SVC),m)
KBUILD_CPPFLAGS += -DCONFIG_CNSS_PLAT_IPC_QMI_SVC
endif

ifeq ($(CONFIG_CNSS_HW_SECURE_DISABLE), y)
KBUILD_CPPFLAGS += -DCONFIG_CNSS_HW_SECURE_DISABLE
endif

ifeq ($(CONFIG_CNSS_HW_SECURE_SMEM), y)
KBUILD_CPPFLAGS += -DCONFIG_CNSS_HW_SECURE_SMEM
endif

ifeq ($(CONFIG_CNSS2_CONDITIONAL_POWEROFF),y)
KBUILD_CPPFLAGS += -DCONFIG_CNSS2_CONDITIONAL_POWEROFF
endif

ifeq ($(CONFIG_CNSS_REQ_FW_DIRECT),y)
KBUILD_CPPFLAGS += -DCONFIG_CNSS_REQ_FW_DIRECT
endif

ifeq ($(CONFIG_CNSS_SUPPORT_DUAL_DEV),y)
KBUILD_CPPFLAGS += -DCONFIG_CNSS_SUPPORT_DUAL_DEV
endif

ifeq ($(CONFIG_AUTO_PROJECT),y)
KBUILD_CPPFLAGS += -DCONFIG_PULLDOWN_WLANEN
endif

ifeq ($(CONFIG_CNSS2_SSR_DRIVER_DUMP),y)
KBUILD_CPPFLAGS += -DCONFIG_CNSS2_SSR_DRIVER_DUMP
endif

ifeq ($(CONFIG_FREE_M3_BLOB_MEM),y)
KBUILD_CPPFLAGS += -DCONFIG_FREE_M3_BLOB_MEM
endif

ifeq ($(CONFIG_DISABLE_CNSS_SRAM_DUMP),y)
KBUILD_CPPFLAGS += -DCONFIG_DISABLE_CNSS_SRAM_DUMP
endif

ifeq ($(CONFIG_CNSS2_SMMU_DB_SUPPORT),y)
KBUILD_CPPFLAGS += -DCONFIG_CNSS2_SMMU_DB_SUPPORT
endif

ifeq ($(CONFIG_CNSS2_ENUM_WITH_LOW_SPEED),y)
KBUILD_CPPFLAGS += -DCONFIG_CNSS2_ENUM_WITH_LOW_SPEED
endif

ifeq ($(CONFIG_SLATE_MODULE_ENABLED), y)
KBUILD_CPPFLAGS += -DCONFIG_SLATE_MODULE_ENABLED
endif

ifeq ($(CONFIG_FEATURE_SMEM_MAILBOX), y)
KBUILD_CPPFLAGS += -DCONFIG_FEATURE_SMEM_MAILBOX
endif

found = $(shell if grep -qF "int msm_pcie_dsp_link_control" $(srctree)/include/linux/msm_pcie.h; then echo "yes" ;else echo "no" ;fi;)
ifeq ($(findstring yes, $(found)), yes)
KBUILD_CPPFLAGS += -DCONFIG_PCIE_SWITCH_SUPPORT
endif

found = $(shell if grep -qF "int msm_pcie_retrain_port_link" $(srctree)/include/linux/msm_pcie.h; then echo "yes" ;else echo "no" ;fi;)
ifeq ($(findstring yes, $(found)), yes)
KBUILD_CPPFLAGS += -DCONFIG_PCIE_SWITCH_RETRAIN_LINK_SUPPORT
endif

obj-$(CONFIG_CNSS2) += cnss2/
obj-$(CONFIG_ICNSS2) += icnss2/
obj-$(CONFIG_CNSS_GENL) += cnss_genl/
obj-$(CONFIG_WCNSS_MEM_PRE_ALLOC) += cnss_prealloc/
obj-y += cnss_utils/
