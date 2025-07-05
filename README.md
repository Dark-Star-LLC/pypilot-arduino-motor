# pypilot-arduino-motor
PlatformIO version of the pypilot motor controller sketch.

We are using platform IO in order to program the arduino using Visual Studio, as a work around for problems encountered with Arduino IDE.

See [pypilot/.../arduino/motor/motor.ino](https://github.com/pypilot/pypilot/blob/master/arduino/motor/motor.ino) for the original source.  Also see:
* https://open-boat-projects.org/en/pypilot/
* https://github.com/pypilot/workbook/wiki/installing-the-arduino
* https://github.com/AndreasW29/pypilot-tinypilot-mysolution-infos/blob/main/READMEenglish.md
* https://pypilot.org/schematics/hbridge_controller.pdf

# diffs
To see the latest copies of the analogous files, access these urls:
* https://github.com/pypilot/pypilot/blob/master/arduino/motor/motor.ino
* https://github.com/Dark-Star-LLC/pypilot-arduino-motor/blob/main/src/motor.cpp
* https://github.com/pypilot/pypilot/blob/master/arduino/motor/crc.h
* https://github.com/Dark-Star-LLC/pypilot-arduino-motor/blob/main/src/crc.h

To get a diff of this motor.cpp vs the main pypilot motor.ino, inside a local copy of this repo:
```sh
git remote add pypilot_original_repo https://github.com/pypilot/pypilot.git
git fetch pypilot_original_repo
git worktree add -b temp_pypilot_branch ~/pypilot_temp pypilot_original_repo/master

git diff main -- src/motor.cpp src/crc.h temp_pypilot_branch -- arduino/motor/motor.ino

# similarly, for crc.h
git diff main -- src/crc.h temp_pypilot_branch -- arduino/motor/crc.h

# cleanup when finished
git worktree remove ~/pypilot_temp
```

