### fftw单精度  

```sh
./configure --enable-float --prefix=/es01/yeesuan/yeesuan003/lhxone-test/software/fftw3 CC=gcc F77=gfortran --enable-shared --enable-static --enable-sse --enable-sse2 --enable-avx --enable-avx2 --enable-fma --enable-mpi --enable-threads --enable-openmpi
```

### fftw双精度  

```sh
./configure --prefix=/es01/yeesuan/yeesuan003/lhxone-test/software/fftw3 CC=gcc F77=gfortran --enable-shared --enable-static --enable-sse2 --enable-avx --enable-avx2 --enable-fma --enable-mpi --enable-threads --enable-openmp
```

#### 配置环境变量

```shell
export PATH=/es01/yeesuan/yeesuan003/lhxone-test/software/fftw3/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/es01/yeesuan/yeesuan003/lhxone-test/software/fftw3/lib
export C_INCLUDE_PATH=$C_INCLUDE_PATH:/es01/yeesuan/yeesuan003/lhxone-test/software/fftw3/include
```

### 配置pgplot环境变量

```shell
export PGPLOT_DIR=/es01/yeesuan/yeesuan003/source/pgplot
export PGPLOT_DEV=/Xserve
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/es01/yeesuan/yeesuan003/source/pgplot/lib
export C_INCLUDE_PATH=$C_INCLUDE_PATH:/es01/yeesuan/yeesuan003/source/pgplot/include
export PGPLOT_FONT=/es01/yeesuan/yeesuan003/source/pgplot/grfont.dat
export PGPLOT_LIB="-L/es01/yeesuan/yeesuan003/lhxone-test/software/X11_inc -lX11 -L /es01/yeesuan/yeesuan003/source/pgplot -lpgplot"
```

### tempo2配置

```shell
./configure --prefix=/es01/yeesuan/yeesuan003/lhxone-test/software/tempo2

make && make install

export TEMPO2=/es01/yeesuan/yeesuan003/lhxone-test/software/tempo2
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/es01/yeesuan/yeesuan003/lhxone-test/software/tempo2/lib
export C_INCLUDE_PATH=$C_INCLUDE_PATH:/es01/yeesuan/yeesuan003/lhxone-test/software/tempo2/include
```

### libffi

```/es01/yeesuan/yeesuan003/lhxone-test/software/libffi```

```sh
export LIBFFI=/es01/yeesuan/yeesuan003/lhxone-test/software/libffi
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/es01/yeesuan/yeesuan003/lhxone-test/software/libffi/lib64
export C_INCLUDE_PATH=$C_INCLUDE_PATH:/es01/yeesuan/yeesuan003/lhxone-test/software/libffi/include
```

### glib

```sh
./configure --prefix=/es01/yeesuan/yeesuan003/lhxone-test/software/glib LIBFFI_CFLAGS=-I/es01/yeesuan/yeesuan003/lhxone-test/software/libffi/include LIBFFI_LIBS='-L/es01/yeesuan/yeesuan003/lhxone-test/software/libffi/lib64/ -lffi'
```

环境变量

```sh
cp /es01/yeesuan/yeesuan003/lhxone-test/software/glib/lib/glib-2.0/include/glibconfig.h /es01/yeesuan/yeesuan003/lhxone-test/software/glib/include/glib-2.0/
export GLIB=/es01/yeesuan/yeesuan003/lhxone-test/software/glib
export PATH=/es01/yeesuan/yeesuan003/lhxone-test/software/glib/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/es01/yeesuan/yeesuan003/lhxone-test/software/glib/lib
export C_INCLUDE_PATH=$C_INCLUDE_PATH:/es01/yeesuan/yeesuan003/lhxone-test/software/glib/include
```

测试glib

```c
#include <stdio.h>
#include "glib.h"

int main(){
    g_printf("hello world\n");
    return 0;
}
```

```shell
gcc -o glibtest glibtest.c -I/es01/yeesuan/yeesuan003/lhxone-test/software/glib/include/glib-2.0 -L/es01/yeesuan/yeesuan003/lhxone-test/software/glib/lib -lglib-2.0
```


### curl

```sh
./configure --prefix=/es01/yeesuan/yeesuan003/lhxone-test/software/curl --without-ssl
make -j && make install
```

环境变量设置

```sh
export PATH=/es01/yeesuan/yeesuan003/lhxone-test/software/curl/bin${PATH:+:${PATH}}
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/es01/yeesuan/yeesuan003/lhxone-test/software/curl/lib
export C_INCLUDE_PATH=$C_INCLUDE_PATH:/es01/yeesuan/yeesuan003/lhxone-test/software/curl/include
```

### cfitsio

```sh
./configure --prefix=/es01/yeesuan/yeesuan003/lhxone-test/software/cfitsio
```



### libpng

/es01/yeesuan/yeesuan003/lhxone-test/software/libpng

### presto

```sh
export PRESTO=/es01/yeesuan/yeesuan003/source/presto-4.0
export PYTHONPATH=/es01/yeesuan/yeesuan003/source/presto-4.0/lib/python
export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/es01/yeesuan/yeesuan003/source/presto-4.0/lib
export C_INCLUDE_PATH=$C_INCLUDE_PATH:/es01/yeesuan/yeesuan003/source/presto-4.0/include
```



