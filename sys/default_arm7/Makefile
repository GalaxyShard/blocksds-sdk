# SPDX-License-Identifier: CC0-1.0
#
# SPDX-FileContributor: Antonio Niño Díaz, 2023


# Tools
# -----

MAKE		:= make
CP		:= cp

# Verbose flag
# ------------

ifeq ($(VERBOSE),1)
V		:=
else
V		:= @
endif

# Targets
# -------

.PHONY: all clean minimal dswifi maxmod libxm dswifi_maxmod dswifi_libxm

all: minimal dswifi maxmod libxm dswifi_maxmod dswifi_libxm

clean:
	@echo "  CLEAN"
	@rm -rf build
	@rm -f arm7.elf arm7_*.elf

minimal:
	@+$(MAKE) -f Makefile.generic --no-print-directory \
		  NAME=minimal

dswifi:
	@+$(MAKE) -f Makefile.generic --no-print-directory \
		  NAME=dswifi \
		  USE_DSWIFI=1

maxmod:
	@+$(MAKE) -f Makefile.generic --no-print-directory \
		  NAME=maxmod \
		  USE_MAXMOD=1

libxm:
	@+$(MAKE) -f Makefile.generic --no-print-directory \
		  NAME=libxm7 \
		  USE_LIBXM7=1

dswifi_maxmod:
	@+$(MAKE) -f Makefile.generic --no-print-directory \
		  NAME=dswifi_maxmod \
		  USE_DSWIFI=1 \
		  USE_MAXMOD=1
	$(V)$(CP) arm7_dswifi_maxmod.elf arm7.elf

dswifi_libxm:
	@+$(MAKE) -f Makefile.generic --no-print-directory \
		  NAME=dswifi_libxm \
		  USE_DSWIFI=1 \
		  USE_LIBXM7=1
