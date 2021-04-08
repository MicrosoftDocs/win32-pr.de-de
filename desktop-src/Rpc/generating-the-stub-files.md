---
title: Erstellen der Stubdateien
description: Nachdem Sie die Client/Server-Schnittstelle definiert haben, entwickeln Sie in der Regel die Quelldateien für Client und Server.
ms.assetid: e4d08bee-ab9a-4426-a1af-72a7d763797f
keywords:
- Remote Prozedur Aufruf RPC, Tasks, Erstellen von Stub-Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e092663711be60a3a0dc0dd8a4e99c0fa92a3ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856068"
---
# <a name="generating-the-stub-files"></a>Erstellen der Stubdateien

Nachdem Sie die Client/Server-Schnittstelle definiert haben, entwickeln Sie in der Regel die Quelldateien für Client und Server. Verwenden Sie als nächstes ein einzelnes Makefile, um die Stub-und Header Dateien zu generieren. Kompilieren und verknüpfen Sie die Client-und Server Anwendungen. Wenn Sie jedoch Ihre erste verfügbar für die verteilte Computerumgebung sind, möchten Sie möglicherweise den Mittelwert des compl-Compilers aufrufen, um zu sehen, was die Mitte generiert, bevor Sie fortfahren. Der mittlerer l-Compiler (Midl.exe) wird automatisch installiert, wenn Sie das Platform Software Development Kit (SDK) installieren.

Wenn Sie diese Dateien kompilieren, stellen Sie sicher, dass sich die Dateien "Hello. idl" und "Hello. ACF" im selben Verzeichnis befinden. Mit dem folgenden Befehl werden die Header Datei "Hello. h" und die Client-und Serverstub, "Hello \_ c. c" und "Hello s.c." generiert. \_

**Mittel l Hello. idl**

Beachten Sie, dass "Hello. h" Funktionsprototypen für "helloproc" und "Shutdown" sowie vorwärts Deklarationen für zwei Speicherverwaltungsfunktionen, die Benutzer Zuordnungen " **Mittel l \_ \_** " und " **\_ Benutzer \_ kostenlos**" enthalten. Diese beiden Funktionen werden in der Serveranwendung bereitgestellt. Wenn Daten vom Server an den Client übertragen werden (mithilfe eines \[ **out** - \] Parameters), müssen Sie auch diese beiden Speicherverwaltungsfunktionen in der Client Anwendung bereitstellen.

Beachten Sie die Definitionen für die globale handle-Variable, Hello \_ ifhandle und die Namen der Client-und Server Schnittstellen Handles, Hello \_ v1 \_ 0 \_ c \_ ifspec und Hello \_ v1 \_ 0 \_ s \_ ifspec. Die Client-und Server Anwendungen verwenden die Namen der Schnittstellen Handles in Lauf Zeit aufrufen.

An diesem Punkt müssen Sie keine Schritte mit den Stubdateien "Hello \_ c. c" und "Hello \_ s.c." durchführen.

``` syntax
/*file: hello.h */
/* this ALWAYS GENERATED file contains the definitions for the interfaces */
/* File created by MIDL compiler version 3.00.06 
/* at Tue Feb 20 11:33:32 1996 */
/* Compiler settings for hello.idl:
    Os, W1, Zp8, env=Win32, ms_ext, c_ext
    error checks: none */
//@@MIDL_FILE_HEADING(  )
#include "Rpc.h"
#include "rpcndr.h"
 
#ifndef __hello_h_
#define __hello_h_
 
#ifdef __cplusplus
extern "C"{
#endif 
 
/* Forward Declarations */ 
 
void __RPC_FAR * __RPC_USER MIDL_user_allocate(size_t);
void __RPC_USER MIDL_user_free( void __RPC_FAR * ); 
 
#ifndef __hello_INTERFACE_DEFINED__
#define __hello_INTERFACE_DEFINED__
 
/****************************************
 * Generated header for interface: hello
 * at Tue Feb 20 11:33:32 1996
 * using MIDL 3.00.06
 ****************************************/
/* [implicit_handle][version][uuid] */ 
 
            /* size is 0 */
void HelloProc( 
    /* [string][in] */ unsigned char __RPC_FAR *pszString);
    /* size is 0 */
void Shutdown( void);
extern handle_t hello_IfHandle;
 
extern RPC_IF_HANDLE hello_v1_0_c_ifspec;
extern RPC_IF_HANDLE hello_v1_0_s_ifspec;
#endif /* __hello_INTERFACE_DEFINED__ */
 
/* Additional Prototypes for ALL interfaces */
/* end of Additional Prototypes */
#ifdef __cplusplus
}
#endif
#endif
```

 

 




