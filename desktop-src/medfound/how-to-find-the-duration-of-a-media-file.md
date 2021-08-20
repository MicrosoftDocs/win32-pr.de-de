---
description: Ermitteln der Dauer einer Mediendatei
ms.assetid: 88ecde0c-328f-4ca7-9d26-836e4df06563
title: Suchen der Dauer einer Mediendatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1885d356be54875079341eabc7433c9753792daf01c4848a00ee4ed4fbb343ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117878844"
---
# <a name="how-to-find-the-duration-of-a-media-file"></a>Suchen der Dauer einer Mediendatei

Führen Sie die folgenden Schritte aus, um die Dauer einer Mediendatei zu ermitteln:

1.  Verwenden Sie den [Quell-Resolver,](source-resolver.md) um eine Medienquelle zu erstellen, die die Mediendatei analysieren kann.
2.  Rufen Sie [**ÜBER DIE MEDIENQUELLE::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) auf. Diese Methode gibt den Präsentationsdeskriptor zurück, der den Inhalt der Mediendatei beschreibt.
3.  Fragen Sie den Präsentationsdeskriptor für das [MF \_ PD \_ DURATION-Attribut](mf-pd-duration-attribute.md) ab, indem Sie die [**ATTRIBUTEAttributes::GetUINT64-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) aufrufen. Der Wert des Attributs ist , falls vorhanden, die Dateidauer in Einheiten von 100 Nanosekunden.


```C++
HRESULT GetSourceDuration(IMFMediaSource *pSource, MFTIME *pDuration)
{
    *pDuration = 0;

    IMFPresentationDescriptor *pPD = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_DURATION, (UINT64*)pDuration);
        pPD->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audio-/Videowiedergabe](audio-video-playback.md)
</dt> </dl>

 

 



