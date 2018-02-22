# CS-in-Python
This repository is dedicated for installing the tools used in examples in the following link
http://www.pyrunner.com/weblog/2016/05/26/compressed-sensing-python/

We assume you are working on a fresh installation of Ubuntu 16.04.

1. Download libLBFGS (http://www.chokkan.org/software/liblbfgs/ > Under "Source Code")
  https://github.com/downloads/chokkan/liblbfgs/liblbfgs-1.10.tar.gz
2. Downlaod Libtool (https://www.gnu.org/software/libtool/ > Under "Downloading GNU Libtool")
  http://ftpmirror.gnu.org/libtool/libtool-2.4.6.tar.gz
3. Clone pylbfgs (https://bitbucket.org/rtaylor/pylbfgs)
  git clone https://bitbucket.org/rtaylor/pylbfgs.git
  
Extract all of them to your working directory.
```
tar -xvzf liblbfgs-1.10.tar.gz
tar -xvzf libtool-2.4.6.tar.gz
```
You should now see the following directories in your working directory.

- libtool-2.4.6
- liblbfgs-1.10
- pylbfgs

**Step 1. Install libtool**
```
cd libtool-2.4.6
./configure
make
sudo make install
```
**Step 2. Install libtool**
```
sudo apt-get install -y g++ gfortran build-essential automake python3 python3-pip python3-dev python3-setuptools python3-numpy python3-tk python3-scipy python3-pillow python3-matplotlib
cd ..
cd liblbfgs-1.10
./configure --enable-sse2
make
sudo make install
```
**Step 3. Install pylbfgs**
``` 
cd ..
cd pylbfgs
python3 setup.py install
```
