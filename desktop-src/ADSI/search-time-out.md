---
title: Such Timeout
description: Ein Client kann auch ein Zeitlimit erzwingen, das auf das Zurückgeben des Resultsets durch einen Server gewartet wird.
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- Such Timeout ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfdc63dd4490a840a16eb61598b2461c3e1a40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309220"
---
# <a name="search-time-out"></a><span data-ttu-id="5de19-104">Such Timeout</span><span class="sxs-lookup"><span data-stu-id="5de19-104">Search Time Out</span></span>

<span data-ttu-id="5de19-105">Ein Client kann auch ein Zeitlimit erzwingen, das auf das Zurückgeben des Resultsets durch einen Server gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="5de19-105">A client can also impose a time limit that it will wait for a server to return the result set.</span></span> <span data-ttu-id="5de19-106">Der Wert der Option "Timeout suchen" gibt diesen Grenzwert an.</span><span class="sxs-lookup"><span data-stu-id="5de19-106">The value of the "search time out" option specifies this limit.</span></span> <span data-ttu-id="5de19-107">Wenn der Server nicht innerhalb des angegebenen Zeitraums auf eine Abfrage reagieren kann, kann der Client die Suche beenden und den Vorgang später wiederholen.</span><span class="sxs-lookup"><span data-stu-id="5de19-107">When the server fails to respond to a query within the specified time period, the client can stop the search and try again later.</span></span>

<span data-ttu-id="5de19-108">Die Timeout-Eigenschaft ist nützlich, wenn ein Client eine asynchrone Suche anfordert.</span><span class="sxs-lookup"><span data-stu-id="5de19-108">The time-out property is useful when a client requests an asynchronous search.</span></span> <span data-ttu-id="5de19-109">Bei einer asynchronen Suche sendet der Client eine Anforderung und fährt dann mit anderen Tasks fort, während er darauf wartet, dass der Server die Ergebnisse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5de19-109">In an asynchronous search, the client makes a request and then proceeds with other tasks while waiting for the server to return the results.</span></span> <span data-ttu-id="5de19-110">Es ist möglich, dass der Server offline geschaltet werden kann, ohne den Client zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="5de19-110">It is possible that the server can go offline without notifying the client.</span></span> <span data-ttu-id="5de19-111">In diesem Fall kann der Client nicht erkennen, dass der Server die Abfrage noch verarbeitet oder nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="5de19-111">In this case, the client has no way of recognizing that the server is still processing the query, or if it has ceased to be live.</span></span> <span data-ttu-id="5de19-112">Die Timeout-Eigenschaft stellt dem Client ein Steuerelement in solchen Instanzen bereit.</span><span class="sxs-lookup"><span data-stu-id="5de19-112">The time-out property provides the client some control in such instances.</span></span>

<span data-ttu-id="5de19-113">Weitere Informationen zur Verwendung der Such Timeout Option mit einer bestimmten Suchschnittstelle finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="5de19-113">For more information about using the search time-out option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="5de19-114">Client Zeit Limit mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="5de19-114">Client Time Limit with IDirectorySearch</span></span>](client-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="5de19-115">Suchen mit ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="5de19-115">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="5de19-116">Suchen mit OLE DB</span><span class="sxs-lookup"><span data-stu-id="5de19-116">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




