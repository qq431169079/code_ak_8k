#Kernel location

TOPDIR 	?= $(shell pwd)/../../../..
KERNELDIR ?= $(TOPDIR)/kernel
PLATDIR ?= $(TOPDIR)/platform



# Flags

INCLUDE    =	-I. \
		-I$(KERNELDIR)/include \
		-I$(KERNELDIR)/include/os \
		-I$(KERNELDIR)/include/lwip \
		-I$(KERNELDIR)/include/lwip/ipv4 \
		-I$(PLATDIR)/libplat/include \
		-I$(PLATDIR)/libmpi/include \
		-I$(PLATDIR)/libapp/include \



#Src locations
SRCDIR += .

CSRCS += $(foreach d, $(SRCDIR), $(wildcard $d/*.c))

COBJS += $(patsubst %.c, %.o, $(CSRCS))



#build rule
.PHONY: all target clean

all: target 

target: $(COBJS) 
	@echo ---------------------[build obj complete]----------------------------------	


clean : 
	$(RM) $(COBJS)


# Rules
include $(TOPDIR)/rules.mk

