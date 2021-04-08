---
title: Verwenden von Bindungs Handles und Senden von RPC-Aufrufen
description: Ein häufiger Fehler bei RPC-Programmierern besteht darin, alle Ausnahmen zu behandeln.
ms.assetid: 5b452129-4060-49f9-9400-8585fb5714a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b285fc3030b92e2616c850bf79c73e37f0341c9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728849"
---
# <a name="using-binding-handles-and-making-rpc-calls"></a><span data-ttu-id="8d261-103">Verwenden von Bindungs Handles und Senden von RPC-Aufrufen</span><span class="sxs-lookup"><span data-stu-id="8d261-103">Using Binding Handles and Making RPC Calls</span></span>

<span data-ttu-id="8d261-104">Ein häufiger Fehler bei RPC-Programmierern besteht darin, alle Ausnahmen zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="8d261-104">A common mistake among RPC programmers is handling all exceptions.</span></span> <span data-ttu-id="8d261-105">Viele Programmierer strukturieren ihre Ausnahme Handles wie folgt:</span><span class="sxs-lookup"><span data-stu-id="8d261-105">Many programmers structure their exception handles like the following:</span></span>

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    RpcExcept(1)
        {
        log an error or do something else
        }
    RpcEndExcept
```

<span data-ttu-id="8d261-106">Das Problem mit diesem Handler besteht darin, dass alle Fehler, einschließlich der Fehler im Client Programm, abgefangen werden.</span><span class="sxs-lookup"><span data-stu-id="8d261-106">The problem with this handler is that it catches all errors, including errors in the client program.</span></span> <span data-ttu-id="8d261-107">Das Abfangen von Fehlern im Client Programm erschwert das Debuggen.</span><span class="sxs-lookup"><span data-stu-id="8d261-107">Catching errors in the client program makes debugging more difficult.</span></span> <span data-ttu-id="8d261-108">Die richtige Methode zum Strukturieren eines Ausnahme Handlers ist Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8d261-108">The proper way to structure an exception handler is the following:</span></span>

``` syntax
    RpcTryExcept
        {
        RemoteSample();
        }
    // Return "non-fatal" errors to clients.  Catching fatal errors
    // makes it harder to debug.
    RpcExcept( ( ( (RpcExceptionCode() != STATUS_ACCESS_VIOLATION) &&
                   (RpcExceptionCode() != STATUS_POSSIBLE_DEADLOCK) &&
                   (RpcExceptionCode() != STATUS_INSTRUCTION_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_DATATYPE_MISALIGNMENT) &&
                   (RpcExceptionCode() != STATUS_PRIVILEGED_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_ILLEGAL_INSTRUCTION) &&
                   (RpcExceptionCode() != STATUS_BREAKPOINT) &&
                   (RpcExceptionCode() != STATUS_STACK_OVERFLOW) &&
                   (RpcExceptionCode() != STATUS_HANDLE_NOT_CLOSABLE) &&
                   (RpcExceptionCode() != STATUS_IN_PAGE_ERROR) &&
                   (RpcExceptionCode() != STATUS_ASSERTION_FAILURE) &&
                   (RpcExceptionCode() != STATUS_STACK_BUFFER_OVERRUN) &&
                   (RpcExceptionCode() != STATUS_GUARD_PAGE_VIOLATION)
                    )
                    ? EXCEPTION_EXECUTE_HANDLER : EXCEPTION_CONTINUE_SEARCH ) )
        {
        log an error or do something else
        }
    RpcEndExcept
```

<span data-ttu-id="8d261-109">Dieser Ausnahmehandler hat den Vorteil, dass ein bestimmter Bereich von Fehlern durch ermöglicht wird.</span><span class="sxs-lookup"><span data-stu-id="8d261-109">This exception handler has the advantage of letting a certain range of errors through.</span></span> <span data-ttu-id="8d261-110">Diese Fehler werden vom Server nie zurückgegeben, da Sie auf ein Client seitiges Problem hindeuten.</span><span class="sxs-lookup"><span data-stu-id="8d261-110">These errors will never be returned by the server, because they indicate a client side problem.</span></span>

<span data-ttu-id="8d261-111">Außerdem wird empfohlen, die **\[** [strengen Kontext \_ handle \_](/windows/desktop/Midl/strict-context-handle) **\]** -und **\[** [ \_ typstrict- \_ Kontext \_ handle](/windows/desktop/Midl/type-strict-context-handle)- **\]** Attribute zu verwenden, um sicherzustellen, dass die RPC-Laufzeit ein Kontext Handle für eine Schnittstelle erstellt, die nur als Argument an Methoden dieser Schnittstelle weitergeleitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="8d261-111">Additionally, the use of the **\[**[strict\_context\_handle](/windows/desktop/Midl/strict-context-handle)**\]** and **\[**[type\_strict\_context\_handle](/windows/desktop/Midl/type-strict-context-handle)**\]** attributes are recommended to ensure the RPC run time creates a context handle on one interface that can be passed as an argument only to methods of that interface.</span></span> <span data-ttu-id="8d261-112">Dadurch werden Server Fehler verhindert, die auftreten, wenn Kontext Handles geöffnet und zwischen verschiedenen Schnittstellen, die innerhalb desselben Prozesses vorhanden sind, übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="8d261-112">Doing so will prevent server failures that occur when context handles are opened and passed between different interfaces that exist within the same process.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8d261-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8d261-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d261-114">Strict- \_ Kontext \_ handle</span><span class="sxs-lookup"><span data-stu-id="8d261-114">strict\_context\_handle</span></span>](/windows/desktop/Midl/strict-context-handle)
</dt> <dt>

[<span data-ttu-id="8d261-115">Typ \_ Strict- \_ Kontext \_ handle</span><span class="sxs-lookup"><span data-stu-id="8d261-115">type\_strict\_context\_handle</span></span>](/windows/desktop/Midl/type-strict-context-handle)
</dt> </dl>

 

 