CFLAGS:=-I include/ -Wall -Wextra -pedantic

lab_03: obj/mergesort.o obj/main.o | obj
	gcc -g obj/mergesort.o obj/main.o -o lab_03

test: obj/mergesort.o obj/test.o | obj
	gcc -g obj/mergesort.o obj/test.o -o test

obj/mergesort.o: include/mergesort.h src/mergesort.c | obj
	gcc -g -c $(CFLAGS) src/mergesort.c -o obj/mergesort.o

obj/main.o: include/mergesort.h src/main.c | obj
	gcc -g -c $(CFLAGS) src/main.c -o obj/main.o

obj/test.o: include/mergesort.h src/test.c | obj	
	gcc -g -c $(CFLAGS) src/test.c -o obj/test.o

obj:
	mkdir obj

.PHONY: clean
clean: | obj
	rm -rf obj lab_03 test
