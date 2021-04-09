---
description: Abfragen der Suchfunktionen
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: Abfragen der Suchfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2aa763ab11267da0a9a13a920285491d83273a8d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860393"
---
# <a name="querying-for-seeking-capabilities"></a>Abfragen der Suchfunktionen

Microsoft® DirectShow® unterstützt das Suchen über die [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle. Der Filter Graph-Manager macht diese Schnittstelle verfügbar, aber die Suchfunktion wird immer durch Filter im Diagramm implementiert.

Für einige Daten kann kein Seeding durchgeführt werden. Beispielsweise können Sie keinen livevideostream von einer Kamera aus suchen. Wenn ein Datenstrom durchsuchbar ist, gibt es jedoch unterschiedliche Typen, die er unterstützen kann. Dazu gehören:

-   Suchen einer beliebigen Position im Stream.
-   Die Dauer des Streams wird abgerufen.
-   Abrufen der aktuellen Position innerhalb des Streams.
-   Spielen in umgekehrter Reihenfolge.

Die **imediaseeking** -Schnittstelle definiert einen Satz von Flags, [**\_ sucht nach \_ Such \_ Funktionen**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), die die möglichen Suchfunktionen beschreiben. Um die Funktionen des Streams abzurufen, rufen Sie die [**imediaseeking:: getfunktionalitäten**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) -Methode auf. Die-Methode gibt eine bitweise Kombination von-Flags zurück. Die Anwendung kann Sie mit dem &-Operator (bitweiser **and-** Operator) testen. Der folgende Code überprüft beispielsweise, ob das Diagramm an einer beliebigen Position suchen kann:


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 



