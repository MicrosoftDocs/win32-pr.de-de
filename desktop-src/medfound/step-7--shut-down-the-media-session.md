---
description: Dieses Thema ist Schritt 7 des Tutorials zum Wiedergeben von Mediendateien mit Media Foundation.
ms.assetid: c31444df-8717-4ca8-a9ec-72cbb0ee4125
title: 'Schritt 7: Herunterfahren der Medien Sitzung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9fd11cde51b06d932b212f4effabf315deecb7
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132188"
---
# <a name="step-7-shut-down-the-media-session"></a>Schritt 7: Herunterfahren der Medien Sitzung

Dieses Thema ist Schritt 7 des Tutorials zum Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md). Der gesamte Code wird im Thema Beispiel für die [Wiedergabe von Medien Sitzungen](media-session-playback-example.md)angezeigt.

Um die [Medien Sitzung](media-session.md)herunterzufahren, führen Sie die folgenden Schritte aus:

1.  [**Imfmediasession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) wird aufgerufen, um die aktuelle Präsentation zu schließen.
2.  Warten Sie auf das Ereignis [mesessionclosed](mesessionclosed.md) . Dieses Ereignis ist garantiert das letzte Ereignis der Medien Sitzung.
3.  Rückrufe [**imfmediasession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown). Diese Methode bewirkt, dass die Medien Sitzungen Ressourcen freigeben.
4.  Rückruf von [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) für die aktuelle Medienquelle.

Mit der folgenden Methode wird die Medien Sitzung heruntergefahren. Er verwendet ein Ereignis handle (*m \_ hcloseevent*), um auf das [mesessionclosed](mesessionclosed.md) -Ereignis zu warten. Weitere Informationen finden Sie unter [Step 5: handle Media Session Events](step-5--handle-media-session-events.md).


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



Beenden Sie vor dem Beenden der Anwendung die Medien Sitzung, und klicken Sie dann auf [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) , um die Microsoft Media Foundation Plattform zu beenden.


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

 

 



