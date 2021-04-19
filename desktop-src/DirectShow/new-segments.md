---
description: Neue Segmente
ms.assetid: 6c470b38-481f-4e52-93b8-eb6b343dcefc
title: Neue Segmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5438cb3b457ed8ea0f77bd2ac1dcc5d6d2c72698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345978"
---
# <a name="new-segments"></a>Neue Segmente

Bei einem *Segment* handelt es sich um eine Gruppe von Medien Beispielen, die eine gemeinsame Startzeit, Endzeit und Wiedergabe Rate gemeinsam verwenden. Die [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) -Methode signalisiert den Anfang eines neuen Segments. Er bietet eine Möglichkeit für einen Quell Filter, Downstream-Filter darüber zu informieren, dass sich die Zeit-und rateninformationen geändert haben. Wenn der Quell Filter z. b. einen neuen Punkt im Stream sucht, wird **newsegment** mit der neuen Startzeit aufgerufen.

Bei einigen downstreamfiltern werden die Segmentinformationen beim Verarbeiten von Beispielen verwendet. Wenn z. b. in einem Format, das die Interframe-Komprimierung verwendet, die Endzeit auf einen Delta Rahmen fällt, muss der Quell Filter möglicherweise nach der Endzeit zusätzliche Proben senden. Dadurch kann der Decoder den abschließenden Delta Frame decodieren. Um den richtigen abschließenden Frame zu ermitteln, verweist der Decoder auf die Endzeit des Segments. Ein weiteres Beispiel ist, dass audiorenderer die Segment Rate zusammen mit der audiosamplingrate verwenden, um die korrekte Audioausgabe zu generieren.

Im Push-Modell initiiert der Quell Filter den **newsegment** -Rückruf. Im Pull-Modell erfolgt dies durch den Parserfilter. In jedem Fall ruft der Filter **newsegment** für die downstreameingabepin auf, die den Aufruf an den nächsten Filter weitergibt, bis der Aufruf den Renderer erreicht. Filter müssen **newsegment** -Aufrufe mit anderen streamingaufrufen serialisieren, wie z. b. [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).

Die streamzeit wird nach jedem neuen Segment auf Null zurückgesetzt. Zeitstempel für Stichproben, die nach dem Segment zugestellt werden, beginnen bei Null.

 

 



