Cydia Installer
============

This has been modified to work with recent Xcode releases and Homebrew instead of Fink. Other than that, it is a mirror of [git://git.saurik.com/cydia.git](git://git.saurik.com/cydia.git).

Important
------------

A computer running OS X is required to build Cydia. There is no way around this.

Build Instructions
------------

1. Install the official Apple iOS SDK, which comes with Xcode. Note that recent Xcode builds do not support the armv6 architecture.
2. Install [Homebrew](http://mxcl.github.com/homebrew/)
3. Run `brew install bash ldid gnu-tar wget xz`
4. Clone this repo. Use either the CLI git command, or your favorite GUI. (I use [SourceTree](http://sourcetreeapp.com/) by Atlassian)
5. If you checked out using the CLI, type in `git submodule update --init` Skip this if you use [SourceTree](http://sourcetreeapp.com/) , as it does this automatically for you.
6. Run ./sysroot.sh and wait a bit
7. Type "make" to compile.

Notes
------------

Recent builds of Xcode do not have support for the armv6 architecture, which is the CPU architecture found on older iDevices.

This makefile has been modified so that it compiles for armv7. If you have an iOS SDK old enough to support armv6, you may use "makefile-armv6"

FAQs
------------

Q1. I get `-bash: ./sysroot.sh: /usr/local/bin/bash: bad interpreter: No such file or directory` What does this mean?

A1. It means you didn't follow instructions. Make sure you have installed [Homebrew](http://mxcl.github.com/homebrew/) and ran `brew install bash ldid gnu-tar wget xz`

Q2. I get `ld: file is universal (4 slices) but does not contain a(n) armv6 slice: /Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/SDKs/iPhoneOS6.1.sdk/usr/lib/crt1.o for architecture armv6`

A2. You are trying to compile for the armv6 architecture with a recent Xcode build. That doesn't work, sadly.

Q3. The script tells me to "read compiling.txt" ...What?

A3. You messed up somehow. Make sure you have installed [Homebrew](http://mxcl.github.com/homebrew/) and ran `brew install bash ldid gnu-tar wget xz`

Mirrors
------------

This Git repo is avaliable on [GitHub](https://github.com/angelXwind/Cydia-Installer) (main) and [BitBucket](https://bitbucket.org/angelXwind/Cydia-Installer) (mirror).

It was originally cloned from [git://git.saurik.com/cydia.git](git://git.saurik.com/cydia.git) , which is Saurik's own Git repo. Web UI is avaliable here: [http://gitweb.saurik.com/cydia.git](http://gitweb.saurik.com/cydia.git) .