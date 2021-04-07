---
description: Dieses Thema ist Schritt 6 des Tutorials zum Wiedergeben von Mediendateien mit Media Foundation.
ms.assetid: e2e3e95b-41b2-45fb-b495-0e700220e5f5
title: 'Schritt 6: Wiedergabe von Steuerelementen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dfdfecea3484ac6b06cc44e23fd3bd1b3235324e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863411"
---
# <a name="step-6-control-playback"></a><span data-ttu-id="271c9-103">Schritt 6: Wiedergabe von Steuerelementen</span><span class="sxs-lookup"><span data-stu-id="271c9-103">Step 6: Control Playback</span></span>

<span data-ttu-id="271c9-104">Dieses Thema ist Schritt 6 des Tutorials zum Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md).</span><span class="sxs-lookup"><span data-stu-id="271c9-104">This topic is step 6 of the tutorial [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md).</span></span> <span data-ttu-id="271c9-105">Der gesamte Code wird im Thema Beispiel für die [Wiedergabe von Medien Sitzungen](media-session-playback-example.md)angezeigt.</span><span class="sxs-lookup"><span data-stu-id="271c9-105">The complete code is shown in the topic [Media Session Playback Example](media-session-playback-example.md).</span></span>

<span data-ttu-id="271c9-106">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="271c9-106">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="271c9-107">Wiedergabe wird gestartet</span><span class="sxs-lookup"><span data-stu-id="271c9-107">Starting Playback</span></span>](#starting-playback)
-   [<span data-ttu-id="271c9-108">Anhalten der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="271c9-108">Pausing Playback</span></span>](#pausing-playback)
-   [<span data-ttu-id="271c9-109">Beenden der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="271c9-109">Stopping Playback</span></span>](#stopping-playback)
-   [<span data-ttu-id="271c9-110">Neuzeichnen des Video Fensters</span><span class="sxs-lookup"><span data-stu-id="271c9-110">Repainting the Video Window</span></span>](#repainting-the-video-window)
-   [<span data-ttu-id="271c9-111">Ändern der Größe des Video Fensters</span><span class="sxs-lookup"><span data-stu-id="271c9-111">Resizing the Video Window</span></span>](#resizing-the-video-window)
-   [<span data-ttu-id="271c9-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="271c9-112">Related topics</span></span>](#related-topics)

## <a name="starting-playback"></a><span data-ttu-id="271c9-113">Wiedergabe wird gestartet</span><span class="sxs-lookup"><span data-stu-id="271c9-113">Starting Playback</span></span>

<span data-ttu-id="271c9-114">Um die Wiedergabe zu starten, geben Sie [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)an.</span><span class="sxs-lookup"><span data-stu-id="271c9-114">To start playback, call [**IMFMediaSession::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start).</span></span> <span data-ttu-id="271c9-115">Der folgende Code zeigt, wie von der aktuellen Wiedergabe Position aus begonnen wird.</span><span class="sxs-lookup"><span data-stu-id="271c9-115">The following code shows how to start from the current playback position.</span></span>


```C++
//  Start playback from the current position. 
HRESULT CPlayer::StartPlayback()
{
    assert(m_pSession != NULL);

    PROPVARIANT varStart;
    PropVariantInit(&varStart);

    HRESULT hr = m_pSession->Start(&GUID_NULL, &varStart);
    if (SUCCEEDED(hr))
    {
        // Note: Start is an asynchronous operation. However, we
        // can treat our state as being already started. If Start
        // fails later, we'll get an MESessionStarted event with
        // an error code, and we will update our state then.
        m_state = Started;
    }
    PropVariantClear(&varStart);
    return hr;
}

//  Start playback from paused or stopped.
HRESULT CPlayer::Play()
{
    if (m_state != Paused && m_state != Stopped)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL || m_pSource == NULL)
    {
        return E_UNEXPECTED;
    }
    return StartPlayback();
}

```



<span data-ttu-id="271c9-116">Die [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) -Methode kann auch eine Anfangsposition relativ zum Anfang der Datei angeben. Weitere Informationen finden Sie im Thema zur API-Referenz.</span><span class="sxs-lookup"><span data-stu-id="271c9-116">The [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) method can also specify a starting position relative to the start of the file; see the API reference topic for more information.</span></span>

## <a name="pausing-playback"></a><span data-ttu-id="271c9-117">Anhalten der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="271c9-117">Pausing Playback</span></span>

<span data-ttu-id="271c9-118">Um die Wiedergabe anzuhalten, nennen Sie [**imfmediasession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).</span><span class="sxs-lookup"><span data-stu-id="271c9-118">To pause playback, call [**IMFMediaSession::Pause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).</span></span>


```C++
//  Pause playback.
HRESULT CPlayer::Pause()    
{
    if (m_state != Started)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL || m_pSource == NULL)
    {
        return E_UNEXPECTED;
    }

    HRESULT hr = m_pSession->Pause();
    if (SUCCEEDED(hr))
    {
        m_state = Paused;
    }

    return hr;
}
```



## <a name="stopping-playback"></a><span data-ttu-id="271c9-119">Beenden der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="271c9-119">Stopping Playback</span></span>

<span data-ttu-id="271c9-120">Um die Wiedergabe anzuhalten, nennen Sie [**imfmediasession:: Beendigung**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span><span class="sxs-lookup"><span data-stu-id="271c9-120">To stop playback, call [**IMFMediaSession::Stop**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop).</span></span> <span data-ttu-id="271c9-121">Beim Beenden der Wiedergabe wird das Videobild gelöscht, und das Videofenster wird mit der Hintergrundfarbe (standardmäßig schwarz) gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="271c9-121">While playback is stopped, the video image is cleared and the video window is painted with the background color (black by default).</span></span>


```C++
// Stop playback.
HRESULT CPlayer::Stop()
{
    if (m_state != Started && m_state != Paused)
    {
        return MF_E_INVALIDREQUEST;
    }
    if (m_pSession == NULL)
    {
        return E_UNEXPECTED;
    }

    HRESULT hr = m_pSession->Stop();
    if (SUCCEEDED(hr))
    {
        m_state = Stopped;
    }
    return hr;
}
```



## <a name="repainting-the-video-window"></a><span data-ttu-id="271c9-122">Neuzeichnen des Video Fensters</span><span class="sxs-lookup"><span data-stu-id="271c9-122">Repainting the Video Window</span></span>

<span data-ttu-id="271c9-123">Der [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) zeichnet das Video in dem von der Anwendung angegebenen Fenster.</span><span class="sxs-lookup"><span data-stu-id="271c9-123">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) draws the video in the window specified by the application.</span></span> <span data-ttu-id="271c9-124">Dies erfolgt in einem separaten Thread, und die Anwendung muss den Prozess größtenteils nicht verwalten.</span><span class="sxs-lookup"><span data-stu-id="271c9-124">This occurs on a separate thread, and for the most part, your application does not need to manage this process.</span></span> <span data-ttu-id="271c9-125">Wenn die Wiedergabe angehalten oder angehalten wird, muss der EVR benachrichtigt werden, wenn das Videofenster eine [**WM \_ Paint**](../gdi/wm-paint.md) -Meldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="271c9-125">If playback is paused or stopped, however, the EVR must be notified whenever the video window receives a [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span> <span data-ttu-id="271c9-126">Dadurch kann der EVR das Fenster neu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="271c9-126">This allows the EVR to repaint the window.</span></span> <span data-ttu-id="271c9-127">Um den EVR zu benachrichtigen, wenden Sie die [**imfvideodisplaycontrol:: repaintvideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) -Methode an:</span><span class="sxs-lookup"><span data-stu-id="271c9-127">To notify the EVR, call the [**IMFVideoDisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) method:</span></span>


```C++
//  Repaint the video window. Call this method on WM_PAINT.

HRESULT CPlayer::Repaint()
{
    if (m_pVideoDisplay)
    {
        return m_pVideoDisplay->RepaintVideo();
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="271c9-128">Der folgende Code zeigt den Handler für die [**WM \_**](../gdi/wm-paint.md) -Zeichnungs Nachricht.</span><span class="sxs-lookup"><span data-stu-id="271c9-128">The following code shows the handler for the [**WM\_PAINT**](../gdi/wm-paint.md) message.</span></span> <span data-ttu-id="271c9-129">Diese Funktion sollte von der Nachrichten Schleife der Anwendung aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="271c9-129">This function should be called from the application's message loop.</span></span>


```C++
//  Handler for WM_PAINT messages.
void OnPaint(HWND hwnd)
{
    PAINTSTRUCT ps;
    HDC hdc = BeginPaint(hwnd, &ps);

    if (g_pPlayer && g_pPlayer->HasVideo())
    {
        // Video is playing. Ask the player to repaint.
        g_pPlayer->Repaint();
    }
    else
    {
        // The video is not playing, so we must paint the application window.
        RECT rc;
        GetClientRect(hwnd, &rc);
        FillRect(hdc, &rc, (HBRUSH) COLOR_WINDOW);
    }
    EndPaint(hwnd, &ps);
}
```



<span data-ttu-id="271c9-130">Die- `HasVideo` Methode gibt **true** zurück, wenn das- `CPlayer` Objekt einen gültigen [**imfvideodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Zeiger aufweist.</span><span class="sxs-lookup"><span data-stu-id="271c9-130">The `HasVideo` method returns **TRUE** if the `CPlayer` object has a valid [**IMFVideoDisplayControl**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) pointer.</span></span> <span data-ttu-id="271c9-131">(Siehe [Schritt 1: Deklarieren der cplayer-Klasse](step-1--declare-the-cplayer-class.md).)</span><span class="sxs-lookup"><span data-stu-id="271c9-131">(See [Step 1: Declare the CPlayer Class](step-1--declare-the-cplayer-class.md).)</span></span>


```C++
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }
```



## <a name="resizing-the-video-window"></a><span data-ttu-id="271c9-132">Ändern der Größe des Video Fensters</span><span class="sxs-lookup"><span data-stu-id="271c9-132">Resizing the Video Window</span></span>

<span data-ttu-id="271c9-133">Wenn Sie die Größe des Videofensters ändern, aktualisieren Sie das Ziel Rechteck im EVR, indem Sie die [**imfvideodisplaycontrol:: setvideoposition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) -Methode aufrufen:</span><span class="sxs-lookup"><span data-stu-id="271c9-133">If you resize the video window, update the destination rectangle on the EVR by calling the [**IMFVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) method:</span></span>


```C++
//  Resize the video rectangle.
//
//  Call this method if the size of the video window changes.

HRESULT CPlayer::ResizeVideo(WORD width, WORD height)
{
    if (m_pVideoDisplay)
    {
        // Set the destination rectangle.
        // Leave the default source rectangle (0,0,1,1).

        RECT rcDest = { 0, 0, width, height };

        return m_pVideoDisplay->SetVideoPosition(NULL, &rcDest);
    }
    else
    {
        return S_OK;
    }
}
```



<span data-ttu-id="271c9-134">Weiter: [Schritt 7: Herunterfahren der Medien Sitzung](step-7--shut-down-the-media-session.md)</span><span class="sxs-lookup"><span data-stu-id="271c9-134">Next: [Step 7: Shut Down the Media Session](step-7--shut-down-the-media-session.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="271c9-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="271c9-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="271c9-136">Audio-/Videowiedergabe</span><span class="sxs-lookup"><span data-stu-id="271c9-136">Audio/Video Playback</span></span>](audio-video-playback.md)
</dt> <dt>

[<span data-ttu-id="271c9-137">Wiedergeben von Mediendateien mit Media Foundation</span><span class="sxs-lookup"><span data-stu-id="271c9-137">How to Play Media Files with Media Foundation</span></span>](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
