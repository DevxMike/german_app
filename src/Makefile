CC = g++

CFLAGS = 

CFLAGS_CLANG = -Weverything

EXEC = exec_file
SOURCES = ./source/main.cpp
OBJECTS = $(SOURCES:.cpp=.o)

ifeq ($(CC),gcc)
	CFLAGS += $(CFLAGS_GCC)
else ifeq ($(CC),clang)
	CFLAGS += $(CFLAGS_CLANG)
endif

EXEC: $(OBJECTS)
	$(CC) $(OBJECTS) -o $(EXEC) $(CFLAGS)

%.o: %.c
	$(CC) -c $< -o $@ $(CFLAGS) 

clean:
	rm -f $(OBJECS)
