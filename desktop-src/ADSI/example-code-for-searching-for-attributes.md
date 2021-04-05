---
title: Beispiel Code für die Suche nach Attributen
description: Im folgenden Codebeispiel wird gezeigt, wie Sie die \_ Such Einstellung ADS searchpref \_ attribtypes \_ only suchen verwenden, um nur die Namen von Attributen abzurufen, denen Werte zugewiesen wurden.
ms.assetid: 0e166f06-6030-4615-a46d-a282961d3b55
ms.tgt_platform: multiple
keywords:
- ADSI, Beispiel Code C/C++, suchen nach Attributen
- Beispiel Code für die Suche nach Attributen
- ADSI, Search, idirector ysearch, andere Suchoptionen, zurückgeben von Attributnamen, Beispiel Code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 344ce99fe9de606212d786ff2e7b88b5eba34d14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707433"
---
# <a name="example-code-for-searching-for-attributes"></a><span data-ttu-id="146ba-106">Beispiel Code für die Suche nach Attributen</span><span class="sxs-lookup"><span data-stu-id="146ba-106">Example Code for Searching for Attributes</span></span>

<span data-ttu-id="146ba-107">Im folgenden Codebeispiel wird gezeigt, wie Sie die Such Einstellung **ADS \_ searchpref \_ attribtypes \_ only** suchen verwenden, um nur die Namen von Attributen abzurufen, denen Werte zugewiesen wurden.</span><span class="sxs-lookup"><span data-stu-id="146ba-107">The following code example shows how to use the **ADS\_SEARCHPREF\_ATTRIBTYPES\_ONLY** search preference to retrieve only the names of attributes to which values have been assigned.</span></span> <span data-ttu-id="146ba-108">Im Beispiel wird eine [**ADS- \_ suchpref- \_ Informations**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) Struktur initialisiert, und die Such Einstellung wird durch Aufrufen der [**setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode der [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle festgelegt.</span><span class="sxs-lookup"><span data-stu-id="146ba-108">The example initializes an [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) structure and sets the search preference by calling the [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method of the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span> <span data-ttu-id="146ba-109">Im Beispiel wird dann die [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) -Methode aufgerufen, um die Suche auszuführen.</span><span class="sxs-lookup"><span data-stu-id="146ba-109">The example then calls the [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method to perform the search.</span></span>


```C++
// Setting the search preference.
// m_pSearch is a valid pointer to an IDirectorySearch interface.
ADS_SEARCHPREF_INFO prefInfo[1];
LPWSTR pszColumn = NULL;

// Set the search preference to indicate attribute names only.
prefInfo[0].dwSearchPref = ADS_SEARCHPREF_ATTRIBTYPES_ONLY;
prefInfo[0].vValue.dwType = ADSTYPE_BOOLEAN;
prefInfo[0].vValue.Integer = TRUE;
hr = m_pSearch->SetSearchPreference(prefInfo, 1);

// Execute the search.
hr = m_pSearch->ExecuteSearch(
                L"(|(objectCategory=domainDNS)(objectCategory=organizationalUnit))", 
                NULL, -1, &hSearch );

if(FAILED(hr))
{
   return;
}

// Retrieve the column name.
hr = m_pSearch->GetNextRow(hSearch);

if(FAILED(hr))
{
   return;
}
    
while( m_pSearch->GetNextColumnName( hSearch, &pszColumn ) != S_ADS_NOMORE_COLUMNS )
{
   wprintf(L"%S ", pszColumn );
   FreeADsMem( pszColumn );
}
```



 

 




