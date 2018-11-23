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
	Raspbian Stretch Lite (2018-11-13)

        sudo apt install openjade jadetex transfig imagemagick docbook-dsssl docbook-utils zlibc libxml2-dev byacc
        
        # bison (GNU Bison) 2.5.1
        (You should use 2.5.1 version of BISON because apt-get version doesn't work)
        wget http://ftp.gnu.org/gnu/bison/bison-2.5.1.tar.gz and make (YOU SHOULD USE THIS VERSION apt doesn't works)
        tar xvf bison-2.5.1.tar.gz
        cd bison-2.5.1
        ./configure
        make && sudo make install


Configure Source
	For this "workbench" we will enable DEBUG mode and StartStop daemon, you can view a full list of options to configure as well in Kannel's UserGuide
	    
    CFLAGS='-pthread' ./configure --enable-debug --enable-start-stop-daemon

MaKe

	touch .depend
	make depend
	make -j4
	make 
	make depend
	


