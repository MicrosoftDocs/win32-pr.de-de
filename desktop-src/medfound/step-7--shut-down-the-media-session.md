---
description: Dieses Thema ist Schritt 7 des Tutorials Wiedergeben von Mediendateien mit Media Foundation.
ms.assetid: c31444df-8717-4ca8-a9ec-72cbb0ee4125
title: 'Schritt 7: Herunterfahren der Mediensitzung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa1eec6e798ee260c83fc1532c2012aed8a53625b12195848ac00fcdcf8fae3b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721944"
---
# <a name="step-7-shut-down-the-media-session"></a>Schritt 7: Herunterfahren der Mediensitzung

Dieses Thema ist Schritt 7 des Tutorials Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md). Der vollständige Code wird im Thema [Mediensitzung – Wiedergabebeispiel](media-session-playback-example.md)gezeigt.

Führen Sie die folgenden Schritte aus, um die [Mediensitzung](media-session.md)herunterzufahren:

1.  Rufen Sie [**DEN AUFRUF VONMEDIASESSION::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) auf, um die aktuelle Präsentation zu schließen.
2.  Warten Sie auf das [MESessionClosed-Ereignis.](mesessionclosed.md) Dieses Ereignis ist garantiert das letzte Ereignis aus der Mediensitzung.
3.  Rufen Sie [**ÜBERMEDIASESSION::Shutdown auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown) Diese Methode bewirkt, dass die Mediensitzungen Ressourcen freigeben.
4.  Rufen Sie FÜR DIE aktuelle Medienquelle [**DEN AUFRUF VONMEDIASOURCE::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) auf.

Mit der folgenden Methode wird die Mediensitzung heruntergefahren. Er verwendet ein Ereignishandle (*m \_ hCloseEvent*), um auf das [MESessionClosed-Ereignis](mesessionclosed.md) zu warten. Weitere Informationen finden Sie unter [Schritt 5: Behandeln von Mediensitzungsereignissen.](step-5--handle-media-session-events.md)


```C++
//  Close the media session. 
HRESULT CPlayer::CloseSession()
{
    //  The IMFMediaSession::Close method is asynchronous, but the 
    //  CPlayer::CloseSession method waits on the MESessionClosed event.
    //  
    //  MESessionClosed is guaranteed to be the last event that the 
    //  media session fires.

    HRESULT hr = S_OK;

    SafeRelease(&m_pVideoDisplay);

    // First close the media session.
    if (m_pSession)
    {
        DWORD dwWaitResult = 0;

        m_state = Closing;
           
        hr = m_pSession->Close();
        // Wait for the close operation to complete
        if (SUCCEEDED(hr))
        {
            dwWaitResult = WaitForSingleObject(m_hCloseEvent, 5000);
            if (dwWaitResult == WAIT_TIMEOUT)
            {
                assert(FALSE);
            }
            // Now there will be no more events from this session.
        }
    }

    // Complete shutdown operations.
    if (SUCCEEDED(hr))
    {
        // Shut down the media source. (Synchronous operation, no events.)
        if (m_pSource)
        {
            (void)m_pSource->Shutdown();
        }
        // Shut down the media session. (Synchronous operation, no events.)
        if (m_pSession)
        {
            (void)m_pSession->Shutdown();
        }
    }

    SafeRelease(&m_pSource);
    SafeRelease(&m_pSession);
    m_state = Closed;
    return hr;
}
```



Bevor die Anwendung beendet wird, fahren Sie die Mediensitzung herunter, und rufen Sie dann [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) auf, um die Microsoft Media Foundation Plattform herunterzufahren.


```C++
//  Release all resources held by this object.
HRESULT CPlayer::Shutdown()
{
    // Close the session
    HRESULT hr = CloseSession();

    // Shutdown the Media Foundation platform
    MFShutdown();

    if (m_hCloseEvent)
    {
        CloseHandle(m_hCloseEvent);
        m_hCloseEvent = NULL;
    }

    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> <dt>

[Wiedergeben von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



