# aarch64-wheels
Pre-compiled python wheels for arm64 linux devices running 16.04 LTS (Xenial) on python 3.5

### Make sure you have the latest pip3 that supports wheel
curl -sS https://bootstrap.pypa.io/get-pip.py | sudo python3

### Install wheel
pip3 install wheel

### Make a 'wheelhouse' directory to store wheels
mkdir /tmp/wheelhouse

cd /tmp/wheelhouse

### Find appropriate wheel and download file to wheelhouse directory
wget -O https://github.com/mrjonandrews/aarch64-wheels/tree/master/wheelhouse/numpy-1.14.2-cp35-cp35m-linux_aarch64.whl

### Install
pip3 install --use-wheel --no-index --find-links=/tmp/wheelhouse numpy

or

pip3 install numpy-1.14.2-cp35-cp35m-linux_aarch64.whl

or

### Install from cached wheels remotely
pip3 install --use-wheel --no-index --find-links=https://github.com/mrjonandrews/aarch64-wheels/tree/master/wheelhouse numpy

# If you wanted to optionally build your own directory of wheels for numpy and all its dependencies (replace numpy with whatever package you want to install)
pip3 wheel --wheel-dir=/tmp/wheelhouse numpy
