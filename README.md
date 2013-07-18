CMUSV-GnuRadio
==============


# Installation
The official gnuradio website does provide serveral ways to install gnuradio on your machine. Please feel free to follow 
the [guide](http://gnuradio.org/redmine/projects/gnuradio/wiki/InstallingGR). However, this guide is specifically written
for providing step-by-step installation on Ubuntu 12.10. It also includes UHD and gnuradio installation.

### Steps
1. [Prerequisites and Dependencies](#Prerequisites and Dependencies)
2. [Install uhd](#UHD)
2. Install gnuradio
3. Run "Hello world"

<a name="Prerequisites and Dependencies"/>
## Prerequisites and Dependencies
See [full version](http://gnuradio.org/redmine/projects/gnuradio/wiki/UbuntuInstall#Install-Dependencies)

```
$ sudo apt-get -y install git-core autoconf automake  libtool g++ python-dev swig \
pkg-config libboost-all-dev libfftw3-dev libcppunit-dev libgsl0-dev \
libusb-dev sdcc libsdl1.2-dev python-wxgtk2.8 python-numpy \
python-cheetah python-lxml doxygen python-qt4 python-qwt5-qt4 libxi-dev \
libqt4-opengl-dev libqwt5-qt4-dev libfontconfig1-dev libxrender-dev \
libcomedi-dev python-docutils cmake python-setuptools
``` 

If you want to enable gr-comedi, run the following command:
```
$ sudo apt-get install libcomedi0
```
You might need python interface to work with libcomedi. See [full guide](https://pypi.python.org/pypi/pycomedi/).
Run the follwing command:
```
$ easy_install cython
$ git clone git://tremily.us/pycomedi.git
$ python setup install
```

If you want to enable sphinx, run the following command"
```
$ easy_install -U Sphinx
```
<a name="UHD"/>
## UHD Installation


-------------------------

pdns issue
	if you are using ubuntu 12.04, you might find the issue "pdns-recursor" because of port 53 is already in use. To fix this, stop the running dns service by using the following command:
		sudo /etc/init.d/pdns stop



1 install UHD before GNU
(http://code.ettus.com/redmine/ettus/projects/uhd/wiki/UHD_Build)

1.1 Clone the repository
	git clone git://github.com/EttusResearch/uhd.git

1.2 Folllow the instruction
http://files.ettus.com/uhd_docs/manual/html/build.html



2. Install GNU Radio
http://gnuradio.org/redmine/projects/gnuradio/wiki/BuildGuide

make sure that we set
LD_LIBRARY_PATH=/usr/local/lib
(or antther directory)


## Run Hello World
