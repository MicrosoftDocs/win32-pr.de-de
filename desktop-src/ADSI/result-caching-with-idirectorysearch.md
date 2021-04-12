---
title: Ergebnis Zwischenspeicherung mit idirector ysearch
description: In der \_ Einstellung "ADS searchpref \_ Cache results" wird \_ das Resultset auf dem Client zwischengespeichert.
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- Ergebnis Zwischenspeicherung mit idirector ysearch ADSI
- ADSI, Search, idirector ysearch, andere Suchoptionen, Ergebnis Zwischenspeicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95016699eb4de36344b7e40f35e1a4a9cce761b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309227"
---
# <a name="result-caching-with-idirectorysearch"></a><span data-ttu-id="989f6-105">Ergebnis Zwischenspeicherung mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="989f6-105">Result Caching with IDirectorySearch</span></span>

<span data-ttu-id="989f6-106">In der Einstellung " **ADS \_ searchpref \_ Cache \_ results** " wird das Resultset auf dem Client zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="989f6-106">The **ADS\_SEARCHPREF\_CACHE\_RESULTS** preference caches the result set on the client.</span></span> <span data-ttu-id="989f6-107">Mithilfe der Ergebnis Zwischenspeicherung kann eine Anwendung ein abgerufenes Resultset beibehalten und die abgerufenen Zeilen erneut durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="989f6-107">Result caching enables an application to retain a retrieved result set and go through the retrieved rows again.</span></span> <span data-ttu-id="989f6-108">Sie ermöglicht auch die Cursor Unterstützung, bei der die Methoden [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) und [**IDirectorySearch:: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) verwendet werden können, um das Resultset nach oben und unten zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="989f6-108">It also enables cursor support where the [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) and [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) methods can be used to move up and down the result set.</span></span>

<span data-ttu-id="989f6-109">Standardmäßig ist die Ergebnis Zwischenspeicherung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="989f6-109">By default, result caching is disabled.</span></span> <span data-ttu-id="989f6-110">Die Ergebnis Zwischenspeicherung sollte aktiviert sein, wenn eine der folgenden Punkte zutrifft:</span><span class="sxs-lookup"><span data-stu-id="989f6-110">Result caching should be enabled if any one of the following is true:</span></span>

-   <span data-ttu-id="989f6-111">, Wenn das gleiche Resultset mehrmals aufgezählt werden muss, ohne dass die Suche erneut auf dem Server durchgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="989f6-111">If the same result set must be enumerated multiple times without performing the search again on the server.</span></span>
-   <span data-ttu-id="989f6-112">Wenn die Suche auf dem Server ressourcenintensiv ist (langsame Verbindung, großes Resultset oder komplexe Abfrage).</span><span class="sxs-lookup"><span data-stu-id="989f6-112">If performing the search is resource-intensive on the server (slow connection, large result set, or complex query).</span></span>
-   <span data-ttu-id="989f6-113">, Wenn die Cursor Unterstützung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="989f6-113">If cursor support is required.</span></span>

<span data-ttu-id="989f6-114">Deaktivieren Sie das Caching, wenn Ihre Anwendung die Arbeitsspeicher Anforderungen für das Zwischenspeichern eines großen Resultsets auf dem Client verringern muss.</span><span class="sxs-lookup"><span data-stu-id="989f6-114">Turn off caching if your application must reduce memory requirements for caching a large result set at the client.</span></span>

<span data-ttu-id="989f6-115">Die Ergebnis Zwischenspeicherung erhöht die Arbeitsspeicher Anforderungen auf dem Client. Daher sollte die Ergebnis Zwischenspeicherung deaktiviert werden, wenn dies ein Problem ist.</span><span class="sxs-lookup"><span data-stu-id="989f6-115">Result caching increases the memory requirements on the client, so result caching should be disabled if this is a concern.</span></span>

<span data-ttu-id="989f6-116">Um die Ergebnis Zwischenspeicherung zu aktivieren, legen Sie die Suchoption **ADS \_ searchpref \_ Cache \_ results** mit dem **\_ booleschen adstype** -Wert **true** im [**ADS \_ searchpref- \_ Informations**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) Array fest, das an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="989f6-116">To enable result caching, set an **ADS\_SEARCHPREF\_CACHE\_RESULTS** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="989f6-117">Im folgenden Codebeispiel wird gezeigt, wie das Zwischenspeichern von Ergebnissen aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="989f6-117">The following code example shows how to enable result caching.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




