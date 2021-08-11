---
description: In diesem Thema wird beschrieben, wie Sie mfplay verwenden, um eine Vorschau von Videos von einer Videokamera anzuzeigen.
ms.assetid: ecf6113f-1d8e-4680-87ab-bfd45a9663e4
title: Videovorschau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a58e6c7c70469492ffef38173f0447e19dcf3fe324307e51f3b19609b7d2865
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118237416"
---
# <a name="video-preview"></a>Videovorschau

\[MFPlay ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

In diesem Thema wird beschrieben, wie Sie mfplay verwenden, um eine Vorschau von Videos von einer Videokamera anzuzeigen.

MFPlay bietet die einfachste Möglichkeit in Microsoft Media Foundation, videos von einem Erfassungsgerät in der Vorschau anzuzeigen. Sie sollten MFPlay verwenden, wenn die folgenden Bedingungen erfüllt sind:

-   Sie müssen das Video nicht in einer Datei erfassen.
-   Sie benötigen keine differenzierte Kontrolle darüber, wie das Video gerendert wird. (Beispielsweise müssen Sie die Erstellung des Direct3D-Geräts nicht steuern.)
-   Sie müssen die Videodaten von der Kamera vor dem Rendern nicht verarbeiten.

Andernfalls ist der [Quellleser](source-reader.md) möglicherweise eine bessere Option.

Führen Sie die folgenden Schritte aus, um MFPlay mit einem Videoaufnahmegerät zu verwenden:

1.  Erstellen Sie eine Medienquelle für das Erfassungsgerät. Weitere Informationen finden Sie unter [Enumerating Video Capture Devices (Aufzählen von Videoaufnahmegeräten).](enumerating-video-capture-devices.md)
2.  Rufen Sie [**MFPCreateMediaPlayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) auf, um eine Instanz des Playerobjekts zu erstellen.
3.  Rufen Sie die [**IMFPMediaPlayer::CreateMediaItemFromObject-Methode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) auf. Übergeben Sie einen Zeiger auf die INTERFACESMediaSource-Schnittstelle der Medienquelle. Die -Methode empfängt einen Zeiger auf die [**IMFPMediaItem-Schnittstelle.**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem)
4.  Rufen Sie [**IMFPMediaPlayer::SetMediaItem auf.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem)
5.  Rufen Sie [**IMFPMediaPlayer::P lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) auf, um mit der Vorschau zu beginnen.

Diese Schritte sind im folgenden Code dargestellt:


```C++
    IMFPMediaItem *pItem = NULL;

    if (SUCCEEDED(hr))
    {
        hr = MFPCreateMediaPlayer(
            NULL,       // URL.
            FALSE,      // Do not start playback yet.
            0,          // Option flags.
            NULL,       // Callback interface.
            hwnd,
            &g_pPlayer
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->CreateMediaItemFromObject(
            g_pSource,
            TRUE,       // Blocking call.
            0,          // User data.
            &pItem
            );
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
        hr = g_pPlayer->Play();
    }

    SafeRelease(&pItem);
```



In einer typischen Anwendung würden Sie einen Zeiger auf eine Rückrufschnittstelle in der [**MFPCreateMediaPlayer-Funktion**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) bereitstellen und die Rückrufschnittstelle verwenden, um Ereignisse vom Player abzurufen. Der Einfachheit halber überspringt der hier gezeigte Code diese Schritte. Weitere Informationen finden Sie unter [Erste Schritte mit MFPlay.](getting-started-with-mfplay.md)

### <a name="shutting-down"></a>Herunterfahren

Bevor die Anwendung beendet wird, fahren Sie die Medienquelle und das Playerobjekt wie folgt herunter:

1.  Rufen Sie ÜBER DIE MEDIENQUELLE [**DEN AUFRUF VONMEDIASOURCE::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) auf.
2.  Rufen Sie [**IMFPMediaPlayer::Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) für das Playerobjekt auf.


```C++
    if (g_pSource)
    {
        g_pSource->Shutdown();
        g_pSource->Release();
        g_pSource = NULL;
    }

    if (g_pPlayer)
    {
        g_pPlayer->Shutdown();
        g_pPlayer->Release();
        g_pPlayer = NULL;
    }
```



## <a name="requirements"></a>Anforderungen

MFPlay erfordert Windows 7.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MFPlay](using-mfplay-for-audio-video-playback.md)
</dt> <dt>

[Videoaufnahme](audio-video-capture.md)
</dt> </dl>

 

 



