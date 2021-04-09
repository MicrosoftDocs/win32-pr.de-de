---
title: Fehler durch Ausnahmen anzeigen
description: Bei herkömmlichen C-Programmierern werden Fehler häufig durch Rückgabewerte oder einen speziellen "\ out \"-Parameter zurückgegeben, der den Fehlercode zurückgibt.
ms.assetid: 85ee217d-6e0b-4160-9cec-a652c1daa9a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fafc97e4d9c9d76b965ab67bcd57f4f33100625
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858374"
---
# <a name="indicate-errors-by-exceptions"></a><span data-ttu-id="21647-103">Fehler durch Ausnahmen anzeigen</span><span class="sxs-lookup"><span data-stu-id="21647-103">Indicate Errors by Exceptions</span></span>

<span data-ttu-id="21647-104">Bei herkömmlichen C-Programmierern werden Fehler häufig durch Rückgabewerte oder einen speziellen out-Parameter zurückgegeben, \[ \] der den Fehlercode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="21647-104">For traditional C programmers, errors are commonly returned through return values, or a special \[out\] parameter that returns the error code.</span></span> <span data-ttu-id="21647-105">Dies führt dazu, dass die Schnittstellen folgendermaßen implementiert werden:</span><span class="sxs-lookup"><span data-stu-id="21647-105">This leads to interfaces implemented the following way:</span></span>

``` syntax
long sample(...)
{
    ...
    p = new Cbar(...);
    if (p == NULL)
    {
        // cleanup
        ...
        return ERROR_OUTOFMEMORY;
    }
}
```

<span data-ttu-id="21647-106">Das Problem bei diesem Ansatz besteht darin, dass RPC-Rückgabewerte einfach lange ganze Zahlen sind.</span><span class="sxs-lookup"><span data-stu-id="21647-106">The problem with this approach is that RPC return values are simply long integers.</span></span> <span data-ttu-id="21647-107">Sie haben keine besondere Bedeutung als Fehler (Beachten Sie, dass [**Fehler \_ Status \_ t**](/windows/desktop/Midl/error-status-t) keine besondere Semantik auf der Serverseite aufweist), was wichtige Implikationen bringt.</span><span class="sxs-lookup"><span data-stu-id="21647-107">They have no special meaning as errors (note that [**error\_status\_t**](/windows/desktop/Midl/error-status-t) has no special semantics on the server side), which carries important implications.</span></span>

<span data-ttu-id="21647-108">Erstens wird RPC nicht benachrichtigt, dass der Vorgang fehlgeschlagen ist. Es wird versucht, alle \[ in-, out \] -und \[ out- \] Argumente zu entmarshalling.</span><span class="sxs-lookup"><span data-stu-id="21647-108">First, RPC is not alerted that the operation failed; it attempts to unmarshal all \[in, out\] and \[out\] arguments.</span></span> <span data-ttu-id="21647-109">Die Fehler Semantik von Kontext Handles unterscheidet sich ebenfalls.</span><span class="sxs-lookup"><span data-stu-id="21647-109">The failure semantics of context handles are also different.</span></span> <span data-ttu-id="21647-110">Das Paket, das an den Client zurückgegeben wird, ist im Wesentlichen ein Erfolgs Paket, wobei der Fehlercode tief im Paket verborgen ist.</span><span class="sxs-lookup"><span data-stu-id="21647-110">The packet returned to the client is essentially a success packet, with the error code buried deep in the packet.</span></span> <span data-ttu-id="21647-111">Dies bedeutet auch, dass RPC keine erweiterten Fehlerinformationen verwendet, sodass Client Software häufig nicht erkennen kann, wo der Aufruf fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="21647-111">This also means RPC does not use extended error information, so client software often is unable to discern where the call failed.</span></span>

<span data-ttu-id="21647-112">Die Angabe von Fehlern in RPC-Server Routinen durch Auslösen von SEH-Ausnahmen (strukturierte Ausnahmebehandlung) (nicht C++) ist ein viel besseres Konzept.</span><span class="sxs-lookup"><span data-stu-id="21647-112">Indicating errors in RPC server routines by throwing Structured Exception Handling (SEH) exceptions (not C++) is a much better approach.</span></span> <span data-ttu-id="21647-113">Wenn eine SEH-Ausnahme ausgelöst wird, wird die Steuerung direkt an die RPC-Laufzeit weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="21647-113">When an SEH exception is thrown, control goes directly to the RPC run time.</span></span> <span data-ttu-id="21647-114">Manchmal tritt ein Fehler in einer Routine auf, die nicht ordnungsgemäß bereinigt werden kann, und es muss ein Fehler für den Aufrufer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="21647-114">An error sometimes occurs deep in a routine that cannot properly clean up, and it needs to indicate an error to its caller.</span></span> <span data-ttu-id="21647-115">Die Routine sollte einen Fehler an den Aufrufer zurückgeben, der wiederum einen Fehler an den Aufrufer zurückgeben kann usw.</span><span class="sxs-lookup"><span data-stu-id="21647-115">The routine should return an error to its caller, which in turn can return an error to its caller and so on.</span></span> <span data-ttu-id="21647-116">Allerdings sollte die letzte Server Routine auf dem Stapel eine Ausnahme auslösen, bevor Sie zu RPC zurückkehrt, um RPC anzuzeigen, dass ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="21647-116">However, the last server routine on the stack should throw an exception before it returns to RPC to indicate to RPC that an error occurred.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21647-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="21647-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21647-118">Ausnahmebehandlung</span><span class="sxs-lookup"><span data-stu-id="21647-118">Exception Handling</span></span>](exception-handling.md)
</dt> </dl>

 

 