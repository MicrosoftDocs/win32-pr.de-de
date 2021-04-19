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
# <a name="step-6-handle-graph-events"></a>Schritt 6: Behandeln von Diagramm Ereignissen

Dieses Thema ist Schritt 6 des Tutorials [Audio-/Videowiedergabe in DirectShow](audio-video-playback-in-directshow.md). Der gesamte Code wird im Thema [DirectShow-Wiedergabe Beispiel](directshow-playback-example.md)dargestellt.

Wenn die Anwendung eine neue Instanz des Filter Graph-Managers erstellt, ruft die Anwendung [**imediaeventex:: setnotifywindow**](/windows/desktop/api/Control/nf-control-imediaeventex-setnotifywindow)auf. Diese Methode registriert das Anwendungsfenster, um Ereignisse aus dem Filter Diagramm zu empfangen.


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



Der Wert `WM_GRAPH_EVENT` ist eine private Fenster Meldung. Jedes Mal, wenn die Anwendung diese Nachricht empfängt, ruft Sie die- `DShowPlayer::HandleGraphEvent` Methode auf.


```C++
    case WM_GRAPH_EVENT:
       g_pPlayer->HandleGraphEvent(OnGraphEvent);
       return 0;
```



Die `DShowPlayer::HandleGraphEvent`-Methode führt folgende Schritte aus:

1.  Ruft [**imediaevent:: GetEvent**](/windows/desktop/api/Control/nf-control-imediaevent-getevent) in einer Schleife auf, um alle Ereignisse in der Warteschlange zu erhalten.
2.  Ruft eine Rückruffunktion auf (*pfnongraphevent*).
3.  Ruft [**imediaevent:: freeeventparser**](/windows/desktop/api/Control/nf-control-imediaevent-freeeventparams) auf, um die den einzelnen Ereignissen zugeordneten Daten freizugeben.


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



Der folgende Code zeigt die Rückruffunktion, die an die-Funktion an übermittelt wird `DShowPlayer::HandleGraphEvent` . Die-Funktion verarbeitet die Mindestanzahl von Diagramm Ereignissen ([**EC \_ Complete**](ec-complete.md), [**EC \_ errorabort**](ec-errorabort.md)und [**EC \_ userabort**](ec-userabort.md)). Sie können die-Funktion erweitern, um zusätzliche Ereignisse zu behandeln.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audiowiedergabe und Video Wiedergabe in DirectShow](audio-video-playback-in-directshow.md)
</dt> <dt>

[Beispiel zur DirectShow-Wiedergabe](directshow-playback-example.md)
</dt> <dt>

[Ereignis Benachrichtigung in DirectShow](event-notification-in-directshow.md)
</dt> <dt>

[Reagieren auf Ereignisse](responding-to-events.md)
</dt> </dl>

 

 



