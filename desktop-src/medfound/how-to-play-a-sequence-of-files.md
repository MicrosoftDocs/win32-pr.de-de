---
description: In diesem Thema wird beschrieben, wie Eine Sequenz von Audio-/Videodateien mithilfe von MFPlay wiedergegeben wird.
ms.assetid: ee16eaa3-0506-4444-b139-f8a8498d6597
title: Wiederspielen einer Sequenz von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ddf9cfc6fe48caf5eb185a19ec98ac119fcfbbb78d5e2363bd2db9607a4875
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828160"
---
# <a name="how-to-play-a-sequence-of-files"></a>Wiederspielen einer Sequenz von Dateien

\[MFPlay steht für die Verwendung in den Betriebssystemen zur Verfügung, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

In diesem Thema wird beschrieben, wie Eine Sequenz von Audio-/Videodateien mithilfe von MFPlay wiedergegeben wird.


Das Thema [Erste Schritte mit MFPlay](getting-started-with-mfplay.md) zeigt, wie eine einzelne Mediendatei wiedergegeben wird. Sie können MFPlay auch verwenden, um eine Sequenz von Dateien wiederzuspielen.

### <a name="synchronous-blocking-method"></a>Synchrone (blockierende) Methode

1.  Rufen Sie [**die IMFPMediaPlayer::CreateMediaItemFromURL-Methode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) auf. Die -Methode erstellt ein Medienelement.
2.  Rufen [**Sie IMFPMediaPlayer::SetMediaItem auf,**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) um das Medienelement für die Wiedergabe in die Warteschlange zu stellen.
3.  Rufen [**Sie IMFPMediaPlayer::P lay auf,**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) um die Wiedergabe zu starten.

Diese Schritte werden im folgenden Code gezeigt.


```C++
HRESULT OpenMediaFile(IMFPMediaPlayer *pPlayer, PCWSTR pwszURL)
{
    HRESULT hr = S_OK;
    
    IMFPMediaItem *pItem = NULL;

    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        TRUE,  // Blocking call
        0,     // User data.
        &pItem
        );

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pPlayer->Play();
    }

    if (pItem)
    {
        pItem->Release();
    }
    return hr;
}
```



Die [**CreateMediaItemFromURL-Methode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) verwendet die folgenden Parameter:

-   Der erste Parameter ist die URL der Datei.
-   Der zweite Parameter gibt an, ob die Methode blockiert. Wenn Sie den Wert **TRUE** angeben, wie hier gezeigt, wird die -Methode blockiert, bis das Medienelement erstellt wird.
-   Der dritte Parameter ordnet dem Medienelement einen beliebigen **\_ DWORD-PTR-Wert** zu. Sie können diesen Wert später durch Aufrufen von [**IMFPMediaItem::GetUserData erhalten.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata)
-   Der vierte Parameter empfängt einen Zeiger auf die [**IMFPMediaItem-Schnittstelle**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) des Medienelements.

### <a name="asynchronous-non-blocking-method"></a>Asynchrone (nicht blockierende) Methode

Vermeiden Sie die Blockierungsoption, wenn Sie [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) über Ihren UI-Thread aufrufen, da dies eine spürbare Zeit dauern kann. Die -Methode öffnet in der Regel eine Datei- oder Netzwerkverbindung und liest genügend Daten, um die Dateiheader zu analysieren. Dies kann einige Zeit dauern. Daher ist es im Allgemeinen besser, den zweiten Parameter auf **FALSE zu setzen.** Diese Option bewirkt, dass die -Methode asynchron ausgeführt wird. Wenn die asynchrone Option verwendet wird, muss der letzte Parameter **NULL sein:**


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



Wenn das Medienelement erstellt wird, empfängt Ihre Anwendung ein **MFP \_ EVENT TYPE \_ \_ MEDIAITEM \_ CREATED-Ereignis.** Die Datenstruktur für dieses Ereignis enthält einen Zeiger auf das Medienelement. Übergeben Sie diesen Zeiger auf die [**SetMediaItem-Methode,**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) um das Element für die Wiedergabe in die Warteschlange zu stellen.


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    HRESULT hr = S_OK;
    if (FAILED(pEvent->header.hrEvent))
    {
        // Handle error. (Not shown.)
    }
    else
    {
        hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
    }
}
```



## <a name="requirements"></a>Anforderungen

MFPlay erfordert Windows 7.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MFPlay für die Audio-/Videowiedergabe](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



