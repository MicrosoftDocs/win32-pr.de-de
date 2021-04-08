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
# <a name="generating-the-stub-files"></a><span data-ttu-id="79056-104">Erstellen der Stubdateien</span><span class="sxs-lookup"><span data-stu-id="79056-104">Generating the Stub Files</span></span>

<span data-ttu-id="79056-105">Nachdem Sie die Client/Server-Schnittstelle definiert haben, entwickeln Sie in der Regel die Quelldateien für Client und Server.</span><span class="sxs-lookup"><span data-stu-id="79056-105">After defining the client/server interface, you usually develop your client and server source files.</span></span> <span data-ttu-id="79056-106">Verwenden Sie als nächstes ein einzelnes Makefile, um die Stub-und Header Dateien zu generieren.</span><span class="sxs-lookup"><span data-stu-id="79056-106">Next use a single makefile to generate the stub and header files.</span></span> <span data-ttu-id="79056-107">Kompilieren und verknüpfen Sie die Client-und Server Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="79056-107">Compile and link the client and server applications.</span></span> <span data-ttu-id="79056-108">Wenn Sie jedoch Ihre erste verfügbar für die verteilte Computerumgebung sind, möchten Sie möglicherweise den Mittelwert des compl-Compilers aufrufen, um zu sehen, was die Mitte generiert, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="79056-108">However, if this is your first exposure to the distributed computing environment, you may want to invoke the MIDL compiler now to see what MIDL generates before you continue.</span></span> <span data-ttu-id="79056-109">Der mittlerer l-Compiler (Midl.exe) wird automatisch installiert, wenn Sie das Platform Software Development Kit (SDK) installieren.</span><span class="sxs-lookup"><span data-stu-id="79056-109">The MIDL compiler (Midl.exe) is automatically installed when you install the Platform Software Development Kit (SDK).</span></span>

<span data-ttu-id="79056-110">Wenn Sie diese Dateien kompilieren, stellen Sie sicher, dass sich die Dateien "Hello. idl" und "Hello. ACF" im selben Verzeichnis befinden.</span><span class="sxs-lookup"><span data-stu-id="79056-110">When you compile these files, make sure that Hello.idl and Hello.acf are in the same directory.</span></span> <span data-ttu-id="79056-111">Mit dem folgenden Befehl werden die Header Datei "Hello. h" und die Client-und Serverstub, "Hello \_ c. c" und "Hello s.c." generiert. \_</span><span class="sxs-lookup"><span data-stu-id="79056-111">The following command will generate the header file Hello.h, and the client and server stubs, Hello\_c.c and Hello\_s.c.</span></span>

<span data-ttu-id="79056-112">**Mittel l Hello. idl**</span><span class="sxs-lookup"><span data-stu-id="79056-112">**midl hello.idl**</span></span>

<span data-ttu-id="79056-113">Beachten Sie, dass "Hello. h" Funktionsprototypen für "helloproc" und "Shutdown" sowie vorwärts Deklarationen für zwei Speicherverwaltungsfunktionen, die Benutzer Zuordnungen " **Mittel l \_ \_** " und " **\_ Benutzer \_ kostenlos**" enthalten.</span><span class="sxs-lookup"><span data-stu-id="79056-113">Notice that Hello.h contains function prototypes for HelloProc and Shutdown, as well as forward declarations for two memory management functions, **midl\_user\_allocate** and **midl\_user\_free**.</span></span> <span data-ttu-id="79056-114">Diese beiden Funktionen werden in der Serveranwendung bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="79056-114">You will provide these two functions in the server application.</span></span> <span data-ttu-id="79056-115">Wenn Daten vom Server an den Client übertragen werden (mithilfe eines \[ **out** - \] Parameters), müssen Sie auch diese beiden Speicherverwaltungsfunktionen in der Client Anwendung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="79056-115">If data were being transmitted from the server to the client (by means of an \[**out**\] parameter) you would also need to provide these two memory management functions in the client application.</span></span>

<span data-ttu-id="79056-116">Beachten Sie die Definitionen für die globale handle-Variable, Hello \_ ifhandle und die Namen der Client-und Server Schnittstellen Handles, Hello \_ v1 \_ 0 \_ c \_ ifspec und Hello \_ v1 \_ 0 \_ s \_ ifspec.</span><span class="sxs-lookup"><span data-stu-id="79056-116">Note the definitions for the global handle variable, hello\_IfHandle, and the client and server interface handle names, hello\_v1\_0\_c\_ifspec and hello\_v1\_0\_s\_ifspec.</span></span> <span data-ttu-id="79056-117">Die Client-und Server Anwendungen verwenden die Namen der Schnittstellen Handles in Lauf Zeit aufrufen.</span><span class="sxs-lookup"><span data-stu-id="79056-117">The client and server applications will use the interface handle names in run-time calls.</span></span>

<span data-ttu-id="79056-118">An diesem Punkt müssen Sie keine Schritte mit den Stubdateien "Hello \_ c. c" und "Hello \_ s.c." durchführen.</span><span class="sxs-lookup"><span data-stu-id="79056-118">At this point, you don't need to do anything with the stub files Hello\_c.c and hello\_s.c.</span></span>

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

 

 




