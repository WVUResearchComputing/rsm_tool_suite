#CC = cc
CC = mpiicc
CFLAGS = -g -p -O3 -parallel -std=c99 -march=skylake-avx512
#CFLAGS = -Wall -pedantic -g -std=c99
LIBS = -lm -lgsl -lgslcblas

OBJS = tpm.o

tpm :  $(OBJS)
	$(CC) -o tpm $(OBJS) $(LIBS) $(CFLAGS)

tpm.o: tpm.c $(HEADS)
	$(CC) -c tpm.c $(CFLAGS)

clean:
	rm -rf tpm.o tpm

clean_data:
	rm -rf  Cdout* tpmout* core.*

clean_all: clean clean_data
