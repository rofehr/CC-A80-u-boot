
##
## Makefile for Sunxi Secure Boot
##



include $(TOPDIR)/config.mk

LIB	:= $(obj)libdram.o

COBJS += mctl_hal.o
COBJS += rsb.o


COBJS	:= $(COBJS)
SRCS	:= $(COBJS:.o=.c)
OBJS	:= $(addprefix $(obj),$(COBJS))

all:	$(LIB)

$(LIB):	$(obj).depend $(OBJS)
	$(call cmd_link_o_target, $(OBJS))

#########################################################################

# defines $(obj).depend target
include $(SRCTREE)/rules.mk

sinclude $(obj).depend

#########################################################################
