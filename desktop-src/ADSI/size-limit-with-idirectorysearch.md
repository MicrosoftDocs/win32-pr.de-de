---
title: Größenbeschränkung mit idirector ysearch
description: Der Client kann sich auf eine kleine Anzahl von Objekten konzentrieren, die vom Server zurückgegeben werden, und den Rest des Resultsets ignorieren.
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- Größenbeschränkung mit idirector ysearch ADSI
- ADSI, Search, idirector ysearch, andere Suchoptionen, Größenbeschränkung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25127ea945edcf669e71d7d5b3f969d9eb2cb112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106342028"
---
# <a name="size-limit-with-idirectorysearch"></a><span data-ttu-id="a1c20-105">Größenbeschränkung mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="a1c20-105">Size Limit with IDirectorySearch</span></span>

<span data-ttu-id="a1c20-106">Um die Arbeitsspeicher Anforderung oder andere Zwecke zu verringern, kann sich der Client auf eine kleine Anzahl von Objekten konzentrieren, die vom Server zurückgegeben werden, und den Rest des Resultsets ignorieren, die nicht von Interesse sind.</span><span class="sxs-lookup"><span data-stu-id="a1c20-106">To reduce the memory requirement or for other purposes, the client can focus on a small number of objects returned from the server and ignore the rest of the result set that are not of interest.</span></span> <span data-ttu-id="a1c20-107">Um dies zu erreichen, gibt der Client die Such Größenbeschränkung und andere geeignete Suchkriterien an.</span><span class="sxs-lookup"><span data-stu-id="a1c20-107">To accomplish this, the client specifies the search size limit and other appropriate search criteria.</span></span> <span data-ttu-id="a1c20-108">Wenn das Verzeichnis z. b. die Testergebnisse eines Schulbezirks speichert, können Sie die Top-zehn Studenten mit den höchsten Testergebnissen Abfragen, indem Sie eine Größenbeschränkung von zehn (10) und eine absteigende Sortierreihenfolge angeben.</span><span class="sxs-lookup"><span data-stu-id="a1c20-108">For example, if the directory stores the test scores of a school district, you can query the top ten students with the highest test scores by specifying a size limit of ten (10) and a descending sort order.</span></span>

<span data-ttu-id="a1c20-109">Der Standardwert für die Größenbeschränkung ist nicht begrenzt.</span><span class="sxs-lookup"><span data-stu-id="a1c20-109">The default for size limit is no limit.</span></span> <span data-ttu-id="a1c20-110">Legen Sie zum Festlegen einer Größenbeschränkung eine Suchoption für die Suchoption " **ADS \_ searchpref \_ size \_ Limit** " mit einem **\_ ganzzahligen adstype** -Wert fest, der die maximale Größe in dem an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode über gebenden [**ADS- \_ \_ infoarray**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) enthält.</span><span class="sxs-lookup"><span data-stu-id="a1c20-110">To set a size limit, set an **ADS\_SEARCHPREF\_SIZE\_LIMIT** search option with an **ADSTYPE\_INTEGER** value that contains the maximum size in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="a1c20-111">Im folgenden Codebeispiel wird gezeigt, wie die Größenbeschränkung festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="a1c20-111">The following code example shows how to set the size limit.</span></span> <span data-ttu-id="a1c20-112">Ein Größenlimit von NULL gibt an, dass keine Größenbeschränkung besteht.</span><span class="sxs-lookup"><span data-stu-id="a1c20-112">A size limit value of zero indicates no size limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



<span data-ttu-id="a1c20-113">Für Active Directory gibt die Größenbeschränkung die maximale Anzahl von Objekten an, die von der Suche zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a1c20-113">For Active Directory, the size limit specifies the maximum number of objects to be returned by the search.</span></span> <span data-ttu-id="a1c20-114">Auch für Active Directory beträgt die maximale Anzahl von Objekten, die von einer Suche zurückgegeben werden, 1000 Objekte.</span><span class="sxs-lookup"><span data-stu-id="a1c20-114">Also for Active Directory, the maximum number of objects returned by a search is 1000 objects.</span></span>

 

 




