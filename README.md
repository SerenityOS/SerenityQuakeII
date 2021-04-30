Quake2 SDL
==========

This is a port of Quake2 based on icculus quake2lnx. Changes are:

* Switched to SDL2 from SDL1.2. This allows you to run the game on
  Wayland.
* The building system is now cmake.
* Lots of unmaintained source code removed, including the code for
  different platforms like Solaris, IRIX, etc. This code was almost
  identical to one found in src/linux. Also I removed the code related
  to X11 and SVGAlib.
* Software renderer has a bug in a code which draws alpha surfaces. Just
  switch drawing of alpha surfaces off now.
* Audio CD playback is switched off (Does anyone have CD drive now? ).
* Apply bugfixes from FreeBSD ports.
* Fix some compiler warnings and possible bugs.
* Add 1920x1080 screen resolution.

TODO:
* Remove even more boilerplate and machine-dependent code, use SDL
  crossplatform stuff.
* Fix alpha surfaces rendering in software renderer.
* Build CTF mode.

Building and installation
-------------------------

Build like a regular Serenity Port.
In the `quake2` port directory, run `./package.sh`.

You'll then need to source the QuakeII demo pak file yourself. iD's FTP is offline, however you can find the demo in a few places. Once you've downloaded the demo, move the `pak0.pak` file to `/home/anon/.quake2/baseq2/` and run `quake2` from the command line. 
