# deadstores
A Valgrind tool for finding redundant loads/stores. Documentation is available in the blog post “[Watching for software inefficiencies with Valgrind](https://kristerw.blogspot.com/2020/02/watching-for-software-inefficiencies.html)”.

# How to install
Install in `$HOME/valgrind` by running the commands
```
wget https://sourceware.org/pub/valgrind/valgrind-3.15.0.tar.bz2
tar xf valgrind-3.15.0.tar.bz2
cd valgrind-3.15.0
git clone https://github.com/kristerw/deadstores
patch -p1 < deadstores/patches/valgrind-3.15.0.patch
./autogen.sh
./configure --prefix=$HOME/valgrind
make -j`nproc`
make install
```
