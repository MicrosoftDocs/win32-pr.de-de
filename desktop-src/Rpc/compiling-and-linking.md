---
title: Kompilieren und verknüpfen
description: Das folgende Makefile zeigt die Abhängigkeiten zwischen den Dateien, die erforderlich sind, um die Client-und Server Anwendungen zu kompilieren und Sie mit der RPC-Lauf Zeit Bibliothek und der Standard-C-Lauf Zeit Bibliothek zu verknüpfen.
ms.assetid: 9182baea-7307-4db0-8d66-7fba14227ac9
keywords:
- Remote Prozedur Aufruf RPC, Tasks, kompilieren und verknüpfen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1991e39cc028c01066cd8f13344765787374fa08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947778"
---
# <a name="compiling-and-linking"></a>Kompilieren und verknüpfen

Das folgende Makefile zeigt die Abhängigkeiten zwischen den Dateien, die erforderlich sind, um die Client-und Server Anwendungen zu kompilieren und Sie mit der RPC-Lauf Zeit Bibliothek und der Standard-C-Lauf Zeit Bibliothek zu verknüpfen.

Dieses Makefile kann zum Erstellen von Client-und Server Anwendungen aus dem Quellcode in diesem Tutorial verwendet werden. Die hier gezeigten stubzeilen und Header wurden mit der mittleren l-Version 2,0 generiert. Die Befehle und Argumente des Compilers und des Linkers unterscheiden sich möglicherweise für die Computerkonfiguration. Weitere Informationen finden Sie in der Compilerdokumentation.

``` syntax
#makefile for helloc.exe and hellos.exe
#link refers to the linker
#conflags refers to flags for console applications
#conlibs refers to libraries for console applications
 
!include <ntwin32.mak>
 
all : helloc hellos
 
# Make the client side application helloc
helloc : helloc.exe
helloc.exe : helloc.obj hello_c.obj
    $(link) $(linkdebug) $(conflags) -out:helloc.exe \
        helloc.obj hello_c.obj \
        rpcrt4.lib $(conlibs)
 
# helloc main program
helloc.obj : helloc.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvars) $*.c
 
# helloc stub
hello_c.obj : hello_c.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvars) $*.c
 
# Make the server side application
hellos : hellos.exe
hellos.exe : hellos.obj hellop.obj hello_s.obj
    $(link) $(linkdebug) $(conflags) -out:hellos.exe \
        hellos.obj hello_s.obj hellop.obj \
        rpcrt4.lib $(conlibsmt)
 
# hello server main program
hellos.obj : hellos.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# remote procedures
hellop.obj : hellop.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# hellos stub file
hello_s.obj : hello_s.c hello.h
    $(cc) $(cdebug) $(cflags) $(cvarsmt) $*.c
 
# Stubs and header file from the IDL file
hello.h hello_c.c hello_s.c : hello.idl hello.acf
    midl hello.idl
```

 

 




