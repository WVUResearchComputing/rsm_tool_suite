#CC = cc
CC = mpicc
CFLAGS = -g -pg -O0 -std=c99
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
