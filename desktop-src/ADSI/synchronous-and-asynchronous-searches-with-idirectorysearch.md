---
title: Synchrone und asynchrone Suchvorgänge mit IDirectorySearch
description: Wenn Sie eine Suche mithilfe der IDirectorySearch-Schnittstelle ausführen, sendet die ExecuteSearch-Methode IDirectorySearch die Suchanforderung nicht an den Server.
ms.assetid: c4387202-22a0-497a-af0a-20aa8ede905d
ms.tgt_platform: multiple
keywords:
- Synchrone und asynchrone Suchvorgänge mit IDirectorySearch ADSI
- ADSI, Search, IDirectorySearch, Andere Suchoptionen, synchrone und asynchrone Suchvorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3891351bc7ebb9872938f3022f5397100e0be74ca6cd2d86d21a2535f010cb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118690197"
---
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a>Synchrone und asynchrone Suchvorgänge mit IDirectorySearch

Wenn Sie eine Suche mithilfe der [**IDirectorySearch-Schnittstelle**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) ausführen, sendet die [**IDirectorySearch::ExecuteSearch-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) die Suchanforderung nicht an den Server. Diese Methode speichert nur die Suchparameter. Die Suchanforderung wird tatsächlich gesendet, wenn Sie [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) oder [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow)aufrufen.

Bei Active Directory-Suchen besteht der Hauptunterschied zwischen synchron und asynchron darin, dass die erste Zeile des Ergebnisses zurückgegeben wird, d. h. wenn der erste [**GetFirstRow-**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) oder [**GetNextRow-Aufruf**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) zurückgegeben wird.

Wenn paging in einer synchronen Suche nicht aktiviert ist, wird die erste Zeile zurückgegeben, wenn der Server das gesamte Resultset erstellt und an den Client zurückgegeben hat. Wenn paging aktiviert ist, wird die erste Zeile zurückgegeben, wenn die erste Seite des Resultset zurückgegeben wird.

Wenn paging in einer asynchronen Suche nicht aktiviert ist, wird die erste Zeile zurückgegeben, wenn der Server die erste Zeile des Resultset erstellt hat. Wenn paging aktiviert ist, wird die erste Zeile zurückgegeben, wenn die erste Seite des Resultset zurückgegeben wird.

Der Standardsuchtyp ist synchron. Um eine asynchrone Suche anzugeben, legen Sie eine **ADS \_ SEARCHPREF \_ ASYNCHRONOUS-Suchoption** mit dem **\_ ADSTYPE BOOLEAN-Wert** **TRUE** im [**ADS \_ SEARCHPREF \_ INFO-Array**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) fest, das an die [**IDirectorySearch::SetSearchPreference-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) übergeben wird. Dieser Vorgang wird im folgenden Codebeispiel gezeigt.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




