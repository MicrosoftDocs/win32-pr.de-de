---
description: Dieses Thema ist Schritt 6 des Tutorials Audio-/Videowiedergabe in DirectShow.
ms.assetid: febfe7fa-e5f1-4b37-942a-ed9f8c7c60c1
title: 'Schritt 6: Behandeln von Diagramm Ereignissen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3660e270a542a060ed5e5eee79d5c78c107fea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360741"
---
# <a name="step-6-handle-graph-events"></a><span data-ttu-id="90665-103">Schritt 6: Behandeln von Diagramm Ereignissen</span><span class="sxs-lookup"><span data-stu-id="90665-103">Step 6: Handle Graph Events</span></span>

<span data-ttu-id="90665-104">Dieses Thema ist Schritt 6 des Tutorials [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="90665-104">This topic is step 6 of the tutorial [Audio/Video Playback in DirectShow](audio-video-playback-in-directshow.md).</span></span> <span data-ttu-id="90665-105">Der gesamte Code wird im Thema [DirectShow-Wiedergabe Beispiel](directshow-playback-example.md)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="90665-105">The complete code is shown in the topic [DirectShow Playback Example](directshow-playback-example.md).</span></span>

<span data-ttu-id="90665-106">Wenn die Anwendung eine neue Instanz des Filter Graph-Managers erstellt, ruft die Anwendung [**imediaeventex:: setnotifywindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)auf.</span><span class="sxs-lookup"><span data-stu-id="90665-106">When the application creates a new instance of the Filter Graph Manager, the application calls [**IMediaEventEx::SetNotifyWindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow).</span></span> <span data-ttu-id="90665-107">Diese Methode registriert das Anwendungsfenster, um Ereignisse aus dem Filter Diagramm zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="90665-107">This method registers the application window to receive events from the filter graph.</span></span>


```C++
    hr = m_pGraph->QueryInterface(IID_PPV_ARGS(&m_pEvent));
    if (FAILED(hr))
    {
        goto done;
    }

    // Set up event notification.
    hr = m_pEvent->SetNotifyWindow((OAHWND)m_hwnd, WM_GRAPH_EVENT, NULL);
    if (FAILED(hr))
    {
        goto done;
    }
```



<span data-ttu-id="90665-108">Der Wert `WM_GRAPH_EVENT` ist eine private Fenster Meldung.</span><span class="sxs-lookup"><span data-stu-id="90665-108">The value `WM_GRAPH_EVENT` is a private window message.</span></span> <span data-ttu-id="90665-109">Jedes Mal, wenn die Anwendung diese Nachricht empfängt, ruft Sie die- `DShowPlayer::HandleGraphEvent` Methode auf.</span><span class="sxs-lookup"><span data-stu-id="90665-109">Whenever the application receives this message, it calls the `DShowPlayer::HandleGraphEvent` method.</span></span>


```C++
    case WM_GRAPH_EVENT:
       g_pPlayer->HandleGraphEvent(OnGraphEvent);
       return 0;
```



<span data-ttu-id="90665-110">Die `DShowPlayer::HandleGraphEvent`-Methode führt folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="90665-110">The `DShowPlayer::HandleGraphEvent` method does the following:</span></span>

1.  <span data-ttu-id="90665-111">Ruft [**imediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) in einer Schleife auf, um alle Ereignisse in der Warteschlange zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="90665-111">Calls [**IMediaEvent::GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) in a loop to get all of the queued events.</span></span>
2.  <span data-ttu-id="90665-112">Ruft eine Rückruffunktion auf (*pfnongraphevent*).</span><span class="sxs-lookup"><span data-stu-id="90665-112">Invokes a callback function (*pfnOnGraphEvent*).</span></span>
3.  <span data-ttu-id="90665-113">Ruft [**imediaevent:: freeeventparser**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) auf, um die den einzelnen Ereignissen zugeordneten Daten freizugeben.</span><span class="sxs-lookup"><span data-stu-id="90665-113">Calls [**IMediaEvent::FreeEventParams**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) to free the data associated with each event.</span></span>


```C++
// Respond to a graph event.
//
// The owning window should call this method when it receives the window
// message that the application specified when it called SetEventWindow.
//
// Caution: Do not tear down the graph from inside the callback.

HRESULT DShowPlayer::HandleGraphEvent(GraphEventFN pfnOnGraphEvent)
{
    if (!m_pEvent)
    {
        return E_UNEXPECTED;
    }

    long evCode = 0;
    LONG_PTR param1 = 0, param2 = 0;

    HRESULT hr = S_OK;

    // Get the events from the queue.
    while (SUCCEEDED(m_pEvent->GetEvent(&evCode, &param1, &param2, 0)))
    {
        // Invoke the callback.
        pfnOnGraphEvent(m_hwnd, evCode, param1, param2);

        // Free the event data.
        hr = m_pEvent->FreeEventParams(evCode, param1, param2);
        if (FAILED(hr))
        {
            break;
        }
    }
    return hr;
}
```



<span data-ttu-id="90665-114">Der folgende Code zeigt die Rückruffunktion, die an die-Funktion an übermittelt wird `DShowPlayer::HandleGraphEvent` .</span><span class="sxs-lookup"><span data-stu-id="90665-114">The following code shows the callback function that is passed to `DShowPlayer::HandleGraphEvent`.</span></span> <span data-ttu-id="90665-115">Die-Funktion verarbeitet die Mindestanzahl von Diagramm Ereignissen ([**EC \_ Complete**](ec-complete.md), [**EC \_ errorabort**](ec-errorabort.md)und [**EC \_ userabort**](ec-userabort.md)). Sie können die-Funktion erweitern, um zusätzliche Ereignisse zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="90665-115">The function handles the minimum number of graph events ([**EC\_COMPLETE**](ec-complete.md), [**EC\_ERRORABORT**](ec-errorabort.md), and [**EC\_USERABORT**](ec-userabort.md)); you could expand the function to handle additional events.</span></span>


```C++
void CALLBACK OnGraphEvent(HWND hwnd, long evCode, LONG_PTR param1, LONG_PTR param2)
{
    switch (evCode)
    {
    case EC_COMPLETE:
    case EC_USERABORT:
        g_pPlayer->Stop();
        break;

    case EC_ERRORABORT:
        NotifyError(hwnd, L"Playback error.");
        g_pPlayer->Stop();
        break;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="90665-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="90665-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90665-117">Audiowiedergabe und Video Wiedergabe in DirectShow</span><span class="sxs-lookup"><span data-stu-id="90665-117">Audio/Video Playback in DirectShow</span></span>](audio-video-playback-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="90665-118">Beispiel zur DirectShow-Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="90665-118">DirectShow Playback Example</span></span>](directshow-playback-example.md)
</dt> <dt>

[<span data-ttu-id="90665-119">Ereignis Benachrichtigung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="90665-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="90665-120">Reagieren auf Ereignisse</span><span class="sxs-lookup"><span data-stu-id="90665-120">Responding to Events</span></span>](responding-to-events.md)
</dt> </dl>

 

 



