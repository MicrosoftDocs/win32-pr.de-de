---
title: Die Serveranwendung
description: Zeigen Sie den Serveranwendungsteil eines RPC-Beispiels (Remote Procedure Call, Remoteprozeduraufruf) an. Das Beispiel ist aus der Anwendung "Hallo Welt" im Plattform-SDK.
ms.assetid: 82ccfd67-6626-49c4-8974-86ebc5841444
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34b8a2bb66fd415a9b8f778134edb4903f88a717
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406063"
---
# <a name="the-server-application"></a><span data-ttu-id="1837c-104">Die Serveranwendung</span><span class="sxs-lookup"><span data-stu-id="1837c-104">The Server Application</span></span>

<span data-ttu-id="1837c-105">Das folgende Beispiel ist aus der Anwendung "Hallo Welt" im RPC \\ Hello-Verzeichnis des Platform Software Development Kit (SDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="1837c-105">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="1837c-106">Die Serverseite der verteilten Anwendung informiert das System darüber, dass seine Dienste verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1837c-106">The server side of the distributed application informs the system that its services are available.</span></span> <span data-ttu-id="1837c-107">Anschließend wird auf Clientanforderungen gewartet.</span><span class="sxs-lookup"><span data-stu-id="1837c-107">It then waits for client requests.</span></span> <span data-ttu-id="1837c-108">Der MIDL-Compiler muss mit dem folgenden Beispiel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1837c-108">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="1837c-109">Abhängig von der Größe Ihrer Anwendung und Ihren Codierungseinstellungen können Sie Remoteverfahren in einer oder mehrere separate Dateien implementieren.</span><span class="sxs-lookup"><span data-stu-id="1837c-109">Depending on the size of your application and your coding preferences, you can choose to implement remote procedures in one or more separate files.</span></span> <span data-ttu-id="1837c-110">In diesem Tutorialprogramm enthält die Quelldatei Hellos.c die Hauptserverroutine.</span><span class="sxs-lookup"><span data-stu-id="1837c-110">In this tutorial program, the source file Hellos.c contains the main server routine.</span></span> <span data-ttu-id="1837c-111">Die Datei Hellop.c enthält die Remoteprozedur.</span><span class="sxs-lookup"><span data-stu-id="1837c-111">The file Hellop.c contains the remote procedure.</span></span>

<span data-ttu-id="1837c-112">Der Vorteil der Organisation der Remoteverfahren in separaten Dateien ist, dass die Prozeduren mit einem eigenständigen Programm verknüpft werden können, um den Code zu debuggen, bevor er in eine verteilte Anwendung konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="1837c-112">The benefit of organizing the remote procedures in separate files is that the procedures can be linked with a standalone program to debug the code before it is converted to a distributed application.</span></span> <span data-ttu-id="1837c-113">Nachdem die Prozeduren im eigenständigen Programm ausgeführt wurden, können Sie die Quelldateien kompilieren und mit der Serveranwendung verknüpfen, die die Remoteverfahren enthalten.</span><span class="sxs-lookup"><span data-stu-id="1837c-113">After the procedures work in the standalone program, you can compile and link the source files containing the remote procedures with the server application.</span></span> <span data-ttu-id="1837c-114">Wie bei der Quelldatei der Clientanwendung muss die Quelldatei der Serveranwendung die Headerdatei Hello.h enthalten.</span><span class="sxs-lookup"><span data-stu-id="1837c-114">As with the client-application source file, the server-application source file must include the Hello.h header file.</span></span>

<span data-ttu-id="1837c-115">Der Server ruft die RPC-Laufzeitfunktionen [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) und [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) auf, um dem Client Bindungsinformationen zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="1837c-115">The server calls the RPC run-time functions [**RpcServerUseProtseqEp**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserveruseprotseqep) and [**RpcServerRegisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif) to make binding information available to the client.</span></span> <span data-ttu-id="1837c-116">Dieses Beispielprogramm übergibt den Schnittstellenhandpunktnamen an **RpcServerRegisterIf.**</span><span class="sxs-lookup"><span data-stu-id="1837c-116">This example program passes the interface handle name to **RpcServerRegisterIf**.</span></span> <span data-ttu-id="1837c-117">Die anderen Parameter werden auf **NULL festgelegt.**</span><span class="sxs-lookup"><span data-stu-id="1837c-117">The other parameters are set to **NULL**.</span></span> <span data-ttu-id="1837c-118">Der Server ruft dann die [**RpcServerListen-Funktion**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) auf, um anzugeben, dass er auf Clientanforderungen wartet.</span><span class="sxs-lookup"><span data-stu-id="1837c-118">The server then calls the [**RpcServerListen**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverlisten) function to indicate that it is waiting for client requests.</span></span>

<span data-ttu-id="1837c-119">Die Serveranwendung muss auch die beiden Speicherverwaltungsfunktionen enthalten, die der Serverstub aufruft: [**midl \_ user \_ allocate**](the-midl-user-allocate-function.md) und [**midl \_ user \_ free**](the-midl-user-free-function.md).</span><span class="sxs-lookup"><span data-stu-id="1837c-119">The server application must also include the two memory management functions that the server stub calls: [**midl\_user\_allocate**](the-midl-user-allocate-function.md) and [**midl\_user\_free**](the-midl-user-free-function.md).</span></span> <span data-ttu-id="1837c-120">Diese Funktionen weisen Arbeitsspeicher auf dem Server zu und geben diesen frei, wenn eine Remoteprozedur Parameter an den Server übergibt.</span><span class="sxs-lookup"><span data-stu-id="1837c-120">These functions allocate and free memory on the server when a remote procedure passes parameters to the server.</span></span> <span data-ttu-id="1837c-121">In diesem Beispielprogramm sind **midl \_ user \_ allocate** und **midl \_ user \_ free** einfach Wrapper für die C-Bibliotheksfunktionen [**malloc**](pointers-and-memory-allocation.md) und **free.**</span><span class="sxs-lookup"><span data-stu-id="1837c-121">In this example program, **midl\_user\_allocate** and **midl\_user\_free** are simply wrappers for the C-library functions [**malloc**](pointers-and-memory-allocation.md) and **free**.</span></span> <span data-ttu-id="1837c-122">(Beachten Sie, dass "MIDL" in den vom MIDL-Compiler generierten Vorwärtsdeklarationen Großbuchstaben ist.</span><span class="sxs-lookup"><span data-stu-id="1837c-122">(Note that, in the MIDL compiler- generated forward declarations, "MIDL" is uppercase.</span></span> <span data-ttu-id="1837c-123">Die Headerdatei Rpcndr.h definiert die midl-Benutzerfreigabe und die midl-Benutzer-Zuordnung, um MIDL-Benutzer kostenlos und \_ \_ \_ \_ \_ \_ MIDL-Benutzer \_ \_ zuteilen.)</span><span class="sxs-lookup"><span data-stu-id="1837c-123">The header file Rpcndr.h defines midl\_user\_free and midl\_user\_allocate to be MIDL\_user\_free and MIDL\_user\_allocate, respectively.)</span></span>


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



 

 




