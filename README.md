- REF: https://software.intel.com/sites/landingpage/IntrinsicsGuide/
- REF: https://www.uv.es/varnau/OC_T4.pdf
- REF: http://repository.udistrital.edu.co/bitstream/11349/8019/1/VeraParraNelsonEnrique2018.pdf

### Conjuntos de instrucciones SIMD
~~~
- mmx       64 bit (int)
- sse      128 bit
- sse   2  128 bit
- sse   3  128 bit
- sse 4.1  128 bit
- sse 4.2  128 bit
- avx      256 bit
- avx   2  256 bit
- avx 512  512 bit
~~~ 

### Ver modelo de la cpu
~~~
$ cat /proc/cpuinfo| grep 'model name' | head -n 1
~~~

### Ver Numero de cores / núcleos
~~~
$ cat /proc/cpuinfo| grep cores | head -n 1
~~~

~~~
    Núcleos es un término de hardware que describe el número
de unidades de procesamiento independientes en un componente
computacional individual (matriz o chip).
~~~

### Cantidad de subprocesos
~~~
$ cat /proc/cpuinfo| grep 'process' | wc -l
~~~

~~~
    Un hilo, o hilo de ejecución, es un término de software
para la secuencia de instrucciones de orden básico que puede
pasar por o procesarse en un núcleo de CPU individual.
~~~

### Cantidad de subprocesos por núcleo
~~~
$ cat /proc/cpuinfo| grep 'core id' | sort --unique | wc -l
~~~

### Ver tecnologias que soporta el núcleo
~~~
$ cat /proc/cpuinfo| grep flags | head -n 1
~~~
