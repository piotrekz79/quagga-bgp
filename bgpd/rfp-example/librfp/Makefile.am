#
# This file has been modified by LabN Consulting, L.L.C.
#
#
## Process this file with automake to produce Makefile.in.

if ENABLE_BGP_VNC
BGP_VNC_RFAPI_INC=-I$(top_srcdir)/bgpd/rfapi
BGP_VNC_RFP_LIBDIR=.
BGP_VNC_RFP_INCDIR=$(BGP_VNC_RFP_LIBDIR)
BGP_VNC_RFP_LIB=librfp.a
BGP_VNC_RFP_INC=-I$(BGP_VNC_RFP_INCDIR)

librfp_a_SOURCES = \
	rfp_example.c 

librfp_a_INCLUDES = \
	rfp.h \
	rfp_internal.h 

else
BGP_VNC_RFAPI_INC=
BGP_VNC_RFAPI_SRC=
BGP_VNC_RFP_LIB=
BGP_VNC_RFP_INC=
endif

AM_CPPFLAGS =  -I$(top_srcdir) -I$(top_srcdir)/lib \
	$(BGP_VNC_RFAPI_INC) $(BGP_VNC_RFP_INC)
DEFS = @DEFS@ -DSYSCONFDIR=\"$(sysconfdir)/\"
INSTALL_SDATA=@INSTALL@ -m 600

AM_CFLAGS = $(PICFLAGS)
AM_LDFLAGS = $(PILDFLAGS)

noinst_LIBRARIES = $(BGP_VNC_RFP_LIB)

noinst_HEADERS = \
	$(librfp_a_INCLUDES)
