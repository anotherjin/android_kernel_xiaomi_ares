# SPDX-License-Identifier: GPL-2.0
# Makefile for Hyper-V tools

WARNINGS =  -Wextra
CFLAGS = $(WARNINGS) -g $(shell getconf LFS_CFLAGS)

CFLAGS += -D__EXPORTED_HEADERS__ -I../../include/uapi -I../../include

all: hv_kvp_daemon hv_vss_daemon hv_fcopy_daemon
%: %.c
	$(CC) $(CFLAGS) -o $@ $^

clean:
	$(RM) hv_kvp_daemon hv_vss_daemon hv_fcopy_daemon
