KERNEL_DIR	:= /lib/modules/$(shell uname -r)/build
#KERNEL_DIR	:= /home/liujl/temp/kernel_other/kernel/
KERNEL_VERSION	:= $(shell uname -r)
PWD		:= $(shell pwd)
MODULE_NAME := sr9700
obj-m		:= $(MODULE_NAME).o

all: 
	@echo "Building sr9700 USB2NET chip driver..."
	@(cd $(KERNEL_DIR) && make -C $(KERNEL_DIR) SUBDIRS=$(PWD) CROSS_COMPILE=$(CROSS_COMPILE) modules)

clean:
	-rm -f *.o *.ko .*.cmd .*.flags .mii.mod.o.d *.mod.c Module.symvers Module.markers modules.order version.h
	-rm -rf .tmp_versions

