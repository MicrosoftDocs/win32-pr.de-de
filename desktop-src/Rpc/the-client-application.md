---
title: Die Clientanwendung
description: Das folgende Beispiel ist aus der "Hallo Welt"-Anwendung im Verzeichnis "RPC \\ Hello" des Platform Software Development Kit (SDK).
ms.assetid: 8c33801a-341a-4674-bd41-5bdca7e244fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96f97c7c35e00d3f36c645bfad2825dbada5e3a3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104474037"
---
# <a name="the-client-application"></a><span data-ttu-id="3d106-103">Die Clientanwendung</span><span class="sxs-lookup"><span data-stu-id="3d106-103">The Client Application</span></span>

<span data-ttu-id="3d106-104">Das folgende Beispiel ist aus der "Hallo Welt"-Anwendung im Verzeichnis "RPC \\ Hello" des Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="3d106-104">The example below is from the 'Hello World' application in the RPC\\Hello directory of the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="3d106-105">Die Quelldatei helloc. c enthält eine Direktive, die die von der Mittel l generierte Header Datei Hello. h einschließt.</span><span class="sxs-lookup"><span data-stu-id="3d106-105">The Helloc.c source file contains a directive to include the MIDL-generated header file, Hello.h.</span></span> <span data-ttu-id="3d106-106">In "Hello. h" sind Direktiven zum Einschließen von RPC. h und Rpcndr. h enthalten, die die Definitionen für die RPC-Lauf Zeit Routinen, **helloproc** und **Shutdown** sowie die Datentypen enthalten, die von den Client-und Server Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d106-106">Within Hello.h are directives to include Rpc.h and rpcndr.h, which contain the definitions for the RPC run-time routines, **HelloProc** and **Shutdown**, and data types that the client and server applications use.</span></span> <span data-ttu-id="3d106-107">Der mittlerer l-Compiler muss mit dem folgenden Beispiel verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d106-107">The MIDL compiler must be used with the example below.</span></span>

<span data-ttu-id="3d106-108">Da der Client seine Verbindung mit dem Server verwaltet, ruft die Client Anwendung Lauf Zeitfunktionen auf, um ein Handle für den Server einzurichten und dieses Handle freizugeben, nachdem die Remote Prozedur Aufrufe beendet wurden.</span><span class="sxs-lookup"><span data-stu-id="3d106-108">Because the client is managing its connection to the server, the client application calls run-time functions to establish a handle to the server and to release this handle after the remote procedure calls are complete.</span></span> <span data-ttu-id="3d106-109">Die Funktion [**rpcstringbindingcompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) kombiniert die Komponenten des Bindungs Handles zu einer Zeichen folgen Darstellung des Handles und ordnet Speicher für die Zeichen folgen Bindung zu.</span><span class="sxs-lookup"><span data-stu-id="3d106-109">The function [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) combines the components of the binding handle into a string representation of that handle and allocates memory for the string binding.</span></span> <span data-ttu-id="3d106-110">Die Funktion [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) erstellt ein Server Bindungs handle, **Hello \_ clientibhandle**, für die Client Anwendung aus dieser Zeichen folgen Darstellung.</span><span class="sxs-lookup"><span data-stu-id="3d106-110">The function [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) creates a server binding handle, **hello\_ClientIfHandle**, for the client application from that string representation.</span></span>

<span data-ttu-id="3d106-111">Beim Aufrufen von [**rpcstringbindingcompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose)geben die Parameter nicht die UUID an, da in diesem Tutorial davon ausgegangen wird, dass es nur eine Implementierung der Schnittstelle "Hello" gibt.</span><span class="sxs-lookup"><span data-stu-id="3d106-111">In the call to [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose), the parameters do not specify the UUID because this tutorial assumes there is just one implementation of the interface "hello."</span></span> <span data-ttu-id="3d106-112">Außerdem gibt der-Befehl keine Netzwerkadresse an, da die Anwendung den Standardwert verwendet, bei dem es sich um den lokalen Host Computer handelt.</span><span class="sxs-lookup"><span data-stu-id="3d106-112">In addition, the call does not specify a network address because the application will use the default, which is the local host machine.</span></span> <span data-ttu-id="3d106-113">Die Protokoll Sequenz ist eine Zeichenfolge, die den zugrunde liegenden Netzwerk Transport darstellt.</span><span class="sxs-lookup"><span data-stu-id="3d106-113">The protocol sequence is a character string that represents the underlying network transport.</span></span> <span data-ttu-id="3d106-114">Der Endpunkt ist ein Name, der spezifisch für die Protokoll Sequenz ist.</span><span class="sxs-lookup"><span data-stu-id="3d106-114">The endpoint is a name which is specific to the protocol sequence.</span></span> <span data-ttu-id="3d106-115">In diesem Beispiel werden Named Pipes für den Netzwerk Transport verwendet, sodass die Protokoll Sequenz "ncacn \_ NP" lautet.</span><span class="sxs-lookup"><span data-stu-id="3d106-115">This example uses named pipes for its network transport, so the protocol sequence is "ncacn\_np".</span></span> <span data-ttu-id="3d106-116">Der Endpunkt Name ist " \\ Pipe \\ Hello".</span><span class="sxs-lookup"><span data-stu-id="3d106-116">The endpoint name is "\\pipe\\hello".</span></span>

<span data-ttu-id="3d106-117">Die eigentlichen Remote Prozedur Aufrufe, **helloproc** und **Shutdown**, erfolgen innerhalb des RPC-Ausnahme Handlers – mit einem Satz von Makros, mit denen Sie Ausnahmen steuern können, die außerhalb des Anwendungs Codes auftreten.</span><span class="sxs-lookup"><span data-stu-id="3d106-117">The actual remote procedure calls, **HelloProc** and **Shutdown**, take place within the RPC exception handler—a set of macros that let you control exceptions that occur outside the application code.</span></span> <span data-ttu-id="3d106-118">Wenn das RPC-Lauf Zeit Modul eine Ausnahme meldet, wird die Steuerung an den [**rpcaußer**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) -Block weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="3d106-118">If the RPC run-time module reports an exception, control passes to the [**RpcExcept**](/windows/desktop/api/Rpc/nf-rpc-rpcexcept) block.</span></span> <span data-ttu-id="3d106-119">Hier fügen Sie Code ein, um alle benötigten Bereinigungs Vorgänge durchzuführen und dann ordnungsgemäß zu beenden.</span><span class="sxs-lookup"><span data-stu-id="3d106-119">This is where you would insert code to do any needed cleanup and then exit gracefully.</span></span> <span data-ttu-id="3d106-120">Dieses Beispielprogramm informiert den Benutzer einfach darüber, dass eine Ausnahme aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="3d106-120">This example program simply informs the user that an exception occurred.</span></span> <span data-ttu-id="3d106-121">Wenn Sie keine Ausnahmen verwenden möchten, können Sie die ACF-Attribute " [comm- \_ Status](/windows/desktop/Midl/comm-status) " und " [Fehler \_ Status](/windows/desktop/Midl/fault-status) " verwenden, um Fehler zu melden.</span><span class="sxs-lookup"><span data-stu-id="3d106-121">If you do not want to use exceptions, you can use the ACF attributes [comm\_status](/windows/desktop/Midl/comm-status) and [fault\_status](/windows/desktop/Midl/fault-status) to report errors.</span></span>

<span data-ttu-id="3d106-122">Nachdem die Remote Prozedur Aufrufe abgeschlossen sind, ruft der Client zuerst [**rpcstringfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) auf, um den Arbeitsspeicher freizugeben, der für die Zeichen folgen Bindung reserviert wurde.</span><span class="sxs-lookup"><span data-stu-id="3d106-122">After the remote procedure calls are completed, the client first calls [**RpcStringFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringfree) to free the memory that was allocated for the string binding.</span></span> <span data-ttu-id="3d106-123">Beachten Sie, dass ein Client Programm eine Zeichen folgen Bindung jederzeit freigeben kann, sobald das Bindungs Handle erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3d106-123">Note that once the binding handle has been created, a client program can free a string binding at any time.</span></span> <span data-ttu-id="3d106-124">Der Client ruft dann [**rpcbindingfree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) auf, um das Handle freizugeben.</span><span class="sxs-lookup"><span data-stu-id="3d106-124">The client next calls [**RpcBindingFree**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfree) to release the handle.</span></span>


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



 

 