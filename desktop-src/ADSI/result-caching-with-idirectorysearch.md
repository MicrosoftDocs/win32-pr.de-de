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
# <a name="result-caching-with-idirectorysearch"></a>Ergebnis Zwischenspeicherung mit idirector ysearch

In der Einstellung " **ADS \_ searchpref \_ Cache \_ results** " wird das Resultset auf dem Client zwischengespeichert. Mithilfe der Ergebnis Zwischenspeicherung kann eine Anwendung ein abgerufenes Resultset beibehalten und die abgerufenen Zeilen erneut durchlaufen. Sie ermöglicht auch die Cursor Unterstützung, bei der die Methoden [**IDirectorySearch:: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) und [**IDirectorySearch:: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) verwendet werden können, um das Resultset nach oben und unten zu verschieben.

Standardmäßig ist die Ergebnis Zwischenspeicherung deaktiviert. Die Ergebnis Zwischenspeicherung sollte aktiviert sein, wenn eine der folgenden Punkte zutrifft:

-   , Wenn das gleiche Resultset mehrmals aufgezählt werden muss, ohne dass die Suche erneut auf dem Server durchgeführt werden muss.
-   Wenn die Suche auf dem Server ressourcenintensiv ist (langsame Verbindung, großes Resultset oder komplexe Abfrage).
-   , Wenn die Cursor Unterstützung erforderlich ist.

Deaktivieren Sie das Caching, wenn Ihre Anwendung die Arbeitsspeicher Anforderungen für das Zwischenspeichern eines großen Resultsets auf dem Client verringern muss.

Die Ergebnis Zwischenspeicherung erhöht die Arbeitsspeicher Anforderungen auf dem Client. Daher sollte die Ergebnis Zwischenspeicherung deaktiviert werden, wenn dies ein Problem ist.

Um die Ergebnis Zwischenspeicherung zu aktivieren, legen Sie die Suchoption **ADS \_ searchpref \_ Cache \_ results** mit dem **\_ booleschen adstype** -Wert **true** im [**ADS \_ searchpref- \_ Informations**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) Array fest, das an die [**IDirectorySearch:: setsearchpreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) -Methode übermittelt wird.

Im folgenden Codebeispiel wird gezeigt, wie das Zwischenspeichern von Ergebnissen aktiviert wird.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




