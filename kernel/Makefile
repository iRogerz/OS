KBUILD_CFLAGS += -w
obj-m += kernel1.o
all:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) modules
clean:
	make -C /lib/modules/$(shell uname -r)/build M=$(PWD) clean
unload:
	sudo rmmod kernel1
load:
	sudo insmod kernel1.ko
clear:
	sudo dmesg -c
view:
	dmesg