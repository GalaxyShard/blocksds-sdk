# SPDX-License-Identifier: CC0-1.0
#
# SPDX-FileContributor: Antonio Niño Díaz, 2023


# Tools
# -----

MAKE		:= make

# Verbose flag
# ------------

ifeq ($(VERBOSE),1)
V		:=
else
V		:= @
endif

# Targets
# -------

.PHONY: all clean minimal wifi maxmod libxm wifi_maxmod wifi_libxm

all: minimal wifi maxmod libxm wifi_maxmod wifi_libxm

clean:
	@echo "  CLEAN"
	@rm -rf build

minimal:
	@+$(MAKE) BUILDDIR=build/minimal -f Makefile.generic --no-print-directory
wifi:
	@+$(MAKE) BUILDDIR=build/wifi USE_DSWIFI=1 -f Makefile.generic --no-print-directory
maxmod:
	@+$(MAKE) BUILDDIR=build/maxmod USE_MAXMOD=1 -f Makefile.generic --no-print-directory
libxm:
	@+$(MAKE) BUILDDIR=build/libxm USE_LIBXM7=1 -f Makefile.generic --no-print-directory
wifi_maxmod:
	@+$(MAKE) BUILDDIR=build/wifi_maxmod USE_DSWIFI=1 USE_MAXMOD=1 -f Makefile.generic --no-print-directory
wifi_libxm:
	@+$(MAKE) BUILDDIR=build/wifi_libxm USE_DSWIFI=1 USE_LIBXM7=1 -f Makefile.generic --no-print-directory

