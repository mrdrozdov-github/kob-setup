# Install

Look to https://github.com/tuotuoxp/cpp-torch/blob/master/install.md for inspiration.

```
# Torch / TH
git clone git@github.com:torch/torch7.git
mkdir build
cd build
# I had to modify CMakeLists.txt for this to work.
cmake -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/Users/Andrew/Developer/kob-setup ../lib/TH
make
make install

# Torch / THNN
git clone git@github.com:torch/nn.git
mkdir build
cd build
cmake -DCMAKE_BUILD_TYPE=Release \
-DCMAKE_INSTALL_PREFIX=/Users/Andrew/Developer/kob-setup \
-DCMAKE_PREFIX_PATH=/Users/Andrew/Developer/kob-setup ../lib/THNN
# I had to modify CMakeLists.txt for this to work.
make
make install

# Was necessary to run examples:
export LD_LIBRARY_PATH=/Users/Andrew/Developer/kob-setup/lib:$LD_LIBRARY_PATH
export LD_LIBRARY_PATH=/Users/Andrew/anaconda/lib:$LD_LIBRARY_PATH
```
