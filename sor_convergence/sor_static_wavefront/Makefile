#CC = /opt/rh/devtoolset-2/root/usr/bin/gcc
CC = gcc
OMP_FLAG = -fopenmp
<<<<<<< HEAD
CFLAGS = -O3 -c ${OMP_FLAG}
=======
CFLAGS = -O1 -c ${OMP_FLAG}
#CFLAGS = -O2 -c ${OMP_FLAG}
#CFLAGS = -c ${OMP_FLAG}
>>>>>>> 7046cb8ce94f73f6687fb2a3c9e75bd38a03fb26
LFLAGS = -lm

.SUFFIXES : .o .c

.c.o:
	${CC} ${CFLAGS} -o $@ $*.c

sor: sor.o
	${CC} ${OMP_FLAG} -o $@ $@.o ${LFLAGS}

sor_wavefront_sequential: sor_wavefront_sequential.o
	${CC} ${OMP_FLAG} -o $@ $@.o ${LFLAGS}

sor_wavefront_parallel: sor_wavefront_parallel.o
	${CC} ${OMP_FLAG} -o $@ $@.o ${LFLAGS}

better_sor_wavefront_sequential: better_sor_wavefront_sequential.o
	${CC} ${OMP_FLAG} -o $@ $@.o ${LFLAGS}
clean:
	rm *.o sor sor_wavefront_sequential sor_wavefront_parallel better_sor_wavefront_sequential
