---
title: Ergebniszwischenspeicherung mit IDirectorySearch
description: Die Einstellung ADS \_ SEARCHPREF \_ CACHE RESULTS speichert das \_ Resultset auf dem Client zwischen.
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- Ergebniszwischenspeicherung mit IDirectorySearch ADSI
- ADSI, Search, IDirectorySearch, Andere Suchoptionen, Ergebniszwischenspeicherung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4febc2f02e03759861978e062ee972d8e90df27b996c8161d6163e764fefe9a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838856"
---
# <a name="result-caching-with-idirectorysearch"></a>Ergebniszwischenspeicherung mit IDirectorySearch

Die **Einstellung ADS \_ SEARCHPREF \_ CACHE \_ RESULTS** speichert das Resultset auf dem Client zwischen. Durch die Zwischenspeicherung von Resultsets kann eine Anwendung ein abgerufenes Resultset beibehalten und die abgerufenen Zeilen erneut durchlaufen. Außerdem wird die Cursorunterstützung aktiviert, bei der die Methoden [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) und [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) verwendet werden können, um das Resultset nach oben und unten zu verschieben.

Standardmäßig ist die Ergebniszwischenspeicherung deaktiviert. Die Ergebniszwischenspeicherung sollte aktiviert werden, wenn eine der folgenden Punkte zutrifft:

-   Wenn das gleiche Resultset mehrmals aufzählt werden muss, ohne die Suche erneut auf dem Server durchzuführen.
-   Wenn die Suche auf dem Server ressourcenintensiv ist (langsame Verbindung, großes Resultset oder komplexe Abfrage).
-   Wenn Cursorunterstützung erforderlich ist.

Deaktivieren Sie die Zwischenspeicherung, wenn Ihre Anwendung die Arbeitsspeicheranforderungen für das Zwischenspeichern eines großen Resultset auf dem Client reduzieren muss.

Die Ergebniszwischenspeicherung erhöht die Arbeitsspeicheranforderungen auf dem Client, sodass das Zwischenspeichern von Ergebnisen deaktiviert werden sollte, wenn dies ein Problem ist.

Um das Zwischenspeichern von Ergebnissen zu aktivieren, legen Sie im [**ADS \_ SEARCHPREF \_ INFO-Array,**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) das an die [**IDirectorySearch::SetSearchPreference-Methode**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) übergeben wird, die Suchoption **ADS \_ SEARCHPREF \_ CACHE \_ RESULTS** mit dem **ADSTYPE \_ BOOLEAN-Wert** **TRUE** fest.

Das folgende Codebeispiel zeigt, wie sie die Zwischenspeicherung von Ergebnis aktivieren.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




