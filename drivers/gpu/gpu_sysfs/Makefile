# ==================================
#HACK
# NO MALI GPU
CONFIG_MSM_KGSL=1

# ==================================
# Start --------- Qualcomm ---------
ifdef CONFIG_MSM_KGSL

gpu_sysfs-y +=	gpu_sysfs_target_kgsl.o
# Verify: target specific file is defined.
GPU_SYSFS_TARGET_FILE_DEFINED=1

endif
# End ---------- Qualcomm ----------
# ==================================


# ==================================
# Generate error if the TARGET
# specific file is not defined OR
# picked using the PLATFORM configs.
ifndef GPU_SYSFS_TARGET_FILE_DEFINED
$(warning **** Make sure target file is defined. \
               Check the TARGET and GPU configs in Makefile and Kernel Config. \
               Module won't work without target file. ****)
endif


clean:
	rm -f *.o .*.cmd modules.order Module.symvers gpu_sysfs.ko gpu_sysfs.mod.c
	rm -rf .tmp_versions
