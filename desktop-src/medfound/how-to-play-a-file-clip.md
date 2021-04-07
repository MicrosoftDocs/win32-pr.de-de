---
description: In diesem Thema wird beschrieben, wie Sie ein Segment einer Mediendatei in mfplay abspielen, indem Sie die Start-und Endzeit für die Wiedergabe festlegen.
ms.assetid: cd761a4a-42ad-4994-b1b8-0946d29c3d8b
title: Wiedergeben eines Datei Clips
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 744db96c6dc384f2473f6c6d3361b24950a8881d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863291"
---
# <a name="how-to-play-a-file-clip"></a>Wiedergeben eines Datei Clips

\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

In diesem Thema wird beschrieben, wie Sie ein Segment einer Mediendatei in mfplay abspielen, indem Sie die Start-und Endzeit für die Wiedergabe festlegen.

**So spielen Sie einen dateiclip wieder**

1.  Rufen Sie [**imfpmediaplayer:: foratemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) oder [**imfpmediaplayer:: foratemediaitemfromubject**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject) auf, um ein Medien Element für die Datei zu erstellen.
2.  Optional können Sie die gesamte Dauer der Datei erhalten, wie unter [How to Get the Wiedergabe Duration](how-to-get-the-playback-duration.md)beschrieben.
3.  Aufrufen von [**imfpmediaitem:: setstartstopposition**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition) zum Festlegen der Start-und Endzeiten. Die Endzeit darf die Datei Dauer nicht überschreiten.
4.  Aufrufen von [**imfpmediaplayer:: setmediaitem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) zum Starten der Wiedergabe.

Im folgenden Beispiel wird die blockierende Version von " [**kreatemediaitemfromurl**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl)" verwendet. Wenn die nicht blockierende Version verwendet wird, sollte der Code, der nach dem Erstellen von " **kreatemediaitemfromurl** " angezeigt wird, im Handler für das Ereignis " **\_ \_ \_ mediaitem \_** -Ereignis" des MFP-Ereignis Typs eingefügt werden. Weitere Informationen zu Ereignissen in MF Play finden Sie unter [empfangen von Ereignissen vom Player](getting-started-with-mfplay.md).

Um die Datei Dauer zu erhalten, wird in diesem Beispiel die-Funktion aufgerufen, die `GetPlaybackDuration` im Thema Gewusst [wie: erhalten der Wiedergabedauer](how-to-get-the-playback-duration.md)angezeigt wird.


```C++
HRESULT PlayMediaClip(
    IMFPMediaPlayer *pPlayer,
    PCWSTR pszURL,
    LONGLONG    hnsStart,
    LONGLONG    hnsEnd
    )
{
    IMFPMediaItem *pItem = NULL;
    PROPVARIANT varStart, varEnd;

    ULONGLONG hnsDuration = 0;

    HRESULT hr = pPlayer->CreateMediaItemFromURL(pszURL, TRUE, 0, &pItem);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = GetPlaybackDuration(pItem, &hnsDuration);
    if (FAILED(hr))
    {
        goto done;
    }

    if ((ULONGLONG)hnsEnd > hnsDuration)
    {
        hnsEnd = hnsDuration;
    }

    hr = InitPropVariantFromInt64(hnsStart, &varStart);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = InitPropVariantFromInt64(hnsEnd, &varEnd);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pItem->SetStartStopPosition(
        &MFP_POSITIONTYPE_100NS,
        &varStart,
        &MFP_POSITIONTYPE_100NS,
        &varEnd
        );
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pPlayer->SetMediaItem(pItem);

done:
    SafeRelease(&pItem);
    return hr;
}
```



## <a name="requirements"></a>Anforderungen

MF Play erfordert Windows 7.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



