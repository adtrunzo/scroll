INCLUDE := -I ~/include
LDFLAGS := -L ~/lib -lsense -lm
# If you are compiling this to run on CISC210,
# uncomment the below line
#LDFLAGS := $(LDFLAGS) -lncurses


all: main.o display.o input.o
	cc -o scroll main.o display.o input.o $(LDFLAGS)

clean:
	rm -f *.o scroll
main.o: main.c scroll.h
	cc -c main.c -I ~/include
display.o: display.c
	cc -c display.c -I ~/include
input.o: input.c
	cc -c input.c -I ~/include

run:
	./scroll.sh | ./scroll
