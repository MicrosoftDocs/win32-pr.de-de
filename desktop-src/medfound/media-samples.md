---
description: Erfahren Sie mehr über Medienbeispiele in Microsoft Media Foundation. Ein Medienbeispiel ist ein Objekt, das eine sortierte Liste von null oder mehr Puffern enthält.
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Medienbeispiele (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef5d29b11fb6db316e3fbf6e33e24218ddbbf062
ms.sourcegitcommit: 6fc8a7419bd01787cf6a1c52c355a4a2d1aec471
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/10/2021
ms.locfileid: "111989155"
---
# <a name="media-samples-microsoft-media-foundation"></a>Medienbeispiele (Microsoft Media Foundation)

Ein Medienbeispiel ist ein Objekt, das eine sortierte Liste von null oder mehr Puffern enthält. Medienbeispiele machen die [**INTERFACESSample-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) verfügbar. Die Menge der in einem Beispiel enthaltenen Daten hängt von der Komponente ab, die das Beispiel erstellt, und vom Typ der Daten in den Puffern. Für nicht komprimierte Videos enthält ein Beispiel in der Regel einen einzelnen Videoframe. Bei unkomprimierten Audiodaten kann die Datenmenge variieren, aber in der Regel umfasst ein Audioframe nicht zwei Beispiele. Für komprimierte Daten gelten diese Richtlinien möglicherweise nicht.

Ein einzelnes Beispiel kann aus Effizienzgründen mehrere Puffer enthalten. Beispielsweise wird ein Videoframe in einer ASF-Datei häufig auf mehrere ASF-Pakete verteilt. Die Medienquelle liest die Pakete möglicherweise in mehrere Puffer. Anstatt jedes Fragment in einen Puffer zu kopieren, fügt die Quelle einfach alle Puffer in ein Beispiel ein. Downstreamkomponenten können dann entscheiden, ob die kleineren Puffer in einen zusammenhängenden Puffer kopiert werden sollen. Wenn Sie eine Pipelinekomponente schreiben, sollten Sie im Allgemeinen davon ausgehen, dass jedes Beispiel mehrere Puffer enthalten kann.

In diesem Abschnitt werden die folgenden Themen behandelt:



| Thema                                                        | Beschreibung                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Arbeiten mit Medienbeispielen](working-with-media-samples.md) | Beschreibt das allgemeine Verhalten von Medienbeispielen.                                                                         |
| [Videobeispiele](video-samples.md)                           | Beschreibt eine spezielle Implementierung von [**SPECIALIZEDSample,**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) die für die Aufnahme von unkomprimierten Videoframes entwickelt wurde. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienpuffer](media-buffers.md)
</dt> <dt>

[Media Foundation Primitive](media-foundation-primitives.md)
</dt> </dl>

 

 



