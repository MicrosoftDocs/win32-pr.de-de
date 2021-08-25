---
title: Konfigurieren von Video Streams zur Leistungssuche
description: Konfigurieren von Video Streams zur Leistungssuche
ms.assetid: 2df507f9-60a5-4489-b3db-7fe15604e625
keywords:
- Streams,Konfigurieren von Videostreams
- Codecs,Konfigurieren von Videostreams
- Videostreams,Konfigurieren
- Videostreams, Leistung
- Leistung, Videostreams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b7a21e6352d03375b680702a16190b4af9eef24ca7ba9d592adb79ab5794b5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840160"
---
# <a name="configuring-video-streams-for-seeking-performance"></a>Konfigurieren von Video Streams zur Leistungssuche

Einige Wiedergabeanwendungen führen eine große Suchfunktion für einzelne Streams aus. Suchen ist ein Bereich, in dem die Leistung abhängig von den Einstellungen des Streams stark variieren kann. Wenn Sie wissen, dass Ihre Inhalte für die schnelle Suche optimiert werden müssen, können Sie Ihre Streamkonfiguration anpassen, um die Leistung zu verbessern.

Der größte Faktor, der sich auf die Geschwindigkeit von Suchvorgängen im Video auswirkt, ist der Abstand der Keyframes. Da jeder Frame zwischen Keyframes basierend auf den frames rekonstruiert werden muss, die vor ihm stehen, führen keyframes mit großem Abstand zu längeren Suchzeiten. Wenn beispielsweise ein Videostream mit 30 Bildern pro Sekunde einen maximalen Keyframeabstand von 10 Sekunden auf hat, gibt es möglicherweise 300 Frames zwischen Keyframes. Wenn Sie bis zum letzten [*Deltaframe*](wmformat-glossary.md)suchen, müssen 299 Frames rekonstruiert werden, damit der Frame dekomprimiert werden kann. Wenn jeder Frame,01 Sekunden dauert, dauert die Suche fast 3 Sekunden. Wenn Sie die Effizienz der Suche erhöhen möchten, kann das Verringern des Keyframeabstands hilfreich sein. Wenn Sie die Keyframes jedoch zu nah beieinander festlegen, können Sie die Qualität verlieren.

Sie können den maximalen Keyframeabstand festlegen, indem Sie [**IWMVideoMediaProps::SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing)aufrufen. Die empfohlenen Werte, die auf der Bitrate des Streams basieren, sind in der folgenden Tabelle aufgeführt. Diese Werte bieten ein gutes Gleichgewicht zwischen Leistung und Qualität. Das SDK erzwingt keine Begrenzung der Zeit zwischen Keyframes. Im Allgemeinen können sich Zeiten, die länger als 30 Sekunden sind, negativ auf die Suchzeiten auswirken, sowohl wenn der Inhalt über ein Netzwerk gestreamt wird als auch wenn er lokal wiedergegeben wird.



| Bitrate             | Vorgeschlagener maximaler Keyframeabstand |
|----------------------|-------------------------------------|
| 22 KBit/s bis 300 KBit/s  | 8 Sekunden                           |
| 300 KBit/s bis 600 KBit/s | 6 Sekunden                           |
| 600 KBit/s bis 2 MBit/s   | 4 Sekunden                           |
| 2 MBit/s und höher    | 3 Sekunden                           |



 

Weitere Informationen zum Erzielen der besten Leistung bei der Suche nach Videodateien finden Sie unter [Getting the Best Video Seeking Performance](getting-the-best-video-seeking-performance.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> </dl>

 

 




