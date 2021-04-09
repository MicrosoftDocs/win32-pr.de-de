---
description: Behandeln von Repaint-Ereignissen in der Video Erfassung
ms.assetid: 80739be7-fa38-409d-a827-d788d3044abe
title: Behandeln von Repaint-Ereignissen in der Video Erfassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418ca42ebc80b338b077336fdac48a01dfb8509e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103958066"
---
# <a name="handling-repaint-events-in-video-capture"></a>Behandeln von Repaint-Ereignissen in der Video Erfassung

Wenn Sie ein Video Erfassungs Diagramm ohne Verwendung der [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle erstellen und eine Vorschau des Videos mit dem alten Videorenderer-Filter anzeigen, sollten Sie die Standardbehandlung für [**EC \_ Repaint**](ec-repaint.md) -Ereignisse überschreiben. Fragen Sie den Filter Graph-Manager nach der [**imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent) -Schnittstelle ab, und rufen Sie die [**imediaevent:: canceldefaulthandelt**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) -Methode mit dem Wert EC \_ Repaint auf:


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



Dies verhindert einen möglichen Fehler, durch den die Erfassungs Datei beschädigt werden kann. Wenn der Benutzer das Vorschaufenster abdeckt und seine Darstellung abschließt, empfängt der Videorendererfilter eine WM \_ Paint-Meldung. Standardmäßig fordert der Videorenderer einen neuen Frame an, und der Filter Diagramm-Manager hält das Diagramm an, um einen anderen Videoframe zu finden. Wenn dies geschieht, während das Diagramm eine Datei schreibt, wird die Datei beschädigt. Durch Überschreiben des Standard \_ Verhaltens von EC Repaint wird verhindert, dass der Renderer einen neuen Frame anfordert.

Wenn Sie die **ICaptureGraphBuilder2** -Schnittstelle verwenden, müssen Sie diesen Schritt nicht ausführen, da der Erfassungs Diagramm-Generator dies automatisch erledigt. Außerdem ist es nicht erforderlich, wenn Sie den Video Mischungs-Renderer (VMR) für die Vorschau verwenden. In VMR ist immer der letzte Frame verfügbar, sodass keine EC \_ Repaint-Ereignisse gesendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Erfassungs Themen](advanced-capture-topics.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



