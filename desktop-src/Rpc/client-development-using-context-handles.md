---
title: Client Entwicklung mithilfe von Kontext Handles
description: Die einzige Verwendung eines Client Programms für ein Kontext Handle besteht darin, dass jedes Mal, wenn der Client einen Remote Prozedur Aufruf durchführt, an den Server übergeben wird.
ms.assetid: fcbdfb1e-4f1e-4d22-9a3e-cf5a29d300d0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c7d2dfca901085c743b25eb233ee2493b893e7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515981"
---
# <a name="client-development-using-context-handles"></a><span data-ttu-id="66f6f-103">Client Entwicklung mithilfe von Kontext Handles</span><span class="sxs-lookup"><span data-stu-id="66f6f-103">Client Development Using Context Handles</span></span>

<span data-ttu-id="66f6f-104">Die einzige Verwendung eines Client Programms für ein Kontext Handle besteht darin, dass jedes Mal, wenn der Client einen Remote Prozedur Aufruf durchführt, an den Server übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="66f6f-104">The only use a client program has for a context handle is to pass it to the server each time the client makes a remote procedure call.</span></span> <span data-ttu-id="66f6f-105">Die Client Anwendung muss nicht auf den Inhalt des Handles zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="66f6f-105">The client application does not need to access the contents of the handle.</span></span> <span data-ttu-id="66f6f-106">Es sollte nicht versucht werden, die Daten des Kontext Handles in irgendeiner Weise zu ändern.</span><span class="sxs-lookup"><span data-stu-id="66f6f-106">It should not try to change the context handle data in any way.</span></span> <span data-ttu-id="66f6f-107">Die vom Client aufgerufenen Remote Prozeduren führen alle notwendigen Vorgänge im Kontext des Servers aus.</span><span class="sxs-lookup"><span data-stu-id="66f6f-107">The remote procedures that the client invokes perform all necessary operations on the server's context.</span></span>

<span data-ttu-id="66f6f-108">Vor dem Anfordern eines Kontext Handles von einem Server müssen Clients eine Bindung mit dem Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="66f6f-108">Prior to requesting a context handle from a server, clients must establish a binding with the server.</span></span> <span data-ttu-id="66f6f-109">Der Client kann ein automatisches, implizites oder explizites Bindungs Handle verwenden.</span><span class="sxs-lookup"><span data-stu-id="66f6f-109">The client may use an automatic, implicit, or explicit binding handle.</span></span> <span data-ttu-id="66f6f-110">Mit einem gültigen Bindungs Handle kann der Client eine Remote Prozedur auf dem Server aufrufen, die entweder ein geöffnetes Kontext Handle (nicht **null**) zurückgibt oder einen **\[ out \]** -Parameter in der Parameterliste der Remote Prozedur übergibt.</span><span class="sxs-lookup"><span data-stu-id="66f6f-110">With a valid binding handle, the client can call a remote procedure on the server that either returns an opened (non-**NULL**) context handle or passes one through an **\[out\]** parameter in the remote procedure's parameter list.</span></span>

<span data-ttu-id="66f6f-111">Clients können geöffnete Kontext Handles in beliebiger Weise verwenden.</span><span class="sxs-lookup"><span data-stu-id="66f6f-111">Clients may use opened context handles in any way they require.</span></span> <span data-ttu-id="66f6f-112">Sie sollten das Handle jedoch für ungültig erklären, wenn es nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="66f6f-112">They should, however, invalidate the handle when they no longer need it.</span></span> <span data-ttu-id="66f6f-113">Hierfür gibt es zwei Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="66f6f-113">There are two way to do this:</span></span>

-   <span data-ttu-id="66f6f-114">Um eine Remote Prozedur aufzurufen, die vom Serverprogramm bereitgestellt wird, das den Kontext freigibt und das Kontext Handle schließt (legt es auf **null** fest).</span><span class="sxs-lookup"><span data-stu-id="66f6f-114">To invoke a remote procedure offered by the server program that frees the context and closes the context handle (sets it to **NULL**).</span></span>
-   <span data-ttu-id="66f6f-115">Wenn der Server nicht erreichbar ist, müssen Sie die [**rpcssdestroyclientcontext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) -Funktion aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="66f6f-115">When the server is unreachable, call the [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) function.</span></span>

<span data-ttu-id="66f6f-116">Beim zweiten Ansatz wird nur der Client seitige Zustand bereinigt, und der serverseitige Zustand wird nicht bereinigt. er sollte daher nur verwendet werden, wenn die Netzwerk Partition vermutet wird, und der Client und der Server führen eine unabhängige Bereinigung durch.</span><span class="sxs-lookup"><span data-stu-id="66f6f-116">The second approach only cleans up the client side state, and does not clean up the server-side state, so it should be used only when network partition is suspected, and the client and the server will do an independent cleanup.</span></span> <span data-ttu-id="66f6f-117">Der Server führt eine unabhängige Bereinigung durch die Lauf-Down-Routine durch, und der Client führt dies mithilfe der [**rpcssdestroyclientcontext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) -Funktion aus.</span><span class="sxs-lookup"><span data-stu-id="66f6f-117">The server performs independent cleanup through the run-down routine, the client does so using the [**RpcSsDestroyClientContext**](/windows/desktop/api/Rpcndr/nf-rpcndr-rpcssdestroyclientcontext) function.</span></span>

<span data-ttu-id="66f6f-118">Das folgende Code Fragment zeigt ein Beispiel für die Verwendung eines Kontext Handles durch einen Client.</span><span class="sxs-lookup"><span data-stu-id="66f6f-118">The following code fragment presents an example of how a client might use a context handle.</span></span> <span data-ttu-id="66f6f-119">Informationen zum Anzeigen der Definition der Schnittstelle, die in diesem Beispiel verwendet wird, finden Sie unter [Schnittstellen Entwicklung mithilfe von Kontext Handles](interface-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="66f6f-119">To view the definition of the interface that this example uses, see [Interface Development Using Context Handles](interface-development-using-context-handles.md).</span></span> <span data-ttu-id="66f6f-120">Informationen zur Server Implementierung finden [Sie unter Serverentwicklung mithilfe von Kontext Handles](server-development-using-context-handles.md).</span><span class="sxs-lookup"><span data-stu-id="66f6f-120">For the server implementation, see [Server Development Using Context Handles](server-development-using-context-handles.md).</span></span>

<span data-ttu-id="66f6f-121">In diesem Beispiel ruft der Client remoteopen auf, um ein Kontext Handle zu erhalten, das gültige Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="66f6f-121">In this example, the client calls RemoteOpen to obtain a context handle that contains valid data.</span></span> <span data-ttu-id="66f6f-122">Der Client kann dann das Kontext Handle in Remote Prozedur aufrufen verwenden.</span><span class="sxs-lookup"><span data-stu-id="66f6f-122">The client can then use the context handle in remote procedure calls.</span></span> <span data-ttu-id="66f6f-123">Da das Bindungs Handle nicht mehr benötigt wird, kann der Client das explizite handle freigeben, das zum Erstellen des Kontext Handles verwendet wurde:</span><span class="sxs-lookup"><span data-stu-id="66f6f-123">Because it no longer needs the binding handle, the client can free the explicit handle it used to create the context handle:</span></span>


```C++
// cxhndlc.c  (fragment of client side application)
printf("Calling the remote procedure RemoteOpen\n");
if (RemoteOpen(&phContext, pszFileName) < 0) 
{
    printf("Unable to open %s\n", pszFileName);
    Shutdown();
    exit(2);
}
 
// Now the context handle also manages the binding.
// The variable hBindingHandle is a valid binding handle.
status = RpcBindingFree(&hBindingHandle);
printf("RpcBindingFree returned 0x%x\n", status);
if (status) 
    exit(status);
```



<span data-ttu-id="66f6f-124">Die Client Anwendung in diesem Beispiel verwendet eine Prozedur namens RemoteRead, um eine Datendatei auf dem Server zu lesen, bis das Ende der Datei gefunden wird.</span><span class="sxs-lookup"><span data-stu-id="66f6f-124">The client application in this example uses a procedure called RemoteRead to read a data file on the server until it encounters an end of file.</span></span> <span data-ttu-id="66f6f-125">Anschließend wird die Datei durch Aufrufen von remoteclose geschlossen.</span><span class="sxs-lookup"><span data-stu-id="66f6f-125">It then closes the file by calling RemoteClose.</span></span> <span data-ttu-id="66f6f-126">Das Kontext Handle wird als Parameter in den Funktionen RemoteRead und remoteclose wie folgt angezeigt:</span><span class="sxs-lookup"><span data-stu-id="66f6f-126">The context handle appears as a parameter in the RemoteRead and RemoteClose functions as:</span></span>


```C++
printf("Calling the remote procedure RemoteRead\n");
do 
{
    cbRead = 1024; // Using a 1K buffer
    RemoteRead(phContext, pbBuf, &cbRead);
    // cbRead contains the number of bytes actually read.
    for (int i = 0; i < cbRead; i++)
        putchar(*(pbBuf+i));
} while(cbRead);
 
printf("Calling the remote procedure RemoteClose\n");
if (RemoteClose(&phContext) < 0 ) 
{
    printf("Close failed on %s\n", pszFileName);
    exit(2);
}
```



 

 




