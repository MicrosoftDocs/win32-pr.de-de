---
title: Die Clientanwendung
description: Zeigen Sie den Clientanwendungsteil eines RPC-Beispiels (Remote Procedure Call) an. Das folgende Beispiel ist aus der Anwendung "Hallo Welt" im Platform SDK.
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e0b798543cd70e61f3ff1161503fa64710e53e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405013"
---
# <a name="the-client-application"></a><span data-ttu-id="9ab64-104">Die Clientanwendung</span><span class="sxs-lookup"><span data-stu-id="9ab64-104">The Client Application</span></span>

<span data-ttu-id="9ab64-105">Das folgende Beispiel ist aus der Anwendung "Hallo Welt" im RPC \\ Hello-Verzeichnis des Platform Software Development Kit (SDK) enthalten.</span><span class="sxs-lookup"><span data-stu-id="9ab64-105">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="9ab64-106">Die Helloc.c-Quelldatei enthält eine -Direktive, die die von MIDL generierte Headerdatei Hello.h enthält.</span><span class="sxs-lookup"><span data-stu-id="9ab64-106">The Helloc.c source file contains a directive to include the MIDL-generated header file, Hello.h.</span></span> <span data-ttu-id="9ab64-107">In Hello.h sind -Anweisungen enthalten, die Rpc.h und rpcndr.h enthalten, die die Definitionen für die RPC-Laufzeitroutinen, **HelloProc** und **Shutdown** sowie die Datentypen enthalten, die die Client- und Serveranwendungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="9ab64-107">Within Hello.h are directives to include Rpc.h and rpcndr.h, which contain the definitions for the RPC run-time routines, **HelloProc** and **Shutdown**, and data types that the client and server applications use.</span></span> <span data-ttu-id="9ab64-108">Der MIDL-Compiler muss mit dem folgenden Beispiel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9ab64-108">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="9ab64-109">Da der Client seine Verbindung mit dem Server verwalten soll, ruft die Clientanwendung Laufzeitfunktionen auf, um ein Handle für den Server herzustellen und dieses Handle frei zu geben, nachdem die Remoteprozeduraufrufe abgeschlossen sind.</span><span class="sxs-lookup"><span data-stu-id="9ab64-109">Because the client is managing its connection to the server, the client application calls run-time functions to establish a handle to the server and to release this handle after the remote procedure calls are complete.</span></span> <span data-ttu-id="9ab64-110">Die [**Funktion RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) kombiniert die Komponenten des Bindungshandpunkts in einer Zeichenfolgendarstellung dieses Handle und ordnet Arbeitsspeicher für die Zeichenfolgenbindung zu.</span><span class="sxs-lookup"><span data-stu-id="9ab64-110">The function [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combines the components of the binding handle into a string representation of that handle and allocates memory for the string binding.</span></span> <span data-ttu-id="9ab64-111">Die Funktion [**RpcBindingFromStringBinding erstellt**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) aus dieser Zeichenfolgendarstellung das Serverbindungshandle **hello \_ ClientIfHandle** für die Clientanwendung.</span><span class="sxs-lookup"><span data-stu-id="9ab64-111">The function [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) creates a server binding handle, **hello\_ClientIfHandle**, for the client application from that string representation.</span></span>

<span data-ttu-id="9ab64-112">Beim Aufruf von [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose)geben die Parameter die UUID nicht an, da in diesem Tutorial davon ausgegangen wird, dass es nur eine Implementierung der Schnittstelle "hello" gibt.</span><span class="sxs-lookup"><span data-stu-id="9ab64-112">In the call to [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), the parameters do not specify the UUID because this tutorial assumes there is just one implementation of the interface "hello."</span></span> <span data-ttu-id="9ab64-113">Darüber hinaus gibt der Aufruf keine Netzwerkadresse an, da die Anwendung die Standardeinstellung verwendet, bei der es sich um den lokalen Hostcomputer handelt.</span><span class="sxs-lookup"><span data-stu-id="9ab64-113">In addition, the call does not specify a network address because the application will use the default, which is the local host machine.</span></span> <span data-ttu-id="9ab64-114">Die Protokollsequenz ist eine Zeichenfolge, die den zugrunde liegenden Netzwerktransport darstellt.</span><span class="sxs-lookup"><span data-stu-id="9ab64-114">The protocol sequence is a character string that represents the underlying network transport.</span></span> <span data-ttu-id="9ab64-115">Der Endpunkt ist ein Name, der für die Protokollsequenz spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="9ab64-115">The endpoint is a name which is specific to the protocol sequence.</span></span> <span data-ttu-id="9ab64-116">In diesem Beispiel werden Named Pipes für den Netzwerktransport verwendet, sodass die Protokollsequenz "ncacn \_ np" ist.</span><span class="sxs-lookup"><span data-stu-id="9ab64-116">This example uses named pipes for its network transport, so the protocol sequence is "ncacn\_np".</span></span> <span data-ttu-id="9ab64-117">Der Endpunktname ist \\ "pipe \\ hello".</span><span class="sxs-lookup"><span data-stu-id="9ab64-117">The endpoint name is "\\pipe\\hello".</span></span>

<span data-ttu-id="9ab64-118">Die tatsächlichen Remoteprozeduraufrufe **HelloProc** und **Shutdown** erfolgen innerhalb des RPC-Ausnahmehandlers– einer Reihe von Makros, mit denen Sie Ausnahmen steuern können, die außerhalb des Anwendungscodes auftreten.</span><span class="sxs-lookup"><span data-stu-id="9ab64-118">The actual remote procedure calls, **HelloProc** and **Shutdown**, take place within the RPC exception handler—a set of macros that let you control exceptions that occur outside the application code.</span></span> <span data-ttu-id="9ab64-119">Wenn das RPC-Laufzeitmodul eine Ausnahme meldet, wird die Steuerung an den [**RpcExcept-Block**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) übergibt.</span><span class="sxs-lookup"><span data-stu-id="9ab64-119">If the RPC run-time module reports an exception, control passes to the [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) block.</span></span> <span data-ttu-id="9ab64-120">Hier fügen Sie Code ein, um alle erforderlichen Bereinigungen zu ausführen und dann ordnungsgemäß zu beenden.</span><span class="sxs-lookup"><span data-stu-id="9ab64-120">This is where you would insert code to do any needed cleanup and then exit gracefully.</span></span> <span data-ttu-id="9ab64-121">Dieses Beispielprogramm informiert den Benutzer lediglich darüber, dass eine Ausnahme aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9ab64-121">This example program simply informs the user that an exception occurred.</span></span> <span data-ttu-id="9ab64-122">Wenn Sie keine Ausnahmen verwenden möchten, können Sie die ACF-Attribute [comm \_ status](/windows/desktop/Midl/comm-status) und [fault \_ status](/windows/desktop/Midl/fault-status) verwenden, um Fehler zu melden.</span><span class="sxs-lookup"><span data-stu-id="9ab64-122">If you do not want to use exceptions, you can use the ACF attributes [comm\_status](/windows/desktop/Midl/comm-status) and [fault\_status](/windows/desktop/Midl/fault-status) to report errors.</span></span>

<span data-ttu-id="9ab64-123">Nachdem die Remoteprozeduraufrufe abgeschlossen sind, ruft der Client zuerst [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) auf, um den Arbeitsspeicher frei zu geben, der für die Zeichenfolgenbindung zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="9ab64-123">After the remote procedure calls are completed, the client first calls [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) to free the memory that was allocated for the string binding.</span></span> <span data-ttu-id="9ab64-124">Beachten Sie, dass ein Clientprogramm nach dem Erstellen des Bindungshandpunkts jederzeit eine Zeichenfolgenbindung freigibt.</span><span class="sxs-lookup"><span data-stu-id="9ab64-124">Note that once the binding handle has been created, a client program can free a string binding at any time.</span></span> <span data-ttu-id="9ab64-125">Der Client ruft als Nächstes [**RpcBindingFree auf,**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) um das Handle frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="9ab64-125">The client next calls [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) to release the handle.</span></span>


```C++
/* file: helloc.c */
#include <stdlib.h>
#include <stdio.h>
#include <ctype.h>
#include "hello.h" 
#include <windows.h>

void main()
{
    RPC_STATUS status;
    unsigned char * pszUuid             = NULL;
    unsigned char * pszProtocolSequence = "ncacn_np";
    unsigned char * pszNetworkAddress   = NULL;
    unsigned char * pszEndpoint         = "\\pipe\\hello";
    unsigned char * pszOptions          = NULL;
    unsigned char * pszStringBinding    = NULL;
    unsigned char * pszString           = "hello, world";
    unsigned long ulCode;
 
    status = RpcStringBindingCompose(pszUuid,
                                     pszProtocolSequence,
                                     pszNetworkAddress,
                                     pszEndpoint,
                                     pszOptions,
                                     &pszStringBinding);
    if (status) exit(status);

    status = RpcBindingFromStringBinding(pszStringBinding, &hello_ClientIfHandle);
 
    if (status) exit(status);
 
    RpcTryExcept  
    {
        HelloProc(pszString);
        Shutdown();
    }
    RpcExcept(1) 
    {
        ulCode = RpcExceptionCode();
        printf("Runtime reported exception 0x%lx = %ld\n", ulCode, ulCode);
    }
    RpcEndExcept
 
    status = RpcStringFree(&pszStringBinding); 
 
    if (status) exit(status);
 
    status = RpcBindingFree(&hello_IfHandle);
 
    if (status) exit(status);

    exit(0);
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



 

 