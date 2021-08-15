---
description: Behandeln von Neupaintereignissen in Video Capture
ms.assetid: 80739be7-fa38-409d-a827-d788d3044abe
title: Behandeln von Neupaintereignissen in Video Capture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 433a9897c7c69119eb54d088aff2d22536e20ae43760cc6b4c9430f9a44f6814
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117999759"
---
# <a name="handling-repaint-events-in-video-capture"></a>Behandeln von Neupaintereignissen in Video Capture

Wenn Sie ein Videoaufnahmediagramm erstellen, ohne die [**ICaptureGraphBuilder2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) zu verwenden, und Sie eine Vorschau des Videos mit dem alten Videorendererfilter anzeigen, sollten Sie die Standardbehandlung für [**EC \_ REPAINT-Ereignisse**](ec-repaint.md) außer Kraft setzen. Fragen Sie den Filter Graph Manager für die [**IMediaEvent-Schnittstelle**](/windows/desktop/api/Control/nn-control-imediaevent) ab, und rufen Sie die [**IMediaEvent::CancelDefaultHandling-Methode**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) mit dem Wert EC \_ REPAINT auf:


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



Dadurch wird ein möglicher Fehler verhindert, der die Erfassungsdatei beschädigt. Wenn der Benutzer das Vorschaufenster abdeckt und aufdeckt, empfängt der Videorendererfilter eine WM \_ PAINT-Meldung. Standardmäßig fordert der Videorenderer einen neuen Frame an, und der Filter-Graph-Manager hält das Diagramm an, um einen anderen Videoframe zu erstellen. Wenn dies geschieht, während der Graph eine Datei schreibt, wird die Datei beschädigt. Das Überschreiben des EC \_ REPAINT-Standardverhaltens verhindert, dass der Renderer einen neuen Frame an fordert.

Sie müssen diesen Schritt nicht ausführen, wenn Sie die **ICaptureGraphBuilder2-Schnittstelle** verwenden, da capture Graph Builder dies automatisch für Sie übernimmt. Außerdem ist dies nicht erforderlich, wenn Sie den Video Mixing Renderer (VMR) für die Vorschau verwenden. Der VMR verfügt immer über den neuesten verfügbaren Frame, sodass keine EC \_ REPAINT-Ereignisse gesendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Erfassungsthemen](advanced-capture-topics.md)
</dt> <dt>

[Ereignisbenachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



