all: swapview swapview-llvm

swapview: swapview.d
	dmd -O -release -inline -boundscheck=off $<
	strip $@

swapview-llvm: swapview.d
	ldc2 -g -O4 --flto=full $< -of=$@
	strip $@

clean:
	-rm -f swapview{,-llvm} *.o

