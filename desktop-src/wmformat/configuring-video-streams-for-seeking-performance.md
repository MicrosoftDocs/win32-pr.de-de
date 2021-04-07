---
title: Konfigurieren von Videostreams zum Suchen der Leistung
description: Konfigurieren von Videostreams zum Suchen der Leistung
ms.assetid: 2df507f9-60a5-4489-b3db-7fe15604e625
keywords:
- Streams, Konfigurieren von Videostreams
- Codecs, Konfigurieren von Videostreams
- Videostreams, konfigurieren
- Videostreams, Leistung
- Leistung, Videostreams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4fc68e0b3a91cf135d29dc7123d5af88db84c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723437"
---
# <a name="configuring-video-streams-for-seeking-performance"></a>Konfigurieren von Videostreams zum Suchen der Leistung

Einige Wiedergabe Anwendungen führen viele Suchvorgänge in einzelnen Streams durch. Die Suche ist ein Bereich, in dem die Leistung je nach den Einstellungen des Streams stark variieren kann. Wenn Sie wissen, dass Ihre Inhalte für die schnelle Suche optimiert werden müssen, können Sie Ihre Datenstrom Konfiguration anpassen, um die Leistung zu verbessern.

Der größte Faktor, der sich auf die Geschwindigkeit von Such Vorgängen in Videos auswirkt, ist der Abstand der Keyframes. Da jeder Frame zwischen Keyframes basierend auf den zuvor enthaltenen Frames rekonstruiert werden muss, ergeben weit verbreitete Keyframes längere Suchzeiten. Wenn z. b. ein Videostream mit 30 Frames pro Sekunde einen maximalen Keyframe-Abstand von 10 Sekunden aufweist, gibt es möglicherweise 300 Frames zwischen Keyframes. Wenn Sie den letzten [*Delta Rahmen*](wmformat-glossary.md)suchen, müssen 299 Frames rekonstruiert werden, damit der Frame entpackt wird. Wenn jede Frame-Wiederherstellung 01 Sekunden gedauert hat, dauert die Suche fast 3 Sekunden. Wenn Sie die Effizienz der Suche erhöhen möchten, kann die Herabsetzung der Keyframe-Abstände helfen. Wenn Sie die Keyframes jedoch zu eng beieinander setzen, können Sie die Qualität verlieren.

Sie können den maximalen Keyframe-Abstand festlegen, indem Sie [**iwmvideomedia-Eigenschaften:: setmaxkeyframespacate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing)aufrufen. Die empfohlenen Werte, die auf der Bitrate des Streams basieren, sind in der folgenden Tabelle aufgeführt. Diese Werte stellen eine gute Balance bei der Suche nach Leistung und Qualität dar. Das SDK erzwingt keine Beschränkung für die Zeit zwischen Keyframes. Im Allgemeinen können sich Zeiten, die länger als 30 Sekunden sind, nachteilig auf die Suchzeiten auswirken, wenn der Inhalt über ein Netzwerk gestreamt wird und wenn der Inhalt lokal wiedergegeben wird.



| Bitrate             | Vorgeschlagene maximale Schlüssel Frame Abstände |
|----------------------|-------------------------------------|
| bis zu 300 KBit/s  | 8 Sekunden                           |
| 300 KBit/s auf 600 | 6 Sekunden                           |
| 600 bis 2 Mbit/s   | 4 Sekunden                           |
| 2 Mbit/s und höher    | 3 Sekunden                           |



 

Weitere Informationen zum erzielen der optimalen Leistung beim Suchen von Videodateien finden Sie unter [erzielen der besten](getting-the-best-video-seeking-performance.md)Leistung beim Suchen von Videodateien.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> </dl>

 

 




