---
description: Erfahren Sie mehr über Medienbeispiele in Microsoft Media Foundation. Ein Medienbeispiel ist ein Objekt, das eine geordnete Liste von null oder mehr Puffern enthält.
ms.assetid: 14389eea-8091-4c10-849e-53db3e98a7c8
title: Medienbeispiele (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83bad0186d54d99b6c7f7666a5971f6c35e8e2a561109e7bfd6afd45fd5f5e6a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061070"
---
# <a name="media-samples-microsoft-media-foundation"></a>Medienbeispiele (Microsoft Media Foundation)

Ein Medienbeispiel ist ein Objekt, das eine geordnete Liste von null oder mehr Puffern enthält. Medienbeispiele machen die [**BENUTZEROBERFLÄCHESample-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) verfügbar. Die Menge der in einem Beispiel enthaltenen Daten hängt von der Komponente ab, die das Beispiel erstellt, und vom Typ der Daten in den Puffern. Für unkomprimierte Videos enthält ein Beispiel in der Regel einen einzelnen Videoframe. Bei unkomprimierten Audiodaten kann die Datenmenge variieren, aber in der Regel umfasst ein Audioframe nicht zwei Beispiele. Für komprimierte Daten gelten diese Richtlinien möglicherweise nicht.

Eine einzelne Stichprobe kann aus Effizienzgründen mehrere Puffer enthalten. In einer ASF-Datei ist ein Videoframe beispielsweise häufig auf mehrere ASF-Pakete verteilt. Die Medienquelle liest die Pakete möglicherweise in mehrere Puffer ein. Anstatt jedes Fragment in einen Puffer zu kopieren, legt die Quelle einfach alle Puffer in einem Beispiel ab. Downstreamkomponenten können dann entscheiden, ob die kleineren Puffer in einen zusammenhängenden Puffer kopiert werden. Wenn Sie eine Pipelinekomponente schreiben, sollten Sie im Allgemeinen davon ausgehen, dass jedes Beispiel mehr als einen Puffer enthalten kann.

In diesem Abschnitt werden die folgenden Themen behandelt:



| Thema                                                        | BESCHREIBUNG                                                                                                              |
|--------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| [Arbeiten mit Medienbeispielen](working-with-media-samples.md) | Beschreibt das allgemeine Verhalten von Medienbeispielen.                                                                         |
| [Videobeispiele](video-samples.md)                           | Beschreibt eine spezielle [](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) Implementierung von DURCH-Ton-Bild-Paaren, die für das Halten von unkomprimierten Videoframes entwickelt wurde. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Medienpuffer](media-buffers.md)
</dt> <dt>

[Media Foundation Primitive](media-foundation-primitives.md)
</dt> </dl>

 

 



