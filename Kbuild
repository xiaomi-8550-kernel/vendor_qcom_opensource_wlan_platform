ifeq ($(CONFIG_CNSS_OUT_OF_TREE),y)
KBUILD_CPPFLAGS += -DCONFIG_CNSS_OUT_OF_TREE
endif

ifeq ($(CONFIG_CNSS2_DEBUG),y)
KBUILD_CPPFLAGS += -DCONFIG_CNSS2_DEBUG
endif

ifeq ($(CONFIG_CNSS2_QMI),y)
KBUILD_CPPFLAGS += -DCONFIG_CNSS2_QMI
endif

# CONFIG_CNSS_PLAT_IPC_QMI_SVC should never be "y" here since it
# can be only compiled as a module from out-of-kernel-tree source.
ifeq ($(CONFIG_CNSS_PLAT_IPC_QMI_SVC),m)
KBUILD_CPPFLAGS += -DCONFIG_CNSS_PLAT_IPC_QMI_SVC
endif

obj-$(CONFIG_CNSS2) += cnss2/
obj-$(CONFIG_CNSS_GENL) += cnss_genl/
obj-$(CONFIG_WCNSS_MEM_PRE_ALLOC) += cnss_prealloc/
obj-y += cnss_utils/