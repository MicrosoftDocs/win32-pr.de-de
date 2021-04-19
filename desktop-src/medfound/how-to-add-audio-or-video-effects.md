---
description: In diesem Thema wird beschrieben, wie Sie Audio-/Videoeffekte mit mfplay verwenden.
ms.assetid: 90f34bf3-899f-46e0-80c8-af83caa4835d
title: Hinzufügen von Audio-oder Video Effekten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8d2b02453ce4561ead7fee0d272a07e694e8388
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349795"
---
# <a name="how-to-add-audio-or-video-effects"></a>Hinzufügen von Audio-oder Video Effekten

\[MF Play ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. \]

In diesem Thema wird beschrieben, wie Sie Audio-/Videoeffekte mit mfplay verwenden.

Um einen Effekt mit mfplay zu verwenden, muss der Effekt als Media Foundation Transformation (MFT) implementiert werden. Weitere Informationen finden Sie unter [Media Foundation Transformationen](media-foundation-transforms.md).

**So fügen Sie einen Audio-oder Video Effekt hinzu**

1.  Erstellen Sie eine Instanz des MFT, die den Effekt implementiert.
2.  [**Imfpmediaplayer:: inserteffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect)aufzurufen.

Geben Sie [**inserteffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) ein, bevor Sie die Mediendatei für die Wiedergabe öffnen. MF Play bestimmt automatisch, ob der Effekt ein Videoeffekt oder ein Audioeffekt ist.

Die [**inserteffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect) -Methode nimmt auch einen booleschen Parameter an, der angibt, ob der Effekt optional oder erforderlich ist. Wenn MF Play keinen erforderlichen Effekt hinzufügen kann (z. b. weil das Streamformat nicht kompatibel ist), tritt ein Wiedergabe Fehler auf. In den meisten Fällen ist es besser, einen Effekt als optional festzulegen.

Mfplay verwendet weiterhin den Effekt für alle nachfolgenden Wiedergabe. Um den Effekt zu entfernen, wenden Sie [**imfpmediaplayer:: removeeffect**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect) oder [**imfpmediaplayer:: removealleffects**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects)an.


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

MF Play erfordert Windows 7.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von MF Play für die Audiowiedergabe und Video Wiedergabe](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



