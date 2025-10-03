---
layout: lecture
date: 2023-02-03
title: strace
description: Herramientas para debbugear programas
ready: false
---


>  `strace` es  una herramienta que permite ver las *system calls* que un programa ejecuta. Es una herramienta para diagnosticar y debugear un ejecutable.

strace no muestra `library calls`, para eso existen otras herramientas como `ltrace`.

## Uso:
```shell
strace  <flags>  <programa>
```

## Strace flags
```shell
strace  <flags>  <programa>
```

Algunas flags:
- `-f` :
- `-s` : string length.
- `-t` :
- `-T` :
- `-y` : decode file descriptors (id numbers asigned to file when open).
- `-yy`:
- `-q` :
- `-v` :
- `-o` *file*: escribe la salida en el archivo *file*.


## `system calls` importantes:

+ `int open()`
+ `int close()`
+ `ssize_t read()`
+ `ssize_t write()`
+ `pid_t fork()`: crea un nuevo proceso. Hoy en dia es una `library call`. Retorna un `PID`. On success the PID of the parent is returned in the parent thread, and 0 is returned to the child's thread.
+ `int clone()`     : crea un nuevo proceso/thread. Más flexible
+ `pid_t wait4()`   : waiting for changes on the state of the child.
+ `int execve()`    : execute the program pointed to by filename. 
+ `int exit_group()`: 


