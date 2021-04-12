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
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a>Synchrone und asynchrone Suchvorgänge mit idirector ysearch

Wenn Sie mithilfe der [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) -Schnittstelle eine Suche durchführen, sendet die [**IDirectorySearch:: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) -Methode die Such Anforderung nicht an den Server. Diese Methode speichert nur die Suchparameter. Die Such Anforderung wird tatsächlich gesendet, wenn Sie [**IDirectorySearch:: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) oder [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow)aufrufen.

Bei Active Directory suchen ist der Hauptunterschied zwischen synchronen und asynchronen, wenn die erste Zeile des Ergebnisses zurückgegeben wird, d. h. wenn der erste [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) -oder [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) -Rückruf zurückgegeben wird.

Bei einer synchronen Suche wird die erste Zeile zurückgegeben, wenn der Server erstellt wurde und das gesamte Resultset an den Client zurückgegeben wurde, wenn Paging nicht aktiviert ist. Wenn Paging aktiviert ist, wird die erste Zeile zurückgegeben, wenn die erste Seite des Resultsets zurückgegeben wird.

Bei einer asynchronen Suche wird die erste Zeile zurückgegeben, wenn der Server die erste Zeile des Resultsets erstellt hat, wenn Paging nicht aktiviert ist. Wenn Paging aktiviert ist, wird die erste Zeile zurückgegeben, wenn die erste Seite des Resultsets zurückgegeben wird.

Der Standard Suchtyp ist synchron. Wenn Sie eine asynchrone Suche angeben möchten, legen Sie die Option für die **\_ \_ asynchrone Suchoption ADS searchpref** mit dem **\_ booleschen adstype** -Wert " **true** " im [**ADS \_ searchpref- \_ Informations**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) Array fest, das an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode übermittelt wird. Dieser Vorgang wird im folgenden Codebeispiel gezeigt.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




