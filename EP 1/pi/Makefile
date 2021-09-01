CC=gcc

all: clean sequential pthread openmp mpi mpi-reduce

sequential:
	$(CC) pi_seq.c -o pi_seq

pthread:
	$(CC) pi_pth.c -o pi_pth -lpthread

openmp:
	# For Linux systems
	$(CC) pi_omp.c -o pi_omp -fopenmp
	# For MacOS with clang
	# /usr/local/opt/llvm/bin/clang pi_omp.c -o pi_omp -fopenmp -L/usr/local/opt/llvm/lib

clean:
	rm -f pi_seq pi_pth pi_omp
