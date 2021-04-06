---
title: Angeben anderer Suchoptionen mit idirector ysearch
description: Die idirector ysearch-Schnittstelle bietet zusätzliche Kontrolle über die Durchführung der Suche durch die Verwendung von Suchoptionen.
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- Angeben anderer Suchoptionen mit idirector ysearch ADSI
- ADSI, Search, idirector ysearch, andere Suchoptionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7064a291c3a299a5435ec454a17b1a666f20d0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947326"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a><span data-ttu-id="59701-105">Angeben anderer Suchoptionen mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="59701-105">Specifying Other Search Options with IDirectorySearch</span></span>

<span data-ttu-id="59701-106">Die [**idirector ysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle bietet zusätzliche Kontrolle über die Durchführung der Suche durch die Verwendung von Suchoptionen.</span><span class="sxs-lookup"><span data-stu-id="59701-106">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provide additional control over how the search is performed through the use of search options.</span></span> <span data-ttu-id="59701-107">Diese Suchoptionen werden festgelegt, indem Sie ein Array von Werbeeinblendungen von [**Werbe \_ \_**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) Einblendungen ausfüllen und die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="59701-107">These search options are set by filling in an array of [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) structures and calling the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="59701-108">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="59701-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="59701-109">Verwenden der setsearchpreference-Methode</span><span class="sxs-lookup"><span data-stu-id="59701-109">Using the SetSearchPreference Method</span></span>](using-the-setsearchpreference-method.md)
-   [<span data-ttu-id="59701-110">Synchrone und asynchrone Suchvorgänge mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="59701-110">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [<span data-ttu-id="59701-111">Paging mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="59701-111">Paging with IDirectorySearch</span></span>](paging-with-idirectorysearch.md)
-   [<span data-ttu-id="59701-112">Ergebnis Zwischenspeicherung mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="59701-112">Result Caching with IDirectorySearch</span></span>](result-caching-with-idirectorysearch.md)
-   [<span data-ttu-id="59701-113">Ausführen einer Attribut Bereichs Abfrage</span><span class="sxs-lookup"><span data-stu-id="59701-113">Performing an Attribute Scope Query</span></span>](performing-an-attribute-scoped-query.md)
-   [<span data-ttu-id="59701-114">Sortieren der Suchergebnisse mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="59701-114">Sorting the Search Results with IDirectorySearch</span></span>](sorting-the-search-results-with-idirectorysearch.md)
-   [<span data-ttu-id="59701-115">Verweis Verfolgung mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="59701-115">Referral Chasing with IDirectorySearch</span></span>](referral-chasing-with-idirectorysearch.md)
-   [<span data-ttu-id="59701-116">Größenbeschränkung mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="59701-116">Size Limit with IDirectorySearch</span></span>](size-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="59701-117">Server Zeit Limit bei idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="59701-117">Server Time Limit with IDirectorySearch</span></span>](server-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="59701-118">Client Zeit Limit mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="59701-118">Client Time Limit with IDirectorySearch</span></span>](client-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="59701-119">Zurückgeben von Attributnamen mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="59701-119">Returning Only Attribute Names with IDirectorySearch</span></span>](returning-only-attribute-names-with-idirectorysearch.md)

 

 




