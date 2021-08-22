---
title: Beispielcode für die Suche nach Attributen
description: Das folgende Codebeispiel zeigt, wie Sie die Sucheinstellung ADS \_ SEARCHPREF \_ ATTRIBTYPES ONLY verwenden, um nur die Namen von Attributen abzurufen, denen \_ Werte zugewiesen wurden.
ms.assetid: 0e166f06-6030-4615-a46d-a282961d3b55
ms.tgt_platform: multiple
keywords:
- ADSI, Beispielcode C/C++, Suchen nach Attributen
- Beispielcode für die Suche nach Attributen
- ADSI, Suchen, IDirectorySearch, andere Suchoptionen, Zurückgeben von nur Attributnamen, Beispielcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 207fcfd2bd688f5bb6ddcd19dcb9b1a87a2e40ddb0a7db1e63e9457e671f9947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118428463"
---
# <a name="example-code-for-searching-for-attributes"></a>Beispielcode für die Suche nach Attributen

Das folgende Codebeispiel zeigt, wie Sie die **Sucheinstellung ADS \_ SEARCHPREF \_ ATTRIBTYPES \_ ONLY** verwenden, um nur die Namen von Attributen abzurufen, denen Werte zugewiesen wurden. Im Beispiel wird eine [**ADS \_ SEARCHPREF \_ INFO-Struktur**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) initialisiert und die Suchpräferenz durch Aufrufen der [**SetSearchPreference-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) der [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) festgelegt. Das Beispiel ruft dann die [**ExecuteSearch-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) auf, um die Suche auszuführen.


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



 

 




