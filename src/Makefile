# Makefile for Writing Make Files Example

# *****************************************************
# Variables to control Makefile operation

CXX = g++
CXXFLAGS = -Wall -g
OBJ_DIR =  ../build

# ****************************************************
# Targets needed to bring the executable up to date

main: main.o Point.o Rectangle.o
	$(CXX) $(CXXFLAGS) -o main $(OBJ_DIR)/main.o $(OBJ_DIR)/Point.o $(OBJ_DIR)/Rectangle.o

# The main.o target can be written more simply

main.o: main.cpp Point.h Rectangle.h
	$(CXX) $(CXXFLAGS) -c main.cpp
	mv main.o $(OBJ_DIR)

Point.o: Point.h
	$(CXX) $(CXXFLAGS) -c Point.cpp
	mv Point.o $(OBJ_DIR)

Rectangle.o: Rectangle.h Point.h
	$(CXX) $(CXXFLAGS) -c Rectangle.cpp
	mv Rectangle.o $(OBJ_DIR)

.PHONY: clean
clean:
	rm -rf $(OBJ_DIR)
    rm main

$(shell mkdir -p $(OBJ_DIR))
