SSH Ramdisk Mod
================================

Automated SSH Ramdisk Creator/Loader
Written by msft_guy (https://github.com/msftguy) modified by myself to support iPhone 4 GSM Rev A's (partially)

Is able to currently recognise a Rev A i4 and (sortof) and patch 5.1.1 original revision firmware in an attempt to 
boot it as if it were an original revision iPhone. libpois0n doesn't currently support booting it so you're going 
to have to fix that manually or boot it using something else (such as opensn0w?)

In theory this should create a working ramdisk that can be booted on a Rev A.
All rights to this git are reserved for msft_guy.

Original Readme on https://github.com/msftguy/ssh-rd is below

-------------------------------
Automated SSH ramdisk creator/loader
Compatible devices: hopefully everything Syringe supports

Building: 
 # Submodules (xpwn and syringe)
git submodule init
git submodule update
 
# OS X: you need libusb and arm-elf-binutils (and maybe arm-elf-gcc?) from macports to build syringe
 
# Boost: Stripped down boost needed by fuzzy_patcher included in _3rd/boost_1_48_0: run bootstrap.sh/.cmd, then use build-osx.sh or build-win32.cmd to build.
 
# general building - OS X: cd syringe; make all; cd ../xpwn; make all; cd ../mux_redux; make all; cd ../fuzzy_patcher; make all; cd jsyringeapi; make all; cp *.jnilib ../java/gui/src/res/native/

# general building - Win32: Just set JAVA_HOME to where the JDK is and build the solution.

# Building the Java project:
 Use Eclipse; add stuff from java/_3rd as external JARs.
 On Windows, make sure to use a 32-bit JDK environment to build/debug the java/gui project; since iTunes DLLs are 32bit, and so are the native DLLs that the solution builds.

-------------------------------

This is just the java project. You're going to have to fetch the external jars and such from the original git at https://github.com/msftguy/ssh-rd

A Restore.plist is included here which you can replace the one downloaded from Apple with to get around some errors.... Yes this is a hack job.