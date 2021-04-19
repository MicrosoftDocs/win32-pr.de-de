---
title: Zurückgeben von Attributnamen mit idirector ysearch
description: Sie können eine Suche durchführen, um zu ermitteln, welche Art von Daten für ein bestimmtes Objekt verfügbar ist.
ms.assetid: 47e78b79-2063-420b-aa41-f4f0c35f87ea
ms.tgt_platform: multiple
keywords:
- Zurückgeben von Attributnamen mit idirector ysearch ADSI
- ADSI, Search, idirector ysearch, andere Suchoptionen, zurückgeben von Attributnamen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055acbb3fe19969ce95ea77a633e20b195c0257d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341417"
---
# <a name="returning-only-attribute-names-with-idirectorysearch"></a><span data-ttu-id="182ea-105">Zurückgeben von Attributnamen mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="182ea-105">Returning Only Attribute Names with IDirectorySearch</span></span>

<span data-ttu-id="182ea-106">Sie können eine Suche durchführen, um zu ermitteln, welche Art von Daten für ein bestimmtes Objekt verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="182ea-106">You can perform a search to determine what type of data is available for a particular object.</span></span> <span data-ttu-id="182ea-107">In diesem Fall sind Sie nur an den Namen der Attribute interessiert, nicht an den Attributwerten des Objekts.</span><span class="sxs-lookup"><span data-stu-id="182ea-107">In this case, you are only interested in the attributes names, not the attribute values of the object.</span></span> <span data-ttu-id="182ea-108">Die Option **ADS \_ searchpref \_ attribtypes \_ only** bewirkt, dass der Server nur die Attributnamen und nicht die Attributwerte zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="182ea-108">The **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** option causes the server to only return the attribute names and not the attribute values.</span></span> <span data-ttu-id="182ea-109">Das Resultset enthält jedoch nur die Attribute, denen Werte zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="182ea-109">However, the result set includes only those attributes that have values assigned.</span></span> <span data-ttu-id="182ea-110">Nehmen Sie beispielsweise ein Objekt mit den folgenden Attributen:</span><span class="sxs-lookup"><span data-stu-id="182ea-110">For example, consider an object with the following attributes:</span></span>

``` syntax
name = Jeff
sn = Smith
department = Empty
phone = 206-555-0111
```

<span data-ttu-id="182ea-111">Wenn die Option **ADS \_ searchpref \_ attribtypes \_ only** festgelegt ist, enthält das Resultset Folgendes:</span><span class="sxs-lookup"><span data-stu-id="182ea-111">When the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** option is set, the result set includes:</span></span>

``` syntax
name
sn
department
phone
```

<span data-ttu-id="182ea-112">Der Standardwert ist für Attributwerte und Namen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="182ea-112">The default is for both attribute values and names to be returned.</span></span>

<span data-ttu-id="182ea-113">Wenn Sie nur Attributnamen abrufen möchten, legen Sie die Suchoption **ADS \_ searchpref \_ attribtypes \_ only** mit dem **\_ booleschen adstype** -Wert " **true** " im [**ADS \_ searchpref- \_ Informations**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) Array fest, das an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="182ea-113">To retrieve only attribute names, set an **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="182ea-114">Im folgenden Codebeispiel wird gezeigt, wie nur Attributnamen abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="182ea-114">The following code example shows how to retrieve attribute names only.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



<span data-ttu-id="182ea-115">Weitere Informationen und ein Codebeispiel, das zeigt, wie Sie die Suchoption **ADS \_ searchpref \_ attribtypes \_ only** verwenden, finden Sie unter [Beispielcode für die Suche nach Attributen](example-code-for-searching-for-attributes.md).</span><span class="sxs-lookup"><span data-stu-id="182ea-115">For more information and a code example that shows how to use the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search option, see [Example Code for Searching for Attributes](example-code-for-searching-for-attributes.md).</span></span>

 

 




