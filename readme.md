# Ejecuion de Kernel Module

## Available Scripts

Para la ejecucion del modulo kernel se requieren una serie de pasos especificos:

### `Descargar y descomprimir el codigo fuente`

Se debe descargar y descomprimir el codigo fuente que se desea compilar con el kernel ya sea utilizando un comando como `unzip module.zip`

Seguido de esto dirijase al directorio donde se descomprimio el codigo fuente

### `Compilar modulo kernel`

Para compilar el codigo fuente es necesario tener instalado [make](https://linuxhint.com/install-make-ubuntu/).

Una vez teniendo `make` instalado se ejecuta `make` en el directorio del modulo para iniciar el proceso de compilacion. Esto creara un binario que se puede cargar al kernel.

Si consideras necesario mas velocidad al compilar puedes ejecutar `make -j x` donde **x** es el numero de cores que deseas asignar al proceso.

### `Instalar modulo en el kernel`

Para cargar/instalar el modulo en el kernel se debe ejecutar `sudo make install` lo cual copiara el binario creado en el paso anterior hacia el directorio correspondiente en tu sistema.

### `Habilitar modulo kernel`

Finalemte, para habiliar el Modulo Kernel es necesario ejecutar `modprobe module` lo cual cargara el modulo en el kernel del sistema.

### `Ejecutar programa de prueba`



## Pasos adicionales

### `Habilitar modulo kernel en boot`

Si se desea habilitar el modulo cada vez que se haga un boot nuevo es necesario agregar el nombre del modulo en el archivo `modules` ubicado en `/etc/modules`. Unicamente se requiere agregar una vez el nombre del modulo en el archivo y asegurarse de que solo sea 1 modulo por linea.