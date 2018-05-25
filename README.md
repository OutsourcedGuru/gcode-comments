# gcode-comments
A node command-line tool (CLI) for auto-adding comments to a GCODE file

This is a Node.js file written in JavaScript which will open the indicated GCODE file and create a new one with comments. Each comment will be based upon the type of [RepRap field command](http://reprap.org/wiki/G-code#Fields) which is seen.

## Installation
It is suggested that the script file be placed somewhere in your path so that you don't have to indicate where to find it (as seen below).

Note that `gcode-comments` expects the GCODE file to be in the current working direction, however.

```
$ cd sites
$ git clone --depth=1 https://github.com/OutsourcedGuru/gcode-comments
$ cd gcode-comments
$ chmod a+x gcode-comments
# Copy a GCODE file into this folder, then:
$ ./gcode-comments file.gcode

;FLAVOR:RepRap
;TIME:11265
;Generated with Cura_SteamEngine 2.3.1
M104 S205                                         ; Set extruder temperature
M109 S205                                         ; Set extruder temperature and wait (blocking)

;LAYER_COUNT:28
;LAYER:0
M107                                              ; Turn off fan
M205 X10                                          ; Adjust jerk speed
G1 F2400 E-1                                      ; Move and/or extrude to the indicated point
...

Input:   file.gcode
Output:  file_commented.gcode
```

|Donate||Cryptocurrency|
|:-----:|---|:--------:|
| ![eth-receive](https://user-images.githubusercontent.com/15971213/40564950-932d4d10-601f-11e8-90f0-459f8b32f01c.png) || ![btc-receive](https://user-images.githubusercontent.com/15971213/40564971-a2826002-601f-11e8-8d5e-eeb35ab53300.png) |
|Ethereum||Bitcoin|
