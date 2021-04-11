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
# <a name="step-7-shut-down-the-media-session"></a><span data-ttu-id="880bc-103">Schritt 7: Herunterfahren der Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="880bc-103">Step 7: Shut Down the Media Session</span></span>

<span data-ttu-id="880bc-104">Dieses Thema ist Schritt 7 des Tutorials zum Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="880bc-104">This topic is step 7 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="880bc-105">Der gesamte Code wird im Thema Beispiel für die [Wiedergabe von Medien Sitzungen](media-session-playback-example.md)angezeigt.</span><span class="sxs-lookup"><span data-stu-id="880bc-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="880bc-106">Um die [Medien Sitzung](media-session.md)herunterzufahren, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="880bc-106">To shut down the [Media Session](media-session.md), perform the following steps:</span></span>

1.  <span data-ttu-id="880bc-107">[**Imfmediasession:: Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) wird aufgerufen, um die aktuelle Präsentation zu schließen.</span><span class="sxs-lookup"><span data-stu-id="880bc-107">Call [**IMFMediaSession::Close**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-close) to close the current presentation.</span></span>
2.  <span data-ttu-id="880bc-108">Warten Sie auf das Ereignis [mesessionclosed](mesessionclosed.md) .</span><span class="sxs-lookup"><span data-stu-id="880bc-108">Wait for the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="880bc-109">Dieses Ereignis ist garantiert das letzte Ereignis der Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="880bc-109">This event is guaranteed to be the last event from the Media Session.</span></span>
3.  <span data-ttu-id="880bc-110">Rückrufe [**imfmediasession:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span><span class="sxs-lookup"><span data-stu-id="880bc-110">Call [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="880bc-111">Diese Methode bewirkt, dass die Medien Sitzungen Ressourcen freigeben.</span><span class="sxs-lookup"><span data-stu-id="880bc-111">This method causes the Media Sessions to release resources.</span></span>
4.  <span data-ttu-id="880bc-112">Rückruf von [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) für die aktuelle Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="880bc-112">Call [**IMFMediaSource::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) on the current media source.</span></span>

<span data-ttu-id="880bc-113">Mit der folgenden Methode wird die Medien Sitzung heruntergefahren.</span><span class="sxs-lookup"><span data-stu-id="880bc-113">The following method shuts down the Media Session.</span></span> <span data-ttu-id="880bc-114">Er verwendet ein Ereignis handle (*m \_ hcloseevent*), um auf das [mesessionclosed](mesessionclosed.md) -Ereignis zu warten.</span><span class="sxs-lookup"><span data-stu-id="880bc-114">It uses an event handle (*m\_hCloseEvent*) to wait for the [MESessionClosed](mesessionclosed.md) event.</span></span> <span data-ttu-id="880bc-115">Weitere Informationen finden Sie unter [Step 5: handle Media Session Events](step-5--handle-media-session-events.md).</span><span class="sxs-lookup"><span data-stu-id="880bc-115">See [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md).</span></span>


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



<span data-ttu-id="880bc-116">Beenden Sie vor dem Beenden der Anwendung die Medien Sitzung, und klicken Sie dann auf [**mfshutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) , um die Microsoft Media Foundation Plattform zu beenden.</span><span class="sxs-lookup"><span data-stu-id="880bc-116">Before the application exits, shut down the Media Session, and then call [**MFShutdown**](/windows/desktop/api/mfapi/nf-mfapi-mfshutdown) to shut down the Microsoft Media Foundation platform.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="880bc-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="880bc-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="880bc-118">Audio-/Videowiedergabe</span><span class="sxs-lookup"><span data-stu-id="880bc-118">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="880bc-119">Wiedergeben von Mediendateien mit Media Foundation</span><span class="sxs-lookup"><span data-stu-id="880bc-119">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



