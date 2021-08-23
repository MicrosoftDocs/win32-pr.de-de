---
description: Abfragen von Suchfunktionen
ms.assetid: d1d8c708-75f2-4dc7-a33a-8dd2cea0ee00
title: Abfragen von Suchfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d1d4389d9e5fcf1466a039ae48bbffb2c26a41c29281101984f6a7a291789f1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747450"
---
# <a name="querying-for-seeking-capabilities"></a>Abfragen von Suchfunktionen

Microsoft® DirectShow® unterstützt die Suche über die [**IMediaSeeking-Schnittstelle.**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) Der Filter Graph Manager macht diese Schnittstelle verfügbar, aber die Suchfunktionalität wird immer durch Filter im Diagramm implementiert.

Einige Daten können nicht gesucht werden. Beispielsweise können Sie keinen Livevideostream von einer Kamera aus suchen. Wenn ein Stream gesucht werden kann, gibt es jedoch verschiedene Suchtypen, die er unterstützen kann. Dazu zählen unter anderem folgende Einstellungen:

-   Suchen nach einer beliebigen Position im Stream.
-   Abrufen der Dauer des Streams.
-   Abrufen der aktuellen Position im Stream.
-   Wiedergabe in umgekehrter Richtung.

Die **IMediaSeeking-Schnittstelle** definiert einen Satz von Flags, [**AM SEEKING SEEKING \_ \_ \_ CAPABILITIES**](/windows/win32/api/strmif/ne-strmif-am_seeking_seeking_capabilities), die die möglichen Suchfunktionen beschreiben. Um die Funktionen des Streams abzurufen, rufen Sie die [**IMediaSeeking::GetCapabilities-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) auf. Die -Methode gibt eine bitweise Kombination von Flags zurück. Die Anwendung kann sie mit dem operator & (bitweises **AND)** testen. Der folgende Code überprüft beispielsweise, ob das Diagramm an einer beliebigen Position suchen kann:


```C++
DWORD dwCap = 0;
HRESULT hr = pSeek->GetCapabilities(&dwCap);
if (AM_SEEKING_CanSeekAbsolute & dwCap)
{
    // Graph can seek to absolute positions.
}
```



 

 



