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
# <a name="step-6-control-playback"></a>Schritt 6: Wiedergabe von Steuerelementen

Dieses Thema ist Schritt 6 des Tutorials zum Wiedergeben von [Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md). Der gesamte Code wird im Thema Beispiel für die [Wiedergabe von Medien Sitzungen](media-session-playback-example.md)angezeigt.

Dieses Thema enthält folgende Abschnitte:

-   [Wiedergabe wird gestartet](#starting-playback)
-   [Anhalten der Wiedergabe](#pausing-playback)
-   [Beenden der Wiedergabe](#stopping-playback)
-   [Neuzeichnen des Video Fensters](#repainting-the-video-window)
-   [Ändern der Größe des Video Fensters](#resizing-the-video-window)
-   [Zugehörige Themen](#related-topics)

## <a name="starting-playback"></a>Wiedergabe wird gestartet

Um die Wiedergabe zu starten, geben Sie [**imfmediasession:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start)an. Der folgende Code zeigt, wie von der aktuellen Wiedergabe Position aus begonnen wird.


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



Die [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) -Methode kann auch eine Anfangsposition relativ zum Anfang der Datei angeben. Weitere Informationen finden Sie im Thema zur API-Referenz.

## <a name="pausing-playback"></a>Anhalten der Wiedergabe

Um die Wiedergabe anzuhalten, nennen Sie [**imfmediasession::P ause**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause).


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



## <a name="stopping-playback"></a>Beenden der Wiedergabe

Um die Wiedergabe anzuhalten, nennen Sie [**imfmediasession:: Beendigung**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop). Beim Beenden der Wiedergabe wird das Videobild gelöscht, und das Videofenster wird mit der Hintergrundfarbe (standardmäßig schwarz) gezeichnet.


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



## <a name="repainting-the-video-window"></a>Neuzeichnen des Video Fensters

Der [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) zeichnet das Video in dem von der Anwendung angegebenen Fenster. Dies erfolgt in einem separaten Thread, und die Anwendung muss den Prozess größtenteils nicht verwalten. Wenn die Wiedergabe angehalten oder angehalten wird, muss der EVR benachrichtigt werden, wenn das Videofenster eine [**WM \_ Paint**](../gdi/wm-paint.md) -Meldung empfängt. Dadurch kann der EVR das Fenster neu zeichnen. Um den EVR zu benachrichtigen, wenden Sie die [**imfvideodisplaycontrol:: repaintvideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) -Methode an:


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



Der folgende Code zeigt den Handler für die [**WM \_**](../gdi/wm-paint.md) -Zeichnungs Nachricht. Diese Funktion sollte von der Nachrichten Schleife der Anwendung aufgerufen werden.


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



Die- `HasVideo` Methode gibt **true** zurück, wenn das- `CPlayer` Objekt einen gültigen [**imfvideodisplaycontrol**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) -Zeiger aufweist. (Siehe [Schritt 1: Deklarieren der cplayer-Klasse](step-1--declare-the-cplayer-class.md).)


```C++
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }
```



## <a name="resizing-the-video-window"></a>Ändern der Größe des Video Fensters

Wenn Sie die Größe des Videofensters ändern, aktualisieren Sie das Ziel Rechteck im EVR, indem Sie die [**imfvideodisplaycontrol:: setvideoposition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) -Methode aufrufen:


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



Weiter: [Schritt 7: Herunterfahren der Medien Sitzung](step-7--shut-down-the-media-session.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> <dt>

[Wiedergeben von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
