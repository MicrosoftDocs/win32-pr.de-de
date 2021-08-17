---
title: Leserantwort auf ASF-Features
description: Leserantwort auf ASF-Features
ms.assetid: 0cf800ca-63e8-47e2-a2fc-7ba6789fb4bb
keywords:
- Windows Medienformat-SDK, Leserantworten auf ASF-Features
- Advanced Systems Format (ASF), Leserantworten auf Features
- ASF (Advanced Systems Format), Leserantworten auf Features
- Leserantworten auf ASF-Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8b8b64649388af6186155009f2a47b0f2b2c96cc42645e64dbb04f3054d7c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119084497"
---
# <a name="reader-response-to-asf-features"></a>Leserantwort auf ASF-Features

Die meisten speziellen ASF-Dateifeatures können in Dateien festgelegt werden, um mit benutzerdefinierten Wiedergabeanwendungen zu interagieren, die für deren Verarbeitung entwickelt wurden. Einige der Features verfügen jedoch über integrierte Unterstützung im Readerobjekt.

Das Readerobjekt wählt automatisch Streams aus Sätzen aus, die sich durch die Bitrate gegenseitig ausschließen. Dieser Sonderfall wird als Multiple Bit Rate (MBR) bezeichnet. Der vom Reader ausgewählte Stream basiert auf der Bitrate des Streams. Die Streamnummer und die Reihenfolge, in der sie dem gegenseitigen Ausschlussobjekt hinzugefügt wurde, sind für die automatische Auswahl irrelevant. Wenn eine Datei mehrere Streams enthält, die sich durch die Bitrate gegenseitig ausschließen, wählt der Reader Streams basierend auf der Berechnung der besten Nutzung der verfügbaren Bandbreite aus.

Der sprachbasierte gegenseitige Ausschluss wird vor der Wiedergabe mithilfe einer Ausgabeeinstellung festgelegt. Wenn Sie sowohl sprachbasierte als auch bitratenbasierten gegenseitigen Ausschluss kombinieren, sollten Sie die bitratenbasierten, sich gegenseitig ausschließenden Datenströme nach Sprache gruppieren und die Gruppen dann nach Sprache ausschließen. Der Reader überprüft zuerst die Sprache und bestimmt dann, welche Bitrate verwendet werden soll.

Die Streampriorisierung wird mithilfe eines Arrays von Datensätzen festgelegt. Die Datensätze im Array befinden sich in absteigender Reihenfolge der Priorität. Der letzte Stream im Array ist der erste, der vom Reader gelöscht wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ASF-Dateifeatures**](asf-file-features.md)
</dt> <dt>

[**Gegenseitiger Ausschluss**](mutual-exclusion.md)
</dt> <dt>

[**Streampriorisierung**](stream-prioritization.md)
</dt> </dl>

 

 




