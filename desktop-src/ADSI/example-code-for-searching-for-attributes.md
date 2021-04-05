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
# <a name="example-code-for-searching-for-attributes"></a>Beispiel Code für die Suche nach Attributen

Im folgenden Codebeispiel wird gezeigt, wie Sie die Such Einstellung **ADS \_ searchpref \_ attribtypes \_ only** suchen verwenden, um nur die Namen von Attributen abzurufen, denen Werte zugewiesen wurden. Im Beispiel wird eine [**ADS- \_ suchpref- \_ Informations**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) Struktur initialisiert, und die Such Einstellung wird durch Aufrufen der [**setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode der [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle festgelegt. Im Beispiel wird dann die [**ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) -Methode aufgerufen, um die Suche auszuführen.


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



 

 




