# autotools template

This repository contains an autotools template project.

## Bootstrap the build infrastructure

- Run `autoscan` and rename `configure.scan` to `configure.ac`.
- Run `autoconf`.
- Add 'AM_INIT_AUTOMAKE([-Wall])' after 'AC_INIT'
- Update Makefile.am files
- Generate the `configure` script using `aclocal`
- Run `autoreconf -fi` to generate `config.h.in`
- Generate the `Makefile.in` using `automake --add-missing`
- Run `autoconf` to generate final configure script

## Init after checkout

``` sh
aclocal
autoreconf -fi
automake --add-missing
autoconf
``` 

## Build and install

``` sh
./configure
make
sudo make install
```

## uninstall

``` sh
sudo make uninstall
```

## References

[1] https://en.terminalroot.com.br/gnu-autotools-ultimate-tutorial-for-beginners/
[2] https://elinux.org/images/4/43/Petazzoni.pdf

