# Compile flags.
CFLAGS = -g -Wall -std=c++11
LDFLAGS = -lpthread
OPTFLAGS = -O3
CC = g++

# Default targets.
build: tests thread

# Build target.
tests: tests.cpp
	$(CC) $(CFLAGS) $< -o $@ $(LDFLAGS)

thread: thread.cpp
	$(CC) $(CFLAGS) $< -o $@ $(LDFLAGS)

size: size.cpp
	$(CC) $(CFLAGS) $< -o $@ $(LDFLAGS)

# Optimized version.
opt: $(MAKECMDGOALS)	#variable wich contains the goal from the command line, can be more than one.
	$(CC) $(CFLAGS) $(OPTFLAGS) $<.cpp -o $< $(LDFLAGS)

# Generate assembly code.
asm: $(target)		#in command line use 'target=file.cpp'
	$(CC) $(CFLAGS) $(OPTFLAGS) -S $< -o assembly.s $(LDFLAGS)

# Compile assembly code.
assembly: assembly.s
	$(CC) $< -o $@




