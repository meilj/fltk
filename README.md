# README - Fast Light Tool Kit (FLTK) Version 1.4.0

## WHAT IS FLTK?

    The Fast Light Tool Kit ("FLTK", pronounced "fulltick") is a
    a cross-platform C++ GUI toolkit for UNIX(r)/Linux(r) (X11),
    Microsoft(r) Windows(r), and MacOS(r) X. FLTK provides
    modern GUI functionality without the bloat and supports 3D
    graphics via OpenGL(r) and its built-in GLUT emulation. It
    was originally developed by Mr. Bill Spitzak and is
    currently maintained by a small group of developers across
    the world with a central repository in the US.


## LICENSING

    FLTK comes with complete free source code. FLTK is available
    under the terms of the GNU Library General Public License.
    Contrary to popular belief, it can be used in commercial
    software! (Even Bill Gates could use it.)


## ON-LINE DOCUMENTATION

    All of the documentation is in HTML in the subdirectory
    "documentation". The "index.html" file should be your
    starting point.  PostScript(tm) and PDF versions of this
    documentation is also available from the FLTK web site at:

        http://www.fltk.org/documentation.php


## BUILDING AND INSTALLING FLTK UNDER UNIX AND Mac OS X

    In most cases you can just type "make".  This will run
    configure with the default (no) options and then compile
    everything.

    FLTK uses GNU autoconf to configure itself for your UNIX
    platform. The main things that the configure script will
    look for are the X11, OpenGL (or Mesa), and JPEG header and
    library files.  Make sure that they are in the standard
    include/library locations.  If they aren't you need to
    define the CFLAGS, CXXFLAGS, and LDFLAGS environment
    variables.

    If you aren't using "gcc", "g++", "c++", or "CC" for your
    C++ compiler, you'll also need to set the CXX environment
    variable. Similarly, if you aren't using "gcc" or "cc" for
    your C compiler you'll need to set the CC environment
    variable.

    You can run configure yourself to get the exact setup you
    need. Type "./configure <options>".  Options include:

	--enable-cygwin         - Enable the Cygwin libraries (Windows)
	--enable-debug          - Enable debugging code & symbols
	--disable-gl            - Disable OpenGL support
	--enable-shared         - Enable generation of shared libraries
	--enable-threads        - Enable multithreading support
	--enable-xdbe           - Enable the X double-buffer extension
	--enable-xft            - Enable the Xft library (anti-aliased fonts)

	--bindir=/path          - Set the location for executables
                        	  [default = /usr/local/bin]
	--libdir=/path          - Set the location for libraries
                        	  [default = /usr/local/lib]
	--includedir=/path      - Set the location for include files.
                        	  [default = /usr/local/include]
	--prefix=/dir           - Set the directory prefix for files
                        	  [default = /usr/local]

    When the configure script is done you can just run the
    "make" command. This will build the library, FLUID tool, and
    all of the test programs.

    To install the library, become root and type "make
    install".  This will copy the "fluid" executable to
    "bindir", the header files to "includedir", and the library
    files to "libdir".

    To install additional files and icons to be used by the main
    desktop environments such as KDE, GNOME and XFCE, you will also
    need to run "make install-desktop" as root.


## SVN USERS

    If you've just checked out a fresh copy of FLTK from SVN,
    you'll need to generate an initial version of 'configure'
    by running 'make makeinclude'. (We don't include a copy
    of configure in svn)


## MAKE TARGETS

    make            -- builds the library + test programs (does not install)
    make install    -- builds and installs
    make clean      -- clean for a rebuild
    make distclean  -- like 'clean', but also removes docs, configure, fltk-config
    ( cd src; make ) -- builds just the fltk libraries


## BUILDING FLTK UNDER MICROSOFT WINDOWS

    There are two ways to build FLTK under Microsoft Windows.
    The first is to use the Visual C++ project files under the
    "ide/" directory.  See the file ide/README.IDE for more info.

    The second method is to use a GNU-based development tool.
    To build with the Cygwin or MinGW tools, use the supplied
    configure script as specified in the UNIX section above:

        sh configure ...options...


## BUILDING HTML DOCUMENTATION

    If you want to build the HTML documentation:

    	( cd documentation && make html )

    If you want to build the PDF documentation:

    	( cd documentation && make pdf )

    FLTK uses doxygen for documentation, so you'll at least need doxygen
    installed for creating html docs, and LaTeX for creating PDF docs.


## INTERNET RESOURCES

    FLTK is available on the 'net in a bunch of locations:

	- WWW:   http://www.fltk.org/
	         http://www.fltk.org/str.php [for reporting bugs]
	         http://www.fltk.org/software.php [source code]

    To join the FLTK mailing list, go the following web page:

        http://www.fltk.org/newsgroups.php

## REPORTING BUGS

    To report a bug in FLTK, use the form at:

        http://www.fltk.org/str.php

    For general support and questions, please use the FLTK
    mailing list at "fltk@fltk.org".


## TRADEMARKS

    Microsoft and Windows are registered trademarks of Microsoft
    Corporation. UNIX is a registered trademark of the X/Open
    Group, Inc.  OpenGL is a registered trademark of Silicon
    Graphics, Inc.  Mac OS is a registered trademark of Apple
    Computers, Inc.


## COPYRIGHT

    FLTK is copyright 1998-2016 by Bill Spitzak and others,
    see the CREDITS file for more info.

    This library is free software. Distribution and use rights are
    outlined in the file "COPYING" which should have been included with
    this file.  If this file is missing or damaged, see the license at:

        http://www.fltk.org/COPYING.php
