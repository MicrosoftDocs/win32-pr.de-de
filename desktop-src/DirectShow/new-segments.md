---
description: Neue Segmente
ms.assetid: 6c470b38-481f-4e52-93b8-eb6b343dcefc
title: Neue Segmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28701a29a3b4edd61e9eb408aeab744297eac56408c49dc77dd4328a5afd24b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119790930"
---
# <a name="new-segments"></a>Neue Segmente

Ein *Segment* ist eine Gruppe von Medienbeispielen, die eine gemeinsame Startzeit, Beendigungszeit und Wiedergaberate gemeinsam nutzen. Die [**IPin::NewSegment-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) signalisiert den Anfang eines neuen Segments. Sie bietet eine Möglichkeit für einen Quellfilter, Downstreamfilter darüber zu informieren, dass sich die Zeit- und Rateninformationen geändert haben. Wenn der Quellfilter beispielsweise zu einem neuen Punkt im Stream sucht, ruft er **NewSegment** mit der neuen Startzeit auf.

Einige Downstreamfilter verwenden die Segmentinformationen, wenn sie Beispiele verarbeiten. Wenn z. B. in einem Format, das die Interframekomprimierung verwendet, die Beendigungszeit auf einen Deltaframe fällt, muss der Quellfilter nach der Beendigungszeit möglicherweise zusätzliche Stichproben senden. Dadurch kann der Decoder den endgültigen Deltaframe decodieren. Um den richtigen endgültigen Frame zu bestimmen, verweist der Decoder auf die Beendigungszeit des Segments. Als weiteres Beispiel verwenden Audiorenderer die Segmentrate zusammen mit der Audiosamplingrate, um die richtige Audioausgabe zu generieren.

Im Pushmodell initiiert der Quellfilter den **NewSegment-Aufruf.** Im Pullmodell erfolgt dies durch den Parserfilter. In beiden Fällen ruft der Filter **NewSegment** auf dem Downstreameingabepin auf, der den Aufruf an den nächsten Filter weitergibt, bis der Aufruf den Renderer erreicht. Filter müssen **NewSegment-Aufrufe** mit anderen Streamingaufrufen serialisieren, z.B. [**IMemInputPin::Receive.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)

Die Streamzeit wird nach jedem neuen Segment auf 0 (null) zurückgesetzt. Zeitstempel für Stichproben, die übermittelt werden, nachdem das Segment bei 0 (null) begonnen hat.

 

 



