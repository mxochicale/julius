Installation
-----------



[MAIN REFERENCE](http://www.voxforge.org/home/docs/faq/faq/how-to-compile-julius/julian-from-source)


* Step 1 - Download and Install Julius

```
$ mkdir bin
$ wget https://osdn.jp/projects/julius/downloads/60273/julius-4.3.1.tar.gz/ -O julius-4.3.1.tar.gz
$tar -xvzf julius-4.3.1.tar.gz
```


```
$ ./configure --with-mictype=alsa --enable-setup=standard --prefix=~/bin/julius-4.3.1
$ make all
$ make install
```




* Step 3 - testing

```
$ gedit ~/ .bashrc

# User specific environment and startup programs
PATH=$PATH:$HOME/voxforge/bin/htk/bin:
$HOME/voxforge/bin/julius-4.3.1-linuxbin/bin
```




```
map479-admin@eee320:~$ julius
Julius rev.4.3.1 - based on
JuliusLib rev.4.3.1 (standard)  built for x86_64-unknown-linux-gnu

Copyright (c) 1991-2013 Kawahara Lab., Kyoto University
Copyright (c) 1997-2000 Information-technology Promotion Agency, Japan
Copyright (c) 2000-2005 Shikano Lab., Nara Institute of Science and Technology
Copyright (c) 2005-2013 Julius project team, Nagoya Institute of Technology

Try '-setting' for built-in engine configuration.
Try '-help' for run time options.
```




```
**NOTE I DID NOT USE the  alsa-lib-devel.i686 for installation
** To compile 32-bit Julius on a 64-bit computer:
you will need the .686 version of alsa-lib as root:
# yum install alsa-lib-devel.i686
then add a flag before you run the Julius configure to tell your gcc compiler to compile 32-bit binaries:
$ CFLAGS=-m32  ./configure --with-mictype=alsa --enable-setup=standard --prefix=~/bin/julius-4.3.1 --host=i686-generic-linux-gnu
```
