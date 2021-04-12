---
title: Synchrone und asynchrone Suchvorgänge mit idirector ysearch
description: Wenn Sie mithilfe der IDirectorySearch-Schnittstelle eine Suche durchführen, wird die Such Anforderung von der ExecuteSearch-Methode von IDirectorySearch nicht an den Server gesendet.
ms.assetid: c4387202-22a0-497a-af0a-20aa8ede905d
ms.tgt_platform: multiple
keywords:
- Synchrone und asynchrone Suchvorgänge mit idirector ysearch ADSI
- ADSI, Search, idirector ysearch, andere Suchoptionen, synchrone und asynchrone Suchvorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f369d45aaf4453d310c4bac2259bfa9cd089f567
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104387954"
---
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a><span data-ttu-id="a1026-105">Synchrone und asynchrone Suchvorgänge mit idirector ysearch</span><span class="sxs-lookup"><span data-stu-id="a1026-105">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>

<span data-ttu-id="a1026-106">Wenn Sie mithilfe der [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle eine Suche durchführen, sendet die [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) -Methode die Such Anforderung nicht an den Server.</span><span class="sxs-lookup"><span data-stu-id="a1026-106">When you perform a search using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface, the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method does not send the search request to the server.</span></span> <span data-ttu-id="a1026-107">Diese Methode speichert nur die Suchparameter.</span><span class="sxs-lookup"><span data-stu-id="a1026-107">This method only saves the search parameters.</span></span> <span data-ttu-id="a1026-108">Die Such Anforderung wird tatsächlich gesendet, wenn Sie [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) oder [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a1026-108">The search request is actually sent when you call [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).</span></span>

<span data-ttu-id="a1026-109">Bei Active Directory suchen ist der Hauptunterschied zwischen synchronen und asynchronen, wenn die erste Zeile des Ergebnisses zurückgegeben wird, d. h. wenn der erste [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) -oder [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) -Rückruf zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a1026-109">For Active Directory searches, the primary difference between synchronous and asynchronous is when the first row of the result is returned, that is, when the first [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) call returns.</span></span>

<span data-ttu-id="a1026-110">Bei einer synchronen Suche wird die erste Zeile zurückgegeben, wenn der Server erstellt wurde und das gesamte Resultset an den Client zurückgegeben wurde, wenn Paging nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a1026-110">In a synchronous search, if paging is not enabled, the first row is returned when the server has constructed and returned the entire result set to the client.</span></span> <span data-ttu-id="a1026-111">Wenn Paging aktiviert ist, wird die erste Zeile zurückgegeben, wenn die erste Seite des Resultsets zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a1026-111">If paging is enabled, the first row is returned when the first page of the result set is returned.</span></span>

<span data-ttu-id="a1026-112">Bei einer asynchronen Suche wird die erste Zeile zurückgegeben, wenn der Server die erste Zeile des Resultsets erstellt hat, wenn Paging nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="a1026-112">In an asynchronous search, if paging is not enabled, the first row is returned when the server has constructed the first row of the result set.</span></span> <span data-ttu-id="a1026-113">Wenn Paging aktiviert ist, wird die erste Zeile zurückgegeben, wenn die erste Seite des Resultsets zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a1026-113">If paging is enabled, the first row is returned when the first page of the result set is returned.</span></span>

<span data-ttu-id="a1026-114">Der Standard Suchtyp ist synchron.</span><span class="sxs-lookup"><span data-stu-id="a1026-114">The default search type is synchronous.</span></span> <span data-ttu-id="a1026-115">Wenn Sie eine asynchrone Suche angeben möchten, legen Sie die Option für die **\_ \_ asynchrone Suchoption ADS searchpref** mit dem **\_ booleschen adstype** -Wert " **true** " im [**ADS \_ searchpref- \_ Informations**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) Array fest, das an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="a1026-115">To specify an asynchronous search, set an **ADS\_SEARCHPREF\_ASYNCHRONOUS** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="a1026-116">Dieser Vorgang wird im folgenden Codebeispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a1026-116">This operation is shown in the following code example.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




