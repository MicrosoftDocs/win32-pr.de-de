---
description: Dieses Thema ist Schritt 5 des Tutorials zum Wiedergeben von Mediendateien mit Media Foundation.
ms.assetid: db9b896f-6f56-47b1-b129-331c984e0b16
title: 'Schritt 5: Behandeln von Medien Sitzungs Ereignissen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2ea3092189644f800a5cb27d2e8b07744f5d90c
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106357157"
---
# <a name="step-5-handle-media-session-events"></a>Schritt 5: Behandeln von Medien Sitzungs Ereignissen

Dieses Thema ist Schritt 5 des Tutorials zum Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md). Der gesamte Code wird im Thema Beispiel für die [Wiedergabe von Medien Sitzungen](media-session-playback-example.md)angezeigt.

Hintergrundinformationen zu diesem Thema finden Sie unter [Medienereignis Generatoren](media-event-generators.md). Dieses Thema enthält folgende Abschnitte:

-   [Sitzungs Ereignisse werden erhalten.](#getting-session-events)
-   [Mesessiontopologystatus](#mesessiontopologystatus)
-   [Meendof Presentation](#meendofpresentation)
-   [Menewpresentation](#menewpresentation)
-   [Zugehörige Themen](#related-topics)

## <a name="getting-session-events"></a>Sitzungs Ereignisse werden erhalten.

Um Ereignisse aus der Medien Sitzung zu erhalten, ruft das cplayer-Objekt die [**imfmediaeventgenerator:: begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) -Methode auf, wie in [Schritt 4: Erstellen der Medien Sitzung](step-4--create-the-media-session.md)gezeigt. Diese Methode ist asynchron und bedeutet, dass Sie sofort an den Aufrufer zurückgegeben wird. Wenn das nächste Sitzungs Ereignis auftritt, ruft die Medien Sitzung die [**imfasynccallback:: Aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) -Methode des cplayer-Objekts auf.

Beachten Sie, dass der [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) von einem Arbeits Thread, nicht vom Anwendungs Thread aufgerufen wird. Daher **muss die** Implementierung des Aufrufs multithreadsicher sein. Ein Ansatz besteht darin, die Elementdaten mit einem kritischen Abschnitt zu schützen. Die- `CPlayer` Klasse zeigt jedoch einen alternativen Ansatz:

1.  In der [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode stellt das cplayer-Objekt eine **WM \_ App \_ Player- \_ Ereignis** Meldung an die Anwendung. Der Message-Parameter ist ein [**IMF Media Event**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) -Zeiger.
2.  Die Anwendung empfängt die **WM \_ App \_ Player- \_ Ereignis** Meldung.
3.  Die Anwendung ruft die- `CPlayer::HandleEvent` Methode auf und übergibt den [**IMF Media Event**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) -Zeiger.
4.  Die- `HandleEvent` Methode antwortet auf das-Ereignis.

Der folgende Code zeigt die Methode zum [**aufrufen**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) :


```C++
//  Callback for the asynchronous BeginGetEvent method.

HRESULT CPlayer::Invoke(IMFAsyncResult *pResult)
{
    MediaEventType meType = MEUnknown;  // Event type

    IMFMediaEvent *pEvent = NULL;

    // Get the event from the event queue.
    HRESULT hr = m_pSession->EndGetEvent(pResult, &pEvent);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the event type. 
    hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (meType == MESessionClosed)
    {
        // The session was closed. 
        // The application is waiting on the m_hCloseEvent event handle. 
        SetEvent(m_hCloseEvent);
    }
    else
    {
        // For all other events, get the next event in the queue.
        hr = m_pSession->BeginGetEvent(this, NULL);
        if (FAILED(hr))
        {
            goto done;
        }
    }

    // Check the application state. 
        
    // If a call to IMFMediaSession::Close is pending, it means the 
    // application is waiting on the m_hCloseEvent event and
    // the application's message loop is blocked. 

    // Otherwise, post a private window message to the application. 

    if (m_state != Closing)
    {
        // Leave a reference count on the event.
        pEvent->AddRef();

        PostMessage(m_hwndEvent, WM_APP_PLAYER_EVENT, 
            (WPARAM)pEvent, (LPARAM)meType);
    }

done:
    SafeRelease(&pEvent);
    return S_OK;
}
```



Die [**Aufruf**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Methode führt die folgenden Schritte aus:

1.  Zum Abrufen des Ereignisses muss [**imfmediaeventgenerator:: endgetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) aufgerufen werden. Diese Methode gibt einen Zeiger auf die [**imfmediaevent**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) -Schnittstelle zurück.
2.  Wenn Sie [**imfmediaevent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) aufrufen, um den Ereignis Code abzurufen.
3.  Wenn der Ereignis Code [mesessionclosed](mesessionclosed.md)ist, wird SetEvent aufgerufen, um *das \_ m hcloseevent* -Ereignis festzulegen. Der Grund für diesen Schritt wird in [Schritt 7: Herunterfahren der Medien Sitzung](step-7--shut-down-the-media-session.md)und auch in den Code Kommentaren erläutert.
4.  Für alle anderen Ereignis Codes müssen Sie [**imfmediaeventgenerator:: begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) aufrufen, um das nächste Ereignis anzufordern.
5.  Hiermit wird eine **WM \_ App Player- \_ \_ Ereignis** Meldung im Fenster gepostet.

Der folgende Code zeigt die Methode "Lenker Ereignis", die aufgerufen wird, wenn die Anwendung die Ereignismeldung " **WM \_ App \_ Player \_** " empfängt:


```C++
HRESULT CPlayer::HandleEvent(UINT_PTR pEventPtr)
{
    HRESULT hrStatus = S_OK;            
    MediaEventType meType = MEUnknown;  

    IMFMediaEvent *pEvent = (IMFMediaEvent*)pEventPtr;

    if (pEvent == NULL)
    {
        return E_POINTER;
    }

    // Get the event type.
    HRESULT hr = pEvent->GetType(&meType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the event status. If the operation that triggered the event 
    // did not succeed, the status is a failure code.
    hr = pEvent->GetStatus(&hrStatus);

    // Check if the async operation succeeded.
    if (SUCCEEDED(hr) && FAILED(hrStatus)) 
    {
        hr = hrStatus;
    }
    if (FAILED(hr))
    {
        goto done;
    }

    switch(meType)
    {
    case MESessionTopologyStatus:
        hr = OnTopologyStatus(pEvent);
        break;

    case MEEndOfPresentation:
        hr = OnPresentationEnded(pEvent);
        break;

    case MENewPresentation:
        hr = OnNewPresentation(pEvent);
        break;

    default:
        hr = OnSessionEvent(pEvent, meType);
        break;
    }

done:
    SafeRelease(&pEvent);
    return hr;
}
```



Diese Methode ruft [**imfmediaevent:: GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) auf, um den Ereignistyp und [**imfmediaevent:: GetStatus**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) zu erhalten, um den Erfolg des Fehlercodes zu erhalten, der dem Ereignis zugeordnet ist. Die nächste Aktion, die ausgeführt wird, hängt vom Ereignis Code ab.

## <a name="mesessiontopologystatus"></a>Mesessiontopologystatus

Das Ereignis [mesessiontopologystatus](mesessiontopologystatus.md) signalisiert eine Änderung des Status der Topologie. Das [**MF- \_ Ereignis \_ topologiestatusattribut \_**](mf-event-topology-status-attribute.md) des Ereignis Objekts enthält den Status. In diesem Beispiel ist der einzige relevante Wert " **MF \_ topostatus \_ Ready**", was darauf hinweist, dass die Wiedergabe bereit ist.


```C++
HRESULT CPlayer::OnTopologyStatus(IMFMediaEvent *pEvent)
{
    UINT32 status; 

    HRESULT hr = pEvent->GetUINT32(MF_EVENT_TOPOLOGY_STATUS, &status);
    if (SUCCEEDED(hr) && (status == MF_TOPOSTATUS_READY))
    {
        SafeRelease(&m_pVideoDisplay);

        // Get the IMFVideoDisplayControl interface from EVR. This call is
        // expected to fail if the media file does not have a video stream.

        (void)MFGetService(m_pSession, MR_VIDEO_RENDER_SERVICE, 
            IID_PPV_ARGS(&m_pVideoDisplay));

        hr = StartPlayback();
    }
    return hr;
}
```



Die- `CPlayer::StartPlayback` Methode wird in [Schritt 6: Wiedergabe von Steuer](step-6--control-playback.md)Elementen angezeigt.

In diesem Beispiel wird auch [**mfgetservice**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) aufgerufen, um die [**imfvideodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Schnittstelle vom [erweiterten Videorenderer](enhanced-video-renderer.md) (EVR) zu erhalten. Diese Schnittstelle ist erforderlich, um das Neuzeichnen und die Größe des Videofensters zu verarbeiten, das auch in [Schritt 6: Wiedergabe von Steuer](step-6--control-playback.md)Elementen angezeigt wird.

## <a name="meendofpresentation"></a>Meendof Presentation

Das [meendof Presentation](meendofpresentation.md) -Ereignis signalisiert, dass die Wiedergabe das Ende der Datei erreicht hat. Die Medien Sitzung wechselt automatisch wieder in den Zustand "beendet".


```C++
//  Handler for MEEndOfPresentation event.
HRESULT CPlayer::OnPresentationEnded(IMFMediaEvent *pEvent)
{
    // The session puts itself into the stopped state automatically.
    m_state = Stopped;
    return S_OK;
}
```



## <a name="menewpresentation"></a>Menewpresentation

Das [menewpresentation](menewpresentation.md) -Ereignis signalisiert den Anfang einer neuen Präsentation. Bei den Ereignisdaten handelt es sich um einen [**IMF presentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Zeiger für die neue Präsentation.

In vielen Fällen wird dieses Ereignis überhaupt nicht empfangen. Verwenden Sie in diesem Fall den [**imfpresentationdescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) -Zeiger zum Erstellen einer neuen Wiedergabe Topologie, wie in [Schritt 3: Öffnen einer Mediendatei](step-3--open-a-media-file.md)gezeigt. Stellen Sie dann die neue Topologie in die Medien Sitzung.


```C++
//  Handler for MENewPresentation event.
//
//  This event is sent if the media source has a new presentation, which 
//  requires a new topology. 

HRESULT CPlayer::OnNewPresentation(IMFMediaEvent *pEvent)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFTopology *pTopology = NULL;

    // Get the presentation descriptor from the event.
    HRESULT hr = GetEventObject(pEvent, &pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    // Create a partial topology.
    hr = CreatePlaybackTopology(m_pSource, pPD,  m_hwndVideo,&pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    // Set the topology on the media session.
    hr = m_pSession->SetTopology(0, pTopology);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = OpenPending;

done:
    SafeRelease(&pTopology);
    SafeRelease(&pPD);
    return S_OK;
}
```



Nächstes: [Schritt 6: Wiedergabe von Steuer](step-6--control-playback.md) Elementen

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> <dt>

[Wiedergeben von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



