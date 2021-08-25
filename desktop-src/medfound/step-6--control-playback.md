---
description: Dieses Thema ist Schritt 6 des Tutorials How to Play Media Files with Media Foundation.
ms.assetid: e2e3e95b-41b2-45fb-b495-0e700220e5f5
title: 'Schritt 6: Steuern der Wiedergabe'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef0aa18f671c994837ba195cddba38976c3ffba990eb95748d2bede09141317
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887260"
---
# <a name="step-6-control-playback"></a>Schritt 6: Steuern der Wiedergabe

Dieses Thema ist Schritt 6 des Tutorials [How to Play Media Files with Media Foundation](how-to-play-unprotected-media-files.md). Der vollständige Code wird im Thema [Media Session Playback Example (Media Session Playback Example) gezeigt.](media-session-playback-example.md)

Dieses Thema enthält folgende Abschnitte:

-   [Starten der Wiedergabe](#starting-playback)
-   [Anhalten der Wiedergabe](#pausing-playback)
-   [Beenden der Wiedergabe](#stopping-playback)
-   [Neupaintieren des Videofensters](#repainting-the-video-window)
-   [Ändern der Größe des Videofensters](#resizing-the-video-window)
-   [Zugehörige Themen](#related-topics)

## <a name="starting-playback"></a>Starten der Wiedergabe

Um die Wiedergabe zu starten, rufen [**Sie DIEMEDIASession::Start auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) Der folgende Code zeigt, wie Sie mit der aktuellen Wiedergabeposition beginnen.


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



Die [**Start-Methode**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-start) kann auch eine Anfangsposition relativ zum Anfang der Datei angeben. Weitere Informationen finden Sie im API-Referenzthema.

## <a name="pausing-playback"></a>Anhalten der Wiedergabe

Um die Wiedergabe anzuhalten, rufen [**Sie DIEMEDIASession::P ause auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-pause)


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

Um die Wiedergabe zu beenden, rufen [**Sie DIEMEDIASession::Stop auf.**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-stop) Während die Wiedergabe beendet wird, wird das Videobild deaktiviert, und das Videofenster wird mit der Hintergrundfarbe (standardmäßig schwarz) gestrichen.


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



## <a name="repainting-the-video-window"></a>Neupaintieren des Videofensters

Der [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) zeichnet das Video in dem von der Anwendung angegebenen Fenster. Dies tritt in einem separaten Thread auf, und in den meisten Jahren muss Ihre Anwendung diesen Prozess nicht verwalten. Wenn die Wiedergabe angehalten oder beendet wird, muss der EVR jedoch benachrichtigt werden, wenn das Videofenster eine [**WM \_ PAINT-Nachricht**](../gdi/wm-paint.md) empfängt. Dadurch kann der EVR das Fenster neu anpainten. Um den EVR zu benachrichtigen, rufen Sie [**die METHODE VORVIDEODisplayControl::RepaintVideo**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo) auf:


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



Der folgende Code zeigt den Handler für die [**WM \_ PAINT-Meldung.**](../gdi/wm-paint.md) Diese Funktion sollte über die Meldungsschleife der Anwendung aufgerufen werden.


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



Die `HasVideo` -Methode **gibt TRUE zurück,** `CPlayer` wenn das -Objekt über einen gültigen [**POINTERVIDEODisplayControl-Zeiger**](/windows/desktop/api/evr/nn-evr-imfvideodisplaycontrol) verfügt. (Siehe [Schritt 1: Deklarieren der CPlayer-Klasse](step-1--declare-the-cplayer-class.md).)


```C++
    BOOL          HasVideo() const { return (m_pVideoDisplay != NULL);  }
```



## <a name="resizing-the-video-window"></a>Ändern der Größe des Videofensters

Wenn Sie die Größe des Videofensters ändern, aktualisieren Sie das Zielrechteck auf der EVR, indem Sie die [**METHODE RECTANGLEVideoDisplayControl::SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) aufrufen:


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



Weiter: [Schritt 7: Herunterfahren der Mediensitzung](step-7--shut-down-the-media-session.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> <dt>

[Wiederspielen von Mediendateien mit Media Foundation](how-to-play-unprotected-media-files.md)
</dt> </dl>

 

 
