# CS-in-Python
This repository is dedicated for achieving the installation procedures of the tools used in the following blog
http://www.pyrunner.com/weblog/2016/05/26/compressed-sensing-python/

Copyright (c) 2017 Cheng Chi Tsun

We assume you are working a fresh installation of Ubuntu.

1. Download libLBFGS (http://www.chokkan.org/software/liblbfgs/ > Under "Source Code")
  https://github.com/downloads/chokkan/liblbfgs/liblbfgs-1.10.tar.gz
2. Downlaod Libtool (https://www.gnu.org/software/libtool/ > Under "Downloading GNU Libtool")
  http://ftpmirror.gnu.org/libtool/libtool-2.4.6.tar.gz
3. Clone pylbfgs (https://bitbucket.org/rtaylor/pylbfgs)
  git clone https://bitbucket.org/rtaylor/pylbfgs.git
  
Extract all of them to your working directory.

You should now see the following directories by typing 'ls'

i. libtool-2.4.2
ii. liblbfgs-1.10
iii. pylbfgs

Step 1. Install libtool

cd libtool-2.4.2
./configure
make
sudo make install

Step 2. Install libtool

sudo apt-get install g++ gfortran build-essential automake python-dev 
sudo apt-get install python-setuptools python-numpy
  
cd ..
cd liblbfgs-1.10
./configure --enable-sse2
make
sudo make install
  
Step 3. Install pylbfgs
 
cd ..
cd pylbfgs
python setup.py install

