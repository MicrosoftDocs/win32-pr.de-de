---
title: Reader-Antwort auf ASF-Features
description: Reader-Antwort auf ASF-Features
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- Windows Media-Format-SDK, Leser Antworten auf ASF-Features
- Advanced Systems Format (ASF), Leser Antworten auf Features
- ASF (Advanced Systems Format), Reader-Antworten auf Features
- Antworten von Antworten auf ASF-Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 291752d2d011fbc8b0a3e5211c5d8926f94b1cbd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339203"
---
# <a name="reader-response-to-asf-features"></a>Reader-Antwort auf ASF-Features

Die meisten der besonderen Features der ASF-Datei können in Dateien so festgelegt werden, dass Sie mit benutzerdefinierten Spielanwendungen interagieren, die für die Handhabung vorgesehen sind Einige der Features verfügen jedoch über integrierte Unterstützung im Reader-Objekt.

Das Reader-Objekt wählt automatisch Streams aus Sätzen aus, die sich durch die Bitrate gegenseitig ausschließen. Dieser Sonderfall wird als mehrfache Bitrate (Multiple Bitrate, MBR) bezeichnet. Der vom Reader auswählt Stream basiert auf der Bitrate des Streams. Die streamnummer und die Reihenfolge, in der Sie dem gegenseitigen Ausschluss Objekt hinzugefügt wurde, sind für die automatische Auswahl irrelevant. Wenn eine Datei mehr als einen Satz von Streams enthält, die sich gegenseitig von der Bitrate ausschließen, wählt der Reader Streams basierend auf der Berechnung der optimalen Nutzung der verfügbaren Bandbreite aus.

Der sprachbasierte gegenseitige Ausschluss wird vor der Wiedergabe mithilfe einer Ausgabe Einstellung festgelegt. Wenn Sie sowohl den sprach-als auch den Bitrate-basierten gegenseitigen Ausschluss kombinieren, sollten Sie die Bitrate-basierten, sich gegenseitig exklusiven Datenströme nach Sprache gruppieren und dann die Gruppen nach Sprache ausschließen. Der Reader prüft zuerst die Sprache und bestimmt dann, welche Bitrate verwendet werden soll.

Die streampriorisierung wird mithilfe eines Arrays von Datensätzen festgelegt. Die Datensätze im Array sind in absteigender Reihenfolge der Priorität. Der letzte Datenstrom im Array ist der erste, der vom Reader gelöscht wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen der ASF-Datei**](asf-file-features.md)
</dt> <dt>

[**Gegenseitiger Ausschluss**](mutual-exclusion.md)
</dt> <dt>

[**Streampriorisierung**](stream-prioritization.md)
</dt> </dl>

 

 




