###################################################
#
# Makefile
# Simple TCP/IP communication using sockets
#
# Vangelis Koukis <vkoukis@cslab.ece.ntua.gr>
#
###################################################

CC = gcc

CRYPTODEVDIR=$(HOME)/cryptodev/cryptodev-linux-1.6

CFLAGS = -Wall -I$(CRYPTODEVDIR)
CFLAGS += -g
# CFLAGS += -O2 -fomit-frame-pointer -finline-functions

LIBS =

BINS = crypto-server crypto-client

all: $(BINS)

crypto-server: crypto-server.c crypto-common.h
	$(CC) $(CFLAGS) -o $@ $< $(LIBS)

crypto-client: crypto-client.c crypto-common.h
	$(CC) $(CFLAGS) -o $@ $< $(LIBS)

clean:
	rm -f *.o *~ $(BINS)
