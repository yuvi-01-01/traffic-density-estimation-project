CFLAGS = -pthread -std=c++11 -Wall
OPENCV = `pkg-config opencv --cflags --libs`
LIBS = $(OPENCV)

SRC = ./src
BUILD = ./build
ANALYSIS = ../analysis
ASSETS = ./assets

all:
	mkdir -p $(BUILD)
	mkdir -p $(ANALYSIS)/results
	echo "Building.."
	g++ $(CFLAGS) $(LIBS) $(SRC)/main.cpp -o $(BUILD)/main.out
	echo "Generated $(BUILD)/main.out \nEnter 'make run' to execute."

run:
	mkdir -p $(ANALYSIS)/results
	if [ -f "./build/main.out" ]; then echo "Running $(BUILD)/main.out"; $(BUILD)/main.out; else echo "Build not found. Run 'make' first."; fi

clean:
	rm -rf $(BUILD)
	rm -rf $(ANALYSIS)/results
	echo "Cleaned."

help: 
	echo "Commands:"
	echo "'make'         : builds the executable."
	echo "'make run'     : runs the executable. Does not create the executable."
	echo "'make clean'   : removes the build files."
	echo "'make download': downloads assets and stores them in the appropriate directory."

.DEFAULT: 
	@echo "No such command found. Run 'make help' for more info."

.SILENT: all run clean help download graph model