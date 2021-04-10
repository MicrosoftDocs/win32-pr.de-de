---
description: Medien Beispiele
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Medien Beispiele (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e10df770f0edcdcb329cf8d2bda3d3dc46acbf6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961169"
---
# <a name="media-samples-microsoft-media-foundation"></a>Medien Beispiele (Microsoft Media Foundation)

Ein Medien Beispiel ist ein Objekt, das eine geordnete Liste von 0 (null) oder mehr Puffern enthält. In Medien Beispielen wird die [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle verfügbar gemacht. Die Datenmenge, die in einem Beispiel enthalten ist, hängt von der Komponente ab, die das Beispiel erstellt, und von der Art der Daten in den Puffern. Für nicht komprimierte Videos enthält ein Beispiel normalerweise einen einzelnen Videoframe. Für nicht komprimierte Audiodaten kann die Datenmenge variieren, aber in der Regel umfasst ein audioframe nicht zwei Beispiele. Bei komprimierten Daten werden diese Richtlinien möglicherweise nicht angewendet.

Eine einzelne Stichprobe kann aus Gründen der Effizienz mehrere Puffer enthalten. Beispielsweise wird in einer ASF-Datei ein videaframe häufig zwischen mehreren ASF-Paketen verteilt. Die Medienquelle liest die Pakete möglicherweise in mehrere Puffer. Anstatt jedes Fragment in einen Puffer zu kopieren, platziert die Quelle einfach alle Puffer in eine Stichprobe. Downstreamkomponenten können dann entscheiden, ob die kleineren Puffer in einen zusammenhängenden Puffer kopiert werden sollen. Wenn Sie eine Pipeline Komponente schreiben, sollten Sie in der Regel davon ausgehen, dass jede Stichprobe mehr als einen Puffer enthalten könnte.

In diesem Abschnitt werden die folgenden Themen behandelt:



| Thema                                                        | BESCHREIBUNG                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Arbeiten mit Medien Beispielen](working-with-media-samples.md) | Beschreibt das allgemeine Verhalten von Medien Beispielen.                                                                         |
| [Video Beispiele](video-samples.md)                           | Beschreibt eine spezialisierte Implementierung von [**IMF Sample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) , die für die Aufnahme nicht komprimierter Video Frames konzipiert ist. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medien Puffer](media-buffers.md)
</dt> <dt>

[Media Foundation primitiver](media-foundation-primitives.md)
</dt> </dl>

 

 



