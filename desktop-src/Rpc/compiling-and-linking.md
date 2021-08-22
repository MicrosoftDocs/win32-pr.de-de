---
title: Kompilieren und Verknüpfen
description: Das folgende Makefile zeigt die Abhängigkeiten zwischen den Dateien, die zum Kompilieren der Client- und Serveranwendungen erforderlich sind, und verknüpfen sie mit der RPC-Laufzeitbibliothek und der C-Standardlaufzeitbibliothek.
ms.assetid: 9182baea-7307-4db0-8d66-7fba14227ac9
keywords:
- Remoteprozeduraufruf RPC , Tasks, Kompilieren und Verknüpfen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2500a763db149eca914060dd7920548883fa57fbd5642485a41f5a55c65cd2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118931713"
---
# <a name="compiling-and-linking"></a>Kompilieren und Verknüpfen

Das folgende Makefile zeigt die Abhängigkeiten zwischen den Dateien, die zum Kompilieren der Client- und Serveranwendungen erforderlich sind, und verknüpfen sie mit der RPC-Laufzeitbibliothek und der C-Standardlaufzeitbibliothek.

Dieses Makefile kann verwendet werden, um Client- und Serveranwendungen aus dem Quellcode in diesem Tutorial zu erstellen. Die hier gezeigten Stubs und Header wurden mit MIDL Version 2.0 generiert. Die Compiler- und Linkerbefehle und -argumente können sich für Ihre Computerkonfiguration unterscheiden. Weitere Informationen finden Sie in der Compilerdokumentation.

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

 

 




