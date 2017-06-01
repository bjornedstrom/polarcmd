# polarcmd

Program for interfacing with Polar smart watches on the command line. Polar M400 is supported but other watches may work as well.

This early work in progress currently support:

* Downloading data from the watch over the USB interface
* Displaying overview training session data

Here is an example use (of a failed attempt at figuring out the authors max heart rate):

    $ polarcmd sync
    Downloading /U/0/TL/RECOVS.BPB
    Downloading /U/0/USERID.BPB
    Downloading /U/0/S/UDEVSET.BPB
    ...

    $ polarcmd show
    2017-05-21 17:54:22 - 2017-05-21 18:50:00 (00:55:36)
    distance: 2.87 km, kcal: 494
    avg hr: 119, max hr: 180
    zone 1: 00:06:48 [12%]
    zone 2: 00:18:38 [33%]
    zone 3: 00:10:16 [18%]
    zone 4: 00:02:48 [05%]
    zone 5: 00:02:31 [04%]

# Install

To download data from the watch using the `sync` command, the program `polarsync` (https://github.com/bjornedstrom/polarsync) needs to be reachable on PATH.

# About & License

In May 2017 the author bought a Polar M400 watch. Unfortunately the software does not work on Linux and that's how this project was born.

As far as I know, this is the first open source program that has started to reconstruct Polar protobuf message structs (".proto files"). See polar.proto for the main effort.

Copyright (c) Björn Edström <be@bjrn.se> 2017. See LICENSE for details.
