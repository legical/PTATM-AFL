# By default, the code is compiled for a "big endian" machine.
# To compile on a "little endian" machine set the LITTLE_ENDIAN flag.
# To make smaller object code, but run a little slower, don't use UNROLL_LOOPS.
# To use NIST's modified SHA of 7/11/94, define USE_MODIFIED_SHA

CC = gcc
CFLAGS = -Wall
BINFILE = sha

sha:	sha_driver.o sha.o
	$(CC) -o $@ sha_driver.o sha.o

clean:
	@if [ -z "$(OUT)" ]; then \
		echo "clean $(pwd)"; \
	else \
		echo "mv $(BINFILE) to $(OUT)"; \
		mkdir -p $(OUT); \
		mv -f $(BINFILE)  $(OUT); \
	fi
	rm -rf *.o $(BINFILE) output*
