---
title: Unabhängigkeit von anderen Komponenten
description: Erweiterte Fehler Daten sind auch dann nützlich, wenn der Server oder die Anwendung, über den die Kette übermittelt wurde, erweiterte Fehler Daten nicht erkennt oder Sie nicht nutzt. Empfohlene Vorgehensweisen für derartige Situationen werden am Ende dieses Abschnitts bereitgestellt.
ms.assetid: 32c52afd-cd79-4df3-bf30-72a17ce22089
keywords:
- Unabhängigkeit von anderen Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ba20a47a5bb30d8e23c1a90d666bc6b957ebb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948005"
---
# <a name="independence-from-other-components"></a><span data-ttu-id="5d026-105">Unabhängigkeit von anderen Komponenten</span><span class="sxs-lookup"><span data-stu-id="5d026-105">Independence From Other Components</span></span>

<span data-ttu-id="5d026-106">Erweiterte Fehler Daten sind auch dann nützlich, wenn der Server oder die Anwendung, über den die Kette übermittelt wurde, erweiterte Fehler Daten nicht erkennt oder Sie nicht nutzt.</span><span class="sxs-lookup"><span data-stu-id="5d026-106">Extended error data is useful even when the server or application through which the chain passed does not recognize extended error data, or does not take advantage of it.</span></span> <span data-ttu-id="5d026-107">Empfohlene Vorgehensweisen für derartige Situationen werden am Ende dieses Abschnitts bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="5d026-107">Recommended approaches for such situations are provided at the end of this section.</span></span>

<span data-ttu-id="5d026-108">Erweiterte Fehler Daten sind besonders nützlich, wenn Anwendungen oder Server, die RPC verwenden, erweiterte Fehlerinformationen nutzen.</span><span class="sxs-lookup"><span data-stu-id="5d026-108">Extended error data is most useful when applications or servers using RPC take advantage of extended error information.</span></span> <span data-ttu-id="5d026-109">Wenn Sie einen RPC \_ \_ \* -Fehlercode untersuchen und die beteiligten Server oder Anwendungen keine erweiterten Fehler Daten verfügbar machen, sollten Sie die folgenden Ansätze beachten:</span><span class="sxs-lookup"><span data-stu-id="5d026-109">When investigating an RPC\_S\_\* error code and the servers or applications involved do not make extended error data available, consider the following approaches:</span></span>

-   <span data-ttu-id="5d026-110">Nehmen Sie einen Sniff vor.</span><span class="sxs-lookup"><span data-stu-id="5d026-110">Take a sniff.</span></span>

    <span data-ttu-id="5d026-111">Reproduzieren Sie das Szenario, während Sie den Sniff ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d026-111">Reproduce the scenario while taking the sniff.</span></span> <span data-ttu-id="5d026-112">Der Ausspionieren der Verbindung enthält die erweiterten Fehler Daten.</span><span class="sxs-lookup"><span data-stu-id="5d026-112">The sniff of the wire will contain the extended error data.</span></span>

-   <span data-ttu-id="5d026-113">Überprüfen Sie diese im Debugger.</span><span class="sxs-lookup"><span data-stu-id="5d026-113">Examine it from the debugger.</span></span>

    <span data-ttu-id="5d026-114">Wenn das Erstellen eines Problems mit dem Problem nicht funktioniert, weil der Aufruf lokal erfolgt oder weil der Fehler lokal auftritt, fügen Sie einen Debugger an den Prozess an, der den Fehler zurückgibt, und platzieren Sie unmittelbar nach dem RPC-Aufruf, der den Fehler erzeugt, einen Haltepunkt.</span><span class="sxs-lookup"><span data-stu-id="5d026-114">If taking a sniff of the problem does not work, because the call is local or because the error originates locally, attach a debugger to the process returning the error and put a breakpoint immediately after the RPC call generating the error.</span></span> <span data-ttu-id="5d026-115">RPC weist häufig auf Fehler hin, indem Ausnahmen ausgelöst werden. Wenn Sie also nach Fehler 1825 (RPC \_ S S \_ \_ pkg- \_ Fehler) suchen, aktivieren Sie Exception 1825, und wenn der Debugger bei dieser Ausnahme anhält, überprüfen Sie die erweiterten Fehlerinformationen für den Thread.</span><span class="sxs-lookup"><span data-stu-id="5d026-115">RPC often indicates errors by throwing exceptions, so if you are looking for error 1825 (RPC\_S\_SEC\_PKG\_ERROR), enable exception 1825 and when the debugger breaks on that exception, examine the extended error information for the thread.</span></span>

 

 




