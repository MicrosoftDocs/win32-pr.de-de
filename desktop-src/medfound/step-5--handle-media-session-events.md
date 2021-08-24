---
description: Dieses Thema ist Schritt 5 des Tutorials Wiedergeben von Mediendateien mit Media Foundation.
ms.assetid: db9b896f-6f56-47b1-b129-331c984e0b16
title: 'Schritt 5: Behandeln von Mediensitzungsereignissen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be80d8d336cb5f3996c72d806259ae8c74eed464245ac439fdd356f091965bde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721900"
---
# <a name="step-5-handle-media-session-events"></a>Schritt 5: Behandeln von Mediensitzungsereignissen

Dieses Thema ist Schritt 5 des Tutorials Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md). Der vollständige Code wird im Thema [Mediensitzung – Wiedergabebeispiel](media-session-playback-example.md)gezeigt.

Hintergrundinformationen zu diesem Thema finden Sie unter [Media Event Generators](media-event-generators.md). Dieses Thema enthält folgende Abschnitte:

-   [Abrufen von Sitzungsereignissen](#getting-session-events)
-   [MESessionTopologyStatus](#mesessiontopologystatus)
-   [MEEndOfPresentation](#meendofpresentation)
-   [MENewPresentation](#menewpresentation)
-   [Zugehörige Themen](#related-topics)

## <a name="getting-session-events"></a>Abrufen von Sitzungsereignissen

Um Ereignisse aus der Mediensitzung abzurufen, ruft das CPlayer-Objekt die [**METHODE SFCMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) auf, wie in [Schritt 4: Erstellen der Mediensitzung](step-4--create-the-media-session.md)gezeigt. Diese Methode ist asynchron, d. h. sie kehrt sofort zum Aufrufer zurück. Wenn das nächste Sitzungsereignis auftritt, ruft die Mediensitzung die [**METHODE AWAITAsyncCallback::Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) des CPlayer-Objekts auf.

Es ist wichtig zu beachten, dass [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) von einem Arbeitsthread aufgerufen wird, nicht vom Anwendungsthread. Daher muss die Implementierung von **Invoke** multithreadsicher sein. Ein Ansatz wäre, die Memberdaten mit einem kritischen Abschnitt zu schützen. Die -Klasse zeigt jedoch `CPlayer` einen alternativen Ansatz:

1.  In der [**Invoke-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) sendet das CPlayer-Objekt eine **WM APP PLAYER \_ \_ \_ EVENT-Nachricht** an die Anwendung. Der Message-Parameter ist ein [**POINTERMediaEvent-Zeiger.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
2.  Die Anwendung empfängt die **WM \_ APP PLAYER \_ \_ EVENT-Nachricht.**
3.  Die Anwendung ruft die -Methode auf `CPlayer::HandleEvent` und übergibt den [**POINTERMediaEvent-Zeiger.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
4.  Die `HandleEvent` -Methode antwortet auf das -Ereignis.

Der folgende Code zeigt die [**Invoke-Methode:**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke)


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



Die [**Invoke-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) führt die folgenden Schritte aus:

1.  Rufen Sie [**DENMEDIAEventGenerator::EndGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-endgetevent) auf, um das Ereignis abzurufen. Diese Methode gibt einen Zeiger auf die [**INTERFACESMediaEvent-Schnittstelle**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent) zurück.
2.  Rufen Sie [**ÜBERMEDIAEVENT::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) auf, um den Ereigniscode abzurufen.
3.  Wenn der Ereigniscode [MESessionClosed](mesessionclosed.md)ist, rufen Sie SetEvent auf, um das *m \_ hCloseEvent-Ereignis* festzulegen. Der Grund für diesen Schritt wird in [Schritt 7: Herunterfahren der Mediensitzung](step-7--shut-down-the-media-session.md)und auch in den Codekommentaren erläutert.
4.  Rufen Sie für alle anderen Ereigniscodes [**DIE AKTION ÜBERMEDIAEVENTGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) auf, um das nächste Ereignis anzufordern.
5.  Posten Sie eine **WM \_ APP \_ \_ PLAYER-EREIGNISmeldung** im Fenster.

Der folgende Code zeigt die HandleEvent-Methode, die aufgerufen wird, wenn die Anwendung die **WM \_ APP PLAYER \_ \_ EVENT-Nachricht** empfängt:


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



Diese Methode ruft [**DASMEDIAEvent::GetType**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-gettype) auf, um den Ereignistyp abzurufen, und [**DENMEDIAEvent::GetStatus,**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus) um den Erfolg des Fehlercodes abzurufen, der dem Ereignis zugeordnet ist. Die nächste ausgeführte Aktion hängt vom Ereigniscode ab.

## <a name="mesessiontopologystatus"></a>MESessionTopologyStatus

Das [MESessionTopologyStatus-Ereignis](mesessiontopologystatus.md) signalisiert eine Änderung des Status der Topologie. Das [**MF \_ EVENT \_ TOPOLOGY \_ STATUS-Attribut**](mf-event-topology-status-attribute.md) des Ereignisobjekts enthält den Status. In diesem Beispiel ist MF **\_ TOPOSTATUS \_ READY** der einzige interessante Wert, der angibt, dass die Wiedergabe für den Start bereit ist.


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



Die `CPlayer::StartPlayback` -Methode wird in [Schritt 6: Steuern der Wiedergabe](step-6--control-playback.md)gezeigt.

In diesem Beispiel wird auch [**MFGetService**](/windows/desktop/api/mfidl/nf-mfidl-mfgetservice) aufgerufen, um die [**SCHNITTSTELLE "THICKNESSVideoDisplayControl"**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) vom [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) abzurufen. Diese Schnittstelle ist erforderlich, um das Neumalieren und Ändern der Größe des Videofensters zu verarbeiten. Dies wird auch in [Schritt 6: Steuern der Wiedergabe](step-6--control-playback.md)gezeigt.

## <a name="meendofpresentation"></a>MEEndOfPresentation

Das [MEEndOfPresentation-Ereignis](meendofpresentation.md) signalisiert, dass die Wiedergabe das Ende der Datei erreicht hat. Die Mediensitzung wechselt automatisch wieder in den Zustand "Beendet".


```C++
//  Handler for MEEndOfPresentation event.
HRESULT CPlayer::OnPresentationEnded(IMFMediaEvent *pEvent)
{
    // The session puts itself into the stopped state automatically.
    m_state = Stopped;
    return S_OK;
}
```



## <a name="menewpresentation"></a>MENewPresentation

Das [MENewPresentation-Ereignis](menewpresentation.md) signalisiert den Beginn einer neuen Präsentation. Die Ereignisdaten sind ein [**POINTERPresentationDescriptor-Zeiger**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) für die neue Präsentation.

In vielen Fällen erhalten Sie dieses Ereignis überhaupt nicht. Wenn Sie dies tun, verwenden Sie den [**POINTERPresentationDescriptor-Zeiger,**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor) um eine neue Wiedergabetopologie zu erstellen, wie in [Schritt 3: Öffnen einer Mediendatei](step-3--open-a-media-file.md)gezeigt. Anschließend wird die neue Topologie in der Mediensitzung in die Warteschlange aufgenommen.


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



Weiter: [Schritt 6: Steuern der Wiedergabe](step-6--control-playback.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> <dt>

[Wiedergeben von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



