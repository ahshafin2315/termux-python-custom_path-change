# Python 3.13 for Termux

This is a fork of [termux-change]() by [yubrajbhoi]() with Termux patches (`termux.patch`) applied.

But first make sure you have these dependencies installed with `apt` or `pkg`:

 - `python`, this will install all dependencies needed to build `python-3.13.1`. You can later remove the python pkg ensuring not removing the dependencies.
 - `build-essential`, this will install `clang`, `make` etc.
 - `stow`, to install the package after building it.

After that the package can be build with: `bash build.sh`. That will build and install it in `python-3.13.1` directory in $HOME.

You can install that directory with `stow` like this:

```
mkdir -p $PREFIX/stow
mv $HOME/python-3.13.1 $PREFIX/stow/
cd $PREFIX/stow
stow -v --stow python-3.13.1
```
