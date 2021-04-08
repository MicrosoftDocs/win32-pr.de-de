---
description: Dieses Thema ist Schritt 4 des Tutorials zum Wiedergeben von Mediendateien mit Media Foundation.
ms.assetid: fe5e852f-fe0c-439d-b0c5-d32593b587cb
title: 'Schritt 4: Erstellen der Medien Sitzung'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b4c6c9e36552247cb294a7d0d6996fcc0b8a6ec
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103961224"
---
# <a name="step-4-create-the-media-session"></a><span data-ttu-id="ebe6e-103">Schritt 4: Erstellen der Medien Sitzung</span><span class="sxs-lookup"><span data-stu-id="ebe6e-103">Step 4: Create the Media Session</span></span>

<span data-ttu-id="ebe6e-104">Dieses Thema ist Schritt 4 des Tutorials zum Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="ebe6e-104">This topic is step 4 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="ebe6e-105">Der gesamte Code wird im Thema Beispiel für die [Wiedergabe von Medien Sitzungen](media-session-playback-example.md)angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ebe6e-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="ebe6e-106">`CPlayer::CreateSession`Erstellt eine neue Instanz der Medien Sitzung.</span><span class="sxs-lookup"><span data-stu-id="ebe6e-106">The `CPlayer::CreateSession` creates a new instance of the Media Session.</span></span>


```C++
//  Create a new instance of the media session.
HRESULT CPlayer::CreateSession()
{
    // Close the old session, if any.
    HRESULT hr = CloseSession();
    if (FAILED(hr))
    {
        goto done;
    }

    assert(m_state == Closed);

    // Create the media session.
    hr = MFCreateMediaSession(NULL, &m_pSession);
    if (FAILED(hr))
    {
        goto done;
    }

    // Start pulling events from the media session
    hr = m_pSession->BeginGetEvent((IMFAsyncCallback*)this, NULL);
    if (FAILED(hr))
    {
        goto done;
    }

    m_state = Ready;

done:
    return hr;
}
```



<span data-ttu-id="ebe6e-107">Diese Methode führt die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="ebe6e-107">This method performs the following steps:</span></span>

1.  <span data-ttu-id="ebe6e-108">Ruft `CPlayer::CloseSession` auf, um eine vorherige Instanz der Medien Sitzung zu schließen.</span><span class="sxs-lookup"><span data-stu-id="ebe6e-108">Calls `CPlayer::CloseSession` to close any previous instance of the Media Session.</span></span>
2.  <span data-ttu-id="ebe6e-109">Ruft [**mfkreatemediasession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) auf, um eine neue Instanz der Medien Sitzung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ebe6e-109">Calls [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) to create a new instance of the Media Session.</span></span>
3.  <span data-ttu-id="ebe6e-110">Ruft die [**imfmediaeventgenerator:: begingetevent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) -Methode auf, um das nächste Ereignis aus der Medien Sitzung anzufordern.</span><span class="sxs-lookup"><span data-stu-id="ebe6e-110">Calls the [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent) method to request the next event from the Media Session.</span></span> <span data-ttu-id="ebe6e-111">Der erste Parameter für **begingetevent** ist ein Zeiger auf das **cplayer** -Objekt, das die [**imfasynccallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) -Schnittstelle einrichtet.</span><span class="sxs-lookup"><span data-stu-id="ebe6e-111">The first parameter to **BeginGetEvent** is a pointer to the **CPlayer** object itself, which implents the [**IMFAsyncCallback**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) interface.</span></span>

<span data-ttu-id="ebe6e-112">Die Ereignis Behandlung wird in Schritt 5 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ebe6e-112">Event handling is described in step 5.</span></span>

<span data-ttu-id="ebe6e-113">Weiter: [Schritt 5: Behandeln von Ereignissen für Medien Sitzungen](step-5--handle-media-session-events.md)</span><span class="sxs-lookup"><span data-stu-id="ebe6e-113">Next: [Step 5: Handle Media Session Events](step-5--handle-media-session-events.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="ebe6e-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ebe6e-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ebe6e-115">Audio-/Videowiedergabe</span><span class="sxs-lookup"><span data-stu-id="ebe6e-115">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="ebe6e-116">Wiedergeben von Mediendateien mit Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ebe6e-116">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 



