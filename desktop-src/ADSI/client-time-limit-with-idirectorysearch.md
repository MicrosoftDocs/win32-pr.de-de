---
title: Client Zeit Limit mit idirector ysearch
description: Ein Client kann ein Zeitlimit für einen Server erzwingen, um das Resultset zurückzugeben. Wenn der Server nicht innerhalb des angegebenen Zeitraums auf eine Abfrage reagieren kann, kann der Client die Suche verwerfen und später erneut versuchen.
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- Client Zeit Limit mit idirector ysearch
- ADSI, Search, idirector ysearch, andere Suchoptionen, Client Zeit Limit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed25bd8499f7166d7ea494f71e6f78193f9c778a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339181"
---
# <a name="client-time-limit-with-idirectorysearch"></a><span data-ttu-id="53402-106">Client Zeit Limit mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="53402-106">Client Time Limit with IDirectorySearch</span></span>

<span data-ttu-id="53402-107">Ein Client kann ein Zeitlimit für einen Server erzwingen, um das Resultset zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="53402-107">A client can impose a time limit for a server to return the result set.</span></span> <span data-ttu-id="53402-108">Wenn der Server nicht innerhalb des angegebenen Zeitraums auf eine Abfrage reagieren kann, kann der Client die Suche verwerfen und später erneut versuchen.</span><span class="sxs-lookup"><span data-stu-id="53402-108">When the server fails to respond to a query within the specified time period, the client can abandon the search and try it again later.</span></span>

<span data-ttu-id="53402-109">Die Einstellung für das Client Zeit Limit ist nützlich, wenn ein Client eine asynchrone Suche anfordert.</span><span class="sxs-lookup"><span data-stu-id="53402-109">The client time limit preference is useful when a client requests an asynchronous search.</span></span> <span data-ttu-id="53402-110">Bei einer asynchronen Suche sendet der Client eine Anforderung und fährt dann mit anderen Tasks fort, während er darauf wartet, dass der Server die Ergebnisse zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="53402-110">In an asynchronous search, the client makes a request and then proceeds with other tasks while waiting for the server to return the results.</span></span> <span data-ttu-id="53402-111">Es ist möglich, dass der Server offline geschaltet werden kann, ohne den Client zu benachrichtigen.</span><span class="sxs-lookup"><span data-stu-id="53402-111">It is possible that the server can go offline without notifying the client.</span></span> <span data-ttu-id="53402-112">In diesem Fall wird der Client nicht benachrichtigt, ob der Server die Abfrage noch verarbeitet oder nicht mehr aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="53402-112">In this case, the client will have no notification of whether the server is still processing the query, or if it no longer live.</span></span> <span data-ttu-id="53402-113">Die Einstellung Client Zeit Limit ermöglicht dem Client eine gewisse Kontrolle über solche Situationen.</span><span class="sxs-lookup"><span data-stu-id="53402-113">The client time limit preference gives the client some control of situations like this.</span></span>

<span data-ttu-id="53402-114">Der Standardwert für das Client Zeit Limit ist unbegrenzt.</span><span class="sxs-lookup"><span data-stu-id="53402-114">The default for the client time limit is no limit.</span></span> <span data-ttu-id="53402-115">Zum Festlegen eines Client Zeitlimits legen Sie die Suchoption **ADS \_ searchpref \_ Timeout** mit einem **\_ ganzzahligen adstype** -Wert fest, der das Client Zeitlimit (in Sekunden) in der [**\_ \_ Infodatei von ADS searchpref**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) enthält, die an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="53402-115">To set a client time limit, set an **ADS\_SEARCHPREF\_TIMEOUT** search option with an **ADSTYPE\_INTEGER** value that contains the client time limit, in seconds, in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="53402-116">Ein Client Zeit Limit von 0 (null) gibt keine Zeitbeschränkung an.</span><span class="sxs-lookup"><span data-stu-id="53402-116">A client time limit of zero indicates no time limit.</span></span>

<span data-ttu-id="53402-117">Im folgenden Codebeispiel wird gezeigt, wie das Client Zeit Limit festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="53402-117">The following code example shows how to set the client time limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




