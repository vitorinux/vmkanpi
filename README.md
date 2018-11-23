# vmkanpi
# Install from source Kannel 1.4.5 on RPI 3 model B+

Introduction

	The Kannel Open Source WAP and SMS gateway works as both an SMS
	gateway, for implementing keyword based services via GSM text
	messages, and a WAP gateway, via UDP. The SMS part is fairly
	mature, the WAP part is early in its development. In this release,
	the GET request for WML pages and WMLScript files via HTTP works,
	including compilation for WML and WMLScript to binary forms. Only
	the data call bearer (UDP) is supported, not SMS.
Requirements

	You need a Unix-like operating system that supports POSIX threads
	(pthreads.h). We use RedHat/CentOS Linux and Debian/Ubuntu GNU/Linux 
	systems as main targets.
    
	There is also support for the Cygwin POSIX emulation layer for the 
	Win32 platforms.
	
	You need GNU make, other make's tend not to work. For example,
	the FreeBSD and Solaris versions of make do not work. Check the
	version of your make with "make --version"; if it does not reply
	with "GNU Make version x.y.z", then it is not GNU make.
	
	On Solaris, you probably want to install gcc, GNU make and GNU
	binutils from www.sunfreeware.com.
	
	On MacOS X, you may have problems in compiling the latest libxml
	(2.4.23). There may be linking errors for those library. A work-
	arround is either using an older version of libxml (2.3.9 for 
	example) or to build it as static library without the dynamic one 
	being built.
   Raspbian Stretch Lite (2018-11-13)
	
        $ sudo apt install openjade jadetex transfig imagemagick docbook-dsssl docbook-utils zlibc
