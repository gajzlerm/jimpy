aprox: main.o splines.o points.o aproksymator_na_bazie.o gsl/libgsl.a
	$(CC) -o aprox  main.o splines.o points.o aproksymator_na_bazie.o -L gsl -l ge

intrp: main.o splines.o points.o interpolator.o gsl/libgsl.a
	$(CC) -o intrp  main.o splines.o points.o interpolator.o -L gsl -l ge

prosta: main.o splines.o points.o prosta.o
	$(CC) -o prosta  main.o splines.o points.o prosta.o	

aproksymator_na_bazie.o: makespl.h points.h gsl/solver.h
	$(CC) -I gsl -c aproksymator_na_bazie.c

interpolator.o: makespl.h points.h gsl/solver.h
	$(CC) -I gsl -c interpolator.c

.PHONY: clean

clean:
	-rm *.o aprox intrp prosta
