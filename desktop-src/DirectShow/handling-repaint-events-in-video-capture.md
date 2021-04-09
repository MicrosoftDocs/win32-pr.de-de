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
# <a name="handling-repaint-events-in-video-capture"></a><span data-ttu-id="94a30-103">Behandeln von Repaint-Ereignissen in der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="94a30-103">Handling Repaint Events in Video Capture</span></span>

<span data-ttu-id="94a30-104">Wenn Sie ein Video Erfassungs Diagramm ohne Verwendung der [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle erstellen und eine Vorschau des Videos mit dem alten Videorenderer-Filter anzeigen, sollten Sie die Standardbehandlung für [**EC \_ Repaint**](ec-repaint.md) -Ereignisse überschreiben.</span><span class="sxs-lookup"><span data-stu-id="94a30-104">If you build a video capture graph without using the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface, and you preview the video using the old Video Renderer filter, then you should override the default handling for [**EC\_REPAINT**](ec-repaint.md) events.</span></span> <span data-ttu-id="94a30-105">Fragen Sie den Filter Graph-Manager nach der [**imediaevent**](/windows/desktop/api/Control/nn-control-imediaevent) -Schnittstelle ab, und rufen Sie die [**imediaevent:: canceldefaulthandelt**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) -Methode mit dem Wert EC \_ Repaint auf:</span><span class="sxs-lookup"><span data-stu-id="94a30-105">Query the Filter Graph Manager for the [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) interface and call the [**IMediaEvent::CancelDefaultHandling**](/windows/desktop/api/Control/nf-control-imediaevent-canceldefaulthandling) method with the value EC\_REPAINT:</span></span>


```C++
IMediaEvent *pEvent = 0;
hr = pGraph->QueryInterface(IID_IMediaEvent, (void**)&pEvent);
if (SUCCEEDED(hr))
{
    pEvent->CancelDefaultHandling (EC_REPAINT);
    pEvent->Release();
}
```



<span data-ttu-id="94a30-106">Dies verhindert einen möglichen Fehler, durch den die Erfassungs Datei beschädigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="94a30-106">This prevents a possible error that can corrupt your capture file.</span></span> <span data-ttu-id="94a30-107">Wenn der Benutzer das Vorschaufenster abdeckt und seine Darstellung abschließt, empfängt der Videorendererfilter eine WM \_ Paint-Meldung.</span><span class="sxs-lookup"><span data-stu-id="94a30-107">If the user covers and uncovers the preview window, the Video Renderer filter receives a WM\_PAINT message.</span></span> <span data-ttu-id="94a30-108">Standardmäßig fordert der Videorenderer einen neuen Frame an, und der Filter Diagramm-Manager hält das Diagramm an, um einen anderen Videoframe zu finden.</span><span class="sxs-lookup"><span data-stu-id="94a30-108">By default, the Video Renderer requests a new frame, and the Filter Graph Manager pauses the graph in order to cue another video frame.</span></span> <span data-ttu-id="94a30-109">Wenn dies geschieht, während das Diagramm eine Datei schreibt, wird die Datei beschädigt.</span><span class="sxs-lookup"><span data-stu-id="94a30-109">If that happens while the graph is writing a file, it will corrupt the file.</span></span> <span data-ttu-id="94a30-110">Durch Überschreiben des Standard \_ Verhaltens von EC Repaint wird verhindert, dass der Renderer einen neuen Frame anfordert.</span><span class="sxs-lookup"><span data-stu-id="94a30-110">Overriding the default EC\_REPAINT behavior prevents the renderer from requesting a new frame.</span></span>

<span data-ttu-id="94a30-111">Wenn Sie die **ICaptureGraphBuilder2** -Schnittstelle verwenden, müssen Sie diesen Schritt nicht ausführen, da der Erfassungs Diagramm-Generator dies automatisch erledigt.</span><span class="sxs-lookup"><span data-stu-id="94a30-111">You do not have to perform this step if you are using the **ICaptureGraphBuilder2** interface, because the Capture Graph Builder does it for you automatically.</span></span> <span data-ttu-id="94a30-112">Außerdem ist es nicht erforderlich, wenn Sie den Video Mischungs-Renderer (VMR) für die Vorschau verwenden.</span><span class="sxs-lookup"><span data-stu-id="94a30-112">Also, it is not required if you are using the Video Mixing Renderer (VMR) for preview.</span></span> <span data-ttu-id="94a30-113">In VMR ist immer der letzte Frame verfügbar, sodass keine EC \_ Repaint-Ereignisse gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="94a30-113">The VMR always has the most recent frame available, so it does not send EC\_REPAINT events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="94a30-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94a30-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94a30-115">Erweiterte Erfassungs Themen</span><span class="sxs-lookup"><span data-stu-id="94a30-115">Advanced Capture Topics</span></span>](advanced-capture-topics.md)
</dt> <dt>

[<span data-ttu-id="94a30-116">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="94a30-116">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 



