---
title: Sortieren der Suchergebnisse mit idirector ysearch
description: Standardmäßig werden die Ergebnisse einer Suche in einer nicht garantierten Reihenfolge zurückgegeben. Die Sortierung "ADS \_ searchpref" nach \_ \_ Belieben weist den Server an, das Resultset nach einem angegebenen Attribut Wert zu sortieren, bevor es an den Client zurückgegeben wird.
ms.assetid: 1e44a572-7927-4fd5-a3eb-6dad0760d6e5
ms.tgt_platform: multiple
keywords:
- Sortieren der Suchergebnisse mit idirector ysearch
- ADSI, Search, idirector ysearch, andere Suchoptionen, Sortieren von Suchergebnissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433d24b06ac4d361d6520d8af3376ea12acac1f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730240"
---
# <a name="sorting-the-search-results-with-idirectorysearch"></a><span data-ttu-id="da2a2-106">Sortieren der Suchergebnisse mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="da2a2-106">Sorting the Search Results with IDirectorySearch</span></span>

<span data-ttu-id="da2a2-107">Standardmäßig werden die Ergebnisse einer Suche in einer nicht garantierten Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="da2a2-107">By default, the results of a search are returned in no guaranteed order.</span></span> <span data-ttu-id="da2a2-108">Die **Sortierung "ADS \_ searchpref \_ \_** " nach Belieben weist den Server an, das Resultset nach einem angegebenen Attribut Wert zu sortieren, bevor es an den Client zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="da2a2-108">The **ADS\_SEARCHPREF\_SORT\_ON** preference instructs the server to sort the result set on a specified attribute value before it is returned to the client.</span></span>

<span data-ttu-id="da2a2-109">Es wird empfohlen, dass indizierte Attribute für das Sortieren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da2a2-109">It is recommended that indexed attributes be used for sorting.</span></span> <span data-ttu-id="da2a2-110">Andernfalls muss der Server das gesamte Resultset abrufen und vor dem Senden von Ergebnissen an den Client sortieren.</span><span class="sxs-lookup"><span data-stu-id="da2a2-110">Otherwise, the server must retrieve the complete result set and sort it before sending any results to the client.</span></span> <span data-ttu-id="da2a2-111">Dies gilt auch für auslagerbare Suchvorgänge.</span><span class="sxs-lookup"><span data-stu-id="da2a2-111">This also applies to paged searches.</span></span> <span data-ttu-id="da2a2-112">Beachten Sie, dass die Leistung einer sortierten Suche zunimmt, wenn der Filter ein indiziertes Attribut enthält und dieses Attribut als Sortierschlüssel angegeben wird. in diesem Fall können Active Directory den Sortiervorgang bei der Verarbeitung des Filters erfüllen.</span><span class="sxs-lookup"><span data-stu-id="da2a2-112">Be aware that performance of a sorted search will be increased if the filter includes an indexed attribute and that attribute is specified as the sort key; in this case, Active Directory can satisfy the sort while processing the filter.</span></span> <span data-ttu-id="da2a2-113">Eine effiziente Sortier Abfrage für eine Gruppe von Benutzern könnte z. b. über einen Filter verfügen, der (SN>Smith) und einen Sortierschlüssel von SN enthielt.</span><span class="sxs-lookup"><span data-stu-id="da2a2-113">For example, an efficient sort query for a set of users could have a filter that included (sn>smith) and a sort key of sn.</span></span>

<span data-ttu-id="da2a2-114">Durch die serverseitige Sortierung mit der Option " **ADS \_ searchpref \_ Sort \_ on** Search" wird die Leistung des Servers reduziert.</span><span class="sxs-lookup"><span data-stu-id="da2a2-114">Server-side sorting with the **ADS\_SEARCHPREF\_SORT\_ON** search option will reduce the performance of the server.</span></span> <span data-ttu-id="da2a2-115">Wenn Sie viele Suchvorgänge durchführen, sollten Sie die Ergebnisse manuell auf der Clientseite sortieren, um die Arbeitsauslastung auf dem Server zu verringern.</span><span class="sxs-lookup"><span data-stu-id="da2a2-115">If you will be performing many searches, consider sorting the results manually on the client side to reduce the workload on the server.</span></span>

<span data-ttu-id="da2a2-116">Die Ergebnis Sortierung ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="da2a2-116">By default, result sorting is disabled.</span></span> <span data-ttu-id="da2a2-117">Legen Sie zum Aktivieren der Ergebnis Sortierung **eine ADS \_ searchpref \_ Sort \_ on** Search-Option mit einem **adstype \_ Prov- \_ spezifischen** fest, der auf eine [**ADS \_ SortKey**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) -Struktur im [**ADS \_ searchpref- \_ Informations**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) Array verweist, das an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode weitergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="da2a2-117">To enable result sorting, set an **ADS\_SEARCHPREF\_SORT\_ON** search option with an **ADSTYPE\_PROV\_SPECIFIC** that points to an [**ADS\_SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) structure in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="da2a2-118">Die **ADS \_ SortKey** -Struktur wird verwendet, um das Attribut anzugeben, nach dem sortiert werden soll, und die Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="da2a2-118">The **ADS\_SORTKEY** structure is used to specify the attribute to sort on and the order of the sort.</span></span>

<span data-ttu-id="da2a2-119">Im folgenden Codebeispiel wird gezeigt, wie die Ergebnis Sortierung aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="da2a2-119">The following code example shows how to enable result sorting.</span></span>


```C++
ADS_SORTKEY SortKey;
SortKey.pszAttrType = L"cn";
SortKey.pszReserved = NULL;
SortKey.fReverseorder = FALSE;

ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SORT_ON;
SearchPref.vValue.dwType = ADSTYPE_PROV_SPECIFIC;
SearchPref.vValue.ProviderSpecific.dwLength = sizeof(SortKey);
SearchPref.vValue.ProviderSpecific.lpValue = (LPBYTE)&SortKey;
```



<span data-ttu-id="da2a2-120">Active Directory unterstützt das Sortieren nach konstruierten Attributen nicht, daher ist es nicht möglich, ein konstruiertes Attribut für die Sortierung anzugeben.</span><span class="sxs-lookup"><span data-stu-id="da2a2-120">Active Directory does not support sorting on constructed attributes, so it is not possible to specify a constructed attribute for sorting.</span></span> <span data-ttu-id="da2a2-121">Das Attribut "Unterscheidung nach [**Name**](/windows/desktop/ADSchema/a-distinguishedname) " kann auch nicht für die Sortierung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="da2a2-121">The [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) attribute also cannot be used for sorting.</span></span> <span data-ttu-id="da2a2-122">Active Directory auch das Sortieren nach mehr als einem Attribut nicht zulässt, daher kann die " **ADS \_ searchpref \_ Sort \_** for Search"-Struktur nur eine [**ADS- \_ SortKey**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) -Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="da2a2-122">Active Directory also does not allow sorting on more than one attribute, so the **ADS\_SEARCHPREF\_SORT\_ON** search option can only contain one [**ADS\_SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) structure.</span></span>

 

 