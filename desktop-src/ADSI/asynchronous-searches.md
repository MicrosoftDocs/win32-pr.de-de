---
title: Asynchrone Suchvorgänge
description: Das Aktivieren der asynchronen Suche (Async) führt zum Aufrufen von "GetFirstRow" oder zum ersten Aufrufen von "GetNextRow", bis der erste Eintrag vom Server zurückgegeben wird.
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- Asynchrone Suchvorgänge ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8b8fff875af18b85cdffa4ce67d631d94ed14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947360"
---
# <a name="asynchronous-searches"></a><span data-ttu-id="a9235-104">Asynchrone Suchvorgänge</span><span class="sxs-lookup"><span data-stu-id="a9235-104">Asynchronous Searches</span></span>

<span data-ttu-id="a9235-105">Das Aktivieren der asynchronen Suche (Async) führt zum Aufrufen von " **GetFirstRow** " oder zum ersten Aufrufen von " **GetNextRow** ", bis der erste Eintrag vom Server zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a9235-105">Enabling asynchronous (async) search results in a call to **GetFirstRow** or the first call to **GetNextRow** blocks until the first entry is returned from the server.</span></span> <span data-ttu-id="a9235-106">Das heißt, wenn die Suche auf dem Server viel Zeit erfordert, werden die ersten Ergebnisse schnell zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a9235-106">That is, if the search on the server requires much time, the first few results are returned quickly.</span></span> <span data-ttu-id="a9235-107">Dies kann hilfreich sein, wenn Sie ein Listenfeld mit Suchergebnissen auffüllen.</span><span class="sxs-lookup"><span data-stu-id="a9235-107">This can help when populating a list box with search results.</span></span> <span data-ttu-id="a9235-108">Suchergebnisse werden angezeigt, sobald Sie zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a9235-108">Search results are displayed as they are returned.</span></span>

<span data-ttu-id="a9235-109">Wenn async deaktiviert ist, wird der erste Aufrufen von **GetFirstRow** oder **GetNextRow** blockiert, bis der Server das gesamte Resultset berechnet und zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a9235-109">If async is disabled, the first call to **GetFirstRow** or **GetNextRow** will block until the server computes the entire result set and returns.</span></span> <span data-ttu-id="a9235-110">Nur dann ist die erste zurückgegebene Zeile.</span><span class="sxs-lookup"><span data-stu-id="a9235-110">Only then is the first row returned.</span></span> <span data-ttu-id="a9235-111">Dies wird nicht empfohlen, wenn das Resultset als groß erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="a9235-111">This is not recommended if the result set is expected to be large.</span></span>

<span data-ttu-id="a9235-112">Wenn sowohl Paging als auch Async aktiviert sind, wird der erste Aufrufen von **GetFirstRow** oder **GetNextRow** blockiert, bis der Server die erste Seite der Ergebnisse generiert und sendet.</span><span class="sxs-lookup"><span data-stu-id="a9235-112">If both paging and async are enabled, the first call to **GetFirstRow** or **GetNextRow** will block until the server generates and sends the first page of results.</span></span> <span data-ttu-id="a9235-113">Wenn eine angemessene Seitengröße festgelegt wurde, werden die Ergebnisse sofort angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a9235-113">If a reasonable page size was set, results will appear immediately.</span></span> <span data-ttu-id="a9235-114">Noch wichtiger ist: Wenn die Suchergebnisse sehr groß werden und Sie nach einem bestimmten Eintrag suchen, ist es nicht erforderlich, dass Sie weitere Ergebnisse vom Server anfordern, nachdem Sie die für Sie interessanten Einträge gefunden haben.</span><span class="sxs-lookup"><span data-stu-id="a9235-114">More importantly, if the search results are expected to be very large, and you search for a particular entry, it is not required that you request more results from the server after you have found the entries that interest you.</span></span>

<span data-ttu-id="a9235-115">Eine auslagerbare asynchrone Suche bietet eine gute Kontrolle über eine Suche.</span><span class="sxs-lookup"><span data-stu-id="a9235-115">A paged async search provides fine control of a search.</span></span> <span data-ttu-id="a9235-116">Dies ist hilfreich, wenn die Suchergebnisse sehr groß sein können und eine lange Zeit auf dem Server erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a9235-116">This is useful if the search results may be very large and require extensive time from the server.</span></span>

<span data-ttu-id="a9235-117">Weitere Informationen zur Verwendung von asynchronen Such Vorgängen mit einer bestimmten Suchschnittstelle finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="a9235-117">For more information about using asynchronous searches with a specific search interface, see:</span></span>

-   [<span data-ttu-id="a9235-118">Synchrone und asynchrone Suchvorgänge mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="a9235-118">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [<span data-ttu-id="a9235-119">Suchen mit ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="a9235-119">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="a9235-120">Suchen mit OLE DB</span><span class="sxs-lookup"><span data-stu-id="a9235-120">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




