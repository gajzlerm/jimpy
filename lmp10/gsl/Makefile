libgsl: matrix.o solver.o
	ar rvs libgsl.a $^

matrix.o: matrix.c matrix.h
solver.o: solver.c solver.h matrix.h

.PHONY: clean

clean:
	-rm *.o libgsl.a
