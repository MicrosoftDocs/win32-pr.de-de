---
description: So ermitteln Sie die Dauer einer Mediendatei
ms.assetid: 88ecde0c-328f-4ca7-9d26-836e4df06563
title: So finden Sie die Dauer einer Mediendatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8915e52e97a4532b1d174166ec2863e26d18e34a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104530503"
---
# <a name="how-to-find-the-duration-of-a-media-file"></a>So finden Sie die Dauer einer Mediendatei

Führen Sie die folgenden Schritte aus, um die Dauer einer Mediendatei zu ermitteln:

1.  Verwenden Sie den [quellresolver](source-resolver.md) , um eine Medienquelle zu erstellen, mit der die Mediendatei analysiert werden kann.
2.  Aufrufen von [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) für die Medienquelle. Diese Methode gibt einen Präsentations Deskriptor zurück, der den Inhalt der Mediendatei beschreibt.
3.  Fragen Sie den Präsentations Deskriptor für das [MF \_ PD \_ Duration](mf-pd-duration-attribute.md) -Attribut ab, indem Sie die [**imfattributes:: GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64) -Methode aufrufen. Der Wert des-Attributs, falls vorhanden, ist die Datei Dauer in 100-Nanosecond-Einheiten.


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

 

 



