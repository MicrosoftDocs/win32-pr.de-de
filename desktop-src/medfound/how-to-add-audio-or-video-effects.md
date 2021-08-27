---
description: In diesem Thema wird beschrieben, wie Audio-/Videoeffekte mit MFPlay verwendet werden.
ms.assetid: 90f34bf3-899f-46e0-80c8-af83caa4835d
title: Hinzufügen von Audio- oder Videoeffekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2af2bb310ab4818cac5dd2804d2bb696c284fdd868d916e4e543a205328e909e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061550"
---
# <a name="how-to-add-audio-or-video-effects"></a>Hinzufügen von Audio- oder Videoeffekten

\[MFPlay ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

In diesem Thema wird beschrieben, wie Audio-/Videoeffekte mit MFPlay verwendet werden.

Um einen Effekt mit MFPlay zu verwenden, muss der Effekt als Media Foundation Transform (MFT) implementiert werden. Weitere Informationen finden Sie unter [Media Foundation Transformationen.](media-foundation-transforms.md)

**So fügen Sie einen Audio- oder Videoeffekt hinzu**

1.  Erstellen Sie eine Instanz des MFT, die den Effekt implementiert.
2.  Rufen Sie [**IMFPMediaPlayer::InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect)auf.

Rufen Sie [**InsertEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) auf, bevor Sie die Mediendatei für die Wiedergabe öffnen. MFPlay bestimmt automatisch, ob der Effekt ein Videoeffekt oder ein Audioeffekt ist.

Die [**InsertEffect-Methode**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) verwendet auch einen booleschen Parameter, der angibt, ob der Effekt optional oder erforderlich ist. Wenn MFPlay keinen erforderlichen Effekt hinzufügen kann (z. B. weil das Streamformat nicht kompatibel ist), tritt ein Wiedergabefehler auf. In den meisten Fällen ist es besser, einen Effekt als optional festzulegen.

MFPlay verwendet weiterhin den Effekt für alle nachfolgenden Wiedergaben. Um den Effekt zu entfernen, rufen [**Sie IMFPMediaPlayer::RemoveEffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) oder [**IMFPMediaPlayer::RemoveAllEffects auf.**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects)


```C++
HRESULT AddPlaybackEffect(REFGUID clsid, IMFPMediaPlayer *pPlayer)
{
    IMFTransform *pMFT = NULL;

    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pMFT));

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->InsertEffect(pMFT, TRUE); // Set as optional.
    }

    SafeRelease(&pMFT);
    return hr;
}
```



## <a name="requirements"></a>Anforderungen

MFPlay erfordert Windows 7.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MFPlay für die Audio-/Videowiedergabe](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



