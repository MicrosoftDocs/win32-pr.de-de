---
description: In diesem Thema wird beschrieben, wie Sie mfplay verwenden, um ein Video von einer Videokamera aus anzuzeigen.
ms.assetid: ecf6113f-1d8e-4680-87ab-bfd45a9663e4
title: Video Vorschau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d458568a18f598e5aa4ee7e8fb21059e503362
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359932"
---
# <a name="video-preview"></a>Video Vorschau

\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

In diesem Thema wird beschrieben, wie Sie mfplay verwenden, um ein Video von einer Videokamera aus anzuzeigen.

Mfplay bietet die einfachste Möglichkeit, das Video von einem Erfassungsgerät aus Microsoft Media Foundation in der Vorschau anzuzeigen. Sie sollten MF Play verwenden, wenn die folgenden Bedingungen erfüllt sind:

-   Sie müssen das Video nicht in einer Datei erfassen.
-   Sie benötigen keine fein abgestimmte Kontrolle darüber, wie das Video gerendert wird. (Sie müssen z. b. die Erstellung des Direct3D-Geräts nicht steuern.)
-   Vor dem Rendern müssen die Videodaten nicht von der Kamera verarbeitet werden.

Andernfalls ist der [Quell Leser](source-reader.md) möglicherweise eine bessere Option.

Um mfplay mit einem Video Erfassungsgerät zu verwenden, führen Sie die folgenden Schritte aus:

1.  Erstellen Sie eine Medienquelle für das Erfassungsgerät. Weitere Informationen finden Sie unter Auflisten von [Video Erfassungs Geräten](enumerating-video-capture-devices.md).
2.  Rufen Sie [**mfpkreatemediaplayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) auf, um eine Instanz des Player-Objekts zu erstellen.
3.  Aufrufen der [**imfpmediaplayer:: foratemediaitemfromubject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) -Methode. Übergeben Sie einen Zeiger auf die imfmediasource-Schnittstelle der Medienquelle. Die-Methode empfängt einen Zeiger auf die [**imfpmediaitem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) -Schnittstelle.
4.  Aufrufen von [**imfpmediaplayer:: setmediaitem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem).
5.  [**Imfpmediaplayer aufrufen::P Lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) , um die Vorschau anzuzeigen.

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



In einer typischen Anwendung würden Sie einen Zeiger auf eine Rückruf Schnittstelle in der [**mfpkreatemediaplayer**](/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer) -Funktion bereitstellen und die Rückruf Schnittstelle verwenden, um Ereignisse vom Player zu erhalten. Der Einfachheit halber überspringt der hier gezeigte Code diese Schritte. Weitere Informationen finden Sie unter [Getting Started with MF](getting-started-with-mfplay.md).

### <a name="shutting-down"></a>Wird heruntergefahren

Bevor die Anwendung beendet wird, fahren Sie die Medienquelle und das Player-Objekt wie folgt herunter:

1.  Nennen Sie [**imfmediasource:: Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-shutdown) für die Medienquelle.
2.  Nennen Sie [**imfpmediaplayer:: Shutdown**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown) für das Player-Objekt.


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

MF Play erfordert Windows 7.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[MF Play](using-mfplay-for-audio-video-playback.md)
</dt> <dt>

[Video Erfassung](audio-video-capture.md)
</dt> </dl>

 

 



