---
title: Die Server Anwendung
description: Das folgende Beispiel ist aus der "Hallo Welt"-Anwendung im Verzeichnis "RPC \\ Hello" des Platform Software Development Kit (SDK).
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e6f13e2c8fecdcff820c62f3076dd2a8edd1a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856196"
---
# <a name="the-server-application"></a><span data-ttu-id="ef006-103">Die Server Anwendung</span><span class="sxs-lookup"><span data-stu-id="ef006-103">The Server Application</span></span>

<span data-ttu-id="ef006-104">Das folgende Beispiel ist aus der "Hallo Welt"-Anwendung im Verzeichnis "RPC \\ Hello" des Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="ef006-104">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="ef006-105">Die Serverseite der verteilten Anwendung informiert das System darüber, dass die zugehörigen Dienste verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="ef006-105">The server side of the distributed application informs the system that its services are available.</span></span> <span data-ttu-id="ef006-106">Dann wartet er auf Client Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="ef006-106">It then waits for client requests.</span></span> <span data-ttu-id="ef006-107">Der mittlerer l-Compiler muss mit dem folgenden Beispiel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ef006-107">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="ef006-108">Abhängig von der Größe Ihrer Anwendung und ihren Codierungs Einstellungen können Sie auswählen, dass Remote Prozeduren in einer oder mehreren separaten Dateien implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="ef006-108">Depending on the size of your application and your coding preferences, you can choose to implement remote procedures in one or more separate files.</span></span> <span data-ttu-id="ef006-109">In diesem Tutorial-Programm enthält die Quelldatei hellos. c die Hauptserver Routine.</span><span class="sxs-lookup"><span data-stu-id="ef006-109">In this tutorial program, the source file Hellos.c contains the main server routine.</span></span> <span data-ttu-id="ef006-110">Die Datei hellop. c enthält die Remote Prozedur.</span><span class="sxs-lookup"><span data-stu-id="ef006-110">The file Hellop.c contains the remote procedure.</span></span>

<span data-ttu-id="ef006-111">Der Vorteil der Organisation der Remote Prozeduren in separaten Dateien besteht darin, dass die Prozeduren mit einem eigenständigen Programm verknüpft werden können, um den Code vor der Konvertierung in eine verteilte Anwendung zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="ef006-111">The benefit of organizing the remote procedures in separate files is that the procedures can be linked with a standalone program to debug the code before it is converted to a distributed application.</span></span> <span data-ttu-id="ef006-112">Wenn die Prozeduren im eigenständigen Programm funktionieren, können Sie die Quelldateien, die die Remote Prozeduren enthalten, mit der Serveranwendung kompilieren und verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="ef006-112">After the procedures work in the standalone program, you can compile and link the source files containing the remote procedures with the server application.</span></span> <span data-ttu-id="ef006-113">Wie bei der Quelldatei der Client Anwendung muss die Quelldatei für die Serveranwendung die Header Datei "Hello. h" enthalten.</span><span class="sxs-lookup"><span data-stu-id="ef006-113">As with the client-application source file, the server-application source file must include the Hello.h header file.</span></span>

<span data-ttu-id="ef006-114">Der Server Ruft die RPC-Lauf Zeitfunktionen [**rpcserveruseprotabqep**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) und [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) auf, um dem Client Bindungs Informationen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="ef006-114">The server calls the RPC run-time functions [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) and [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to make binding information available to the client.</span></span> <span data-ttu-id="ef006-115">Dieses Beispielprogramm übergibt den Namen des Schnittstellen Handles an **RpcServerRegisterIf**.</span><span class="sxs-lookup"><span data-stu-id="ef006-115">This example program passes the interface handle name to **RpcServerRegisterIf**.</span></span> <span data-ttu-id="ef006-116">Die anderen Parameter werden auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ef006-116">The other parameters are set to **NULL**.</span></span> <span data-ttu-id="ef006-117">Der Server ruft dann die [**rpcserverlauschen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) -Funktion auf, um anzugeben, dass Sie auf Client Anforderungen wartet.</span><span class="sxs-lookup"><span data-stu-id="ef006-117">The server then calls the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to indicate that it is waiting for client requests.</span></span>

<span data-ttu-id="ef006-118">Die Serveranwendung muss auch die beiden Speicherverwaltungsfunktionen enthalten, die der Serverstub aufruft: [**mittlere \_ Benutzer \_**](the-midl-user-allocate-function.md) Zuordnungen und [**mittlerer l- \_ Benutzer \_ kostenlos**](the-midl-user-free-function.md).</span><span class="sxs-lookup"><span data-stu-id="ef006-118">The server application must also include the two memory management functions that the server stub calls: [**midl\_user\_allocate**](the-midl-user-allocate-function.md) and [**midl\_user\_free**](the-midl-user-free-function.md).</span></span> <span data-ttu-id="ef006-119">Diese Funktionen weisen Arbeitsspeicher auf dem Server zu und verteilen ihn frei, wenn eine Remote Prozedur Parameter an den Server übergibt.</span><span class="sxs-lookup"><span data-stu-id="ef006-119">These functions allocate and free memory on the server when a remote procedure passes parameters to the server.</span></span> <span data-ttu-id="ef006-120">In diesem Beispielprogramm sind die **Mittel l- \_ Benutzer \_** Zuordnungen und die **\_ Benutzer \_ Freihand für mittlere Benutzer** einfach Wrapper für die C-Bibliotheksfunktionen [**malloc**](pointers-and-memory-allocation.md) und **Free**.</span><span class="sxs-lookup"><span data-stu-id="ef006-120">In this example program, **midl\_user\_allocate** and **midl\_user\_free** are simply wrappers for the C-library functions [**malloc**](pointers-and-memory-allocation.md) and **free**.</span></span> <span data-ttu-id="ef006-121">(Beachten Sie, dass in der vom Compiler generierten Forward-Deklarationen "Mittel l" in Großbuchstaben vorliegt.</span><span class="sxs-lookup"><span data-stu-id="ef006-121">(Note that, in the MIDL compiler- generated forward declarations, "MIDL" is uppercase.</span></span> <span data-ttu-id="ef006-122">Die Header Datei Rpcndr. h definiert mittlere \_ Benutzer freie und mittlere Benutzer Zuordnungen, \_ die als \_ \_ mittlere \_ Benutzer \_ kostenfrei \_ \_ sind, bzw. Benutzer Zuordnungen.</span><span class="sxs-lookup"><span data-stu-id="ef006-122">The header file Rpcndr.h defines midl\_user\_free and midl\_user\_allocate to be MIDL\_user\_free and MIDL\_user\_allocate, respectively.)</span></span>


```C++
/* file: hellos.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h"
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszSecurity         = NULL; 
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned int    cMinCalls = 1;
    unsigned int    fDontWait = FALSE;
 
    status = RpcServerUseProtseqEp(pszProtocolSequence,
                                   RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                                   pszEndpoint,
                                   pszSecurity); 
 
    if (status) exit(status);
 
    status = RpcServerRegisterIf(hello_ServerIfHandle,  
                                 NULL,   
                                 NULL); 
 
    if (status) exit(status);
 
    status = RpcServerListen(cMinCalls,
                             RPC_C_LISTEN_MAX_CALLS_DEFAULT,
                             fDontWait);
 
    if (status) exit(status);
 }

/******************************************************/
/*         MIDL allocate and free                     */
/******************************************************/
 
void __RPC_FAR * __RPC_USER midl_user_allocate(size_t len)
{
    return(malloc(len));
}
 
void __RPC_USER midl_user_free(void __RPC_FAR * ptr)
{
    free(ptr);
}
```



 

 




