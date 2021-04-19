---
description: In diesem Thema wird beschrieben, wie eine Sequenz von Audiodateien/Videodateien mit mfplay wiedergegeben wird.
ms.assetid: ee16eaa3-0506-4444-b139-f8a8498d6597
title: Wiedergabe einer Sequenz von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dc4d1523be4cc6cc09416096af260c9eae736c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348331"
---
# <a name="how-to-play-a-sequence-of-files"></a>Wiedergabe einer Sequenz von Dateien

\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

In diesem Thema wird beschrieben, wie eine Sequenz von Audiodateien/Videodateien mit mfplay wiedergegeben wird.


Das Thema " [Getting Started with mfplay](getting-started-with-mfplay.md) " zeigt, wie Sie eine einzelne Mediendatei abspielen können. Sie können auch mfplay verwenden, um eine Sequenz von Dateien wiederzugeben.

### <a name="synchronous-blocking-method"></a>Synchrone (blockierende) Methode

1.  Aufrufen der [**imfpmediaplayer:: foratemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) -Methode. Mit der-Methode wird ein Medien Element erstellt.
2.  [**Imfpmediaplayer:: setmediaitem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) aufrufen, um das Medien Element für die Wiedergabe in die Warteschlange zu stellen.
3.  [**Imfpmediaplayer aufzurufen::P Lay**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) , um die Wiedergabe zu starten.

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



Die Methode " [**kreatemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) " übernimmt die folgenden Parameter:

-   Der erste Parameter ist die URL der Datei.
-   Der zweite Parameter gibt an, ob die-Methode blockiert. Das Angeben des Werts **true**, wie hier gezeigt, bewirkt, dass die-Methode blockiert wird, bis das Medien Element erstellt wird.
-   Der dritte Parameter ordnet dem Medien Element einen beliebigen **DWORD- \_ ptr** -Wert zu. Sie können diesen Wert später abrufen, indem Sie [**imfpmediaitem:: getuserdata**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata)aufrufen.
-   Der vierte Parameter erhält einen Zeiger auf die [**imfpmediaitem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) -Schnittstelle des Medien Elements.

### <a name="asynchronous-non-blocking-method"></a>Asynchrone (nicht blockierende) Methode

Vermeiden Sie die Blockierungs Option, wenn Sie " [**foratemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) " aus dem UI-Thread aufrufen, da es eine spürbare Zeit für den Abschluss des Vorgangs dauern kann. Die-Methode öffnet in der Regel eine Datei-oder Netzwerkverbindung und liest genügend Daten, um die Dateiheader zu analysieren, die alle eine Weile dauern können. Daher ist es in der Regel besser, den zweiten Parameter auf **false** festzulegen. Diese Option bewirkt, dass die-Methode asynchron ausführt. Wenn die asynchrone Option verwendet wird, muss der letzte Parameter **null** sein:


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



Wenn das Medien Element erstellt wird, empfängt Ihre Anwendung einen Ereignis **vom Typ "MFP- \_ \_ Ereignistyp \_ mediaitem \_ erstellt** ". Die Datenstruktur für dieses Ereignis enthält einen Zeiger auf das Medien Element. Übergeben Sie diesen Zeiger an die [**setmediaitem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) -Methode, um das Element in die Warteschlange zu stellen.


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

MF Play erfordert Windows 7.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



