---
title: Such Zeitlimit
description: Wenn Sie eine Suche auf einem Server mit hoher Arbeitsauslastung anfordern, empfiehlt es sich, den Server anzuweisen, die Suche auf ein bestimmtes Zeitlimit zu beschränken.
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- Such Zeit Limit ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ff9de38a17fe6ebac4ebb045e2f8b896bc764
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342029"
---
# <a name="search-time-limit"></a><span data-ttu-id="d4ea2-104">Such Zeitlimit</span><span class="sxs-lookup"><span data-stu-id="d4ea2-104">Search Time Limit</span></span>

<span data-ttu-id="d4ea2-105">Wenn Sie eine Suche auf einem Server mit hoher Arbeitsauslastung anfordern, empfiehlt es sich, den Server anzuweisen, die Suche auf ein bestimmtes Zeitlimit zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="d4ea2-105">When you request a search on a server that is under a heavy workload, you may want to instruct the server to restrict the search to a specified time limit.</span></span> <span data-ttu-id="d4ea2-106">Wenn Sie z. b. eine Anwendung ausführen möchten, um einen wöchentlichen Bericht auf einem Server zu generieren, auf dem die Kapazität fast erreicht ist, und um zu vermeiden, dass die CPU-Zeit maximiert und andere Aufträge nicht ausgeführt werden, können Sie die Suchzeit auf einen kleinen Wert festlegen und die Anwendung später erneut ausführen, wenn der Bericht nicht generiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d4ea2-106">For example, to execute an application to generate a weekly report on a server that is running near capacity, and to avoid maximizing the CPU time and preventing other jobs from running, you can set the search time to a small value and rerun the application later if it fails to generate the report.</span></span>

<span data-ttu-id="d4ea2-107">Einige Server können Ihr eigenes Verwaltungszeit Limit erzwingen.</span><span class="sxs-lookup"><span data-stu-id="d4ea2-107">Some servers can impose their own administrative time limit.</span></span> <span data-ttu-id="d4ea2-108">Wenn Sie in diesen Fällen einen Wert für das Limit für die Suche angeben, der größer ist als das administrative Zeit Limit, ignoriert der Server Ihre Spezifikation und verwendet stattdessen die interne administrative Zeitbegrenzung.</span><span class="sxs-lookup"><span data-stu-id="d4ea2-108">In these cases, if you specify a search time limit value greater than the administrative time limit, the server ignores your specification and use its internal administrative time limit instead.</span></span>

<span data-ttu-id="d4ea2-109">Weitere Informationen zur Verwendung der Option für das Suchen von Zeitlimits mit einer bestimmten Suchschnittstelle finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="d4ea2-109">For more information about using the search time limit option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="d4ea2-110">Server Zeit Limit bei idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="d4ea2-110">Server Time Limit with IDirectorySearch</span></span>](server-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="d4ea2-111">Suchen mit ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="d4ea2-111">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="d4ea2-112">Suchen mit OLE DB</span><span class="sxs-lookup"><span data-stu-id="d4ea2-112">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




