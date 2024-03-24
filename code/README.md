## Testing

### Build

Make sure OpenCV has been installed and is configured with pkg-config. Clone or extract the repository and run

```bash
cd Traffic-Density-Estimation/
cd Code/
make # To compile src/main.cpp
```

### Download Video

```bash
To download the traffic video use the link given below-
https://drive.google.com/file/d/1w1h27n_91rWsvUVuFUY1eZFKvl9oosGP/view?usp=drive_link
After downloading the video, move it to ./assets/trafficvideo.mp4
```

### How To give Input

```bash
In input.txt file pass space separated integers after the video destination
first pass the method number ( example give 1 in case of method 1)
- method 1: pass a space separated integer indicating number of skip frames(1 to 10) (input example- 1 2) where 1 is the method number and 2 is the number of skip frames.
- method 2: pass 2 space separated parameters that is the width and height of the frame.
- method 3 and 4 : pass the number of threads as an integer.
- method 5: pass 0 or 1 which would indicate dense or sparse optical flow.
```

### Run

To execute the compiled file run (Recommended):

```bash
make run # To execute ./build/main.out
```

### Additional Commands

A few additional make rules:

```bash
make clean      # To clean the build and runtime files run.
make help       # To see all make options.
```

An incorrect make rule helps the user by directing them to the 'make help' command.
