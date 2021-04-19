---
description: Ein Video Erfassungsgerät unterstützt möglicherweise einen Bereich von Frameraten.
ms.assetid: 9578e60d-0339-4382-b798-2d31d2ddbe76
title: Festlegen der Frame Rate für die Video Erfassung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44e105965f5449cb7f4cab59f49410ecfb40221c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348250"
---
# <a name="how-to-set-the-video-capture-frame-rate"></a>Festlegen der Frame Rate für die Video Erfassung

Ein Video Erfassungsgerät unterstützt möglicherweise einen Bereich von Frameraten. Wenn diese Informationen verfügbar sind, werden die minimalen und maximalen Frameraten als Medientyp Attribute gespeichert:



| Attribut                                                         | BESCHREIBUNG         |
|-------------------------------------------------------------------|---------------------|
| [maximal zulässige Anzahl von MF- \_ MT- \_ Frame \_ Raten \_ \_](mf-mt-frame-rate-range-max.md) | Maximale Framerate. |
| [Bereich für die Anzahl von MF \_ MT- \_ Frame \_ Raten \_ \_](mf-mt-frame-rate-range-min.md) | Minimale Framerate. |



 

Der Bereich kann je nach Erfassungs Format variieren. Beispielsweise kann bei größeren Frame Größen die maximale Framerate reduziert werden.

So legen Sie die Framerate fest:

1.  Erstellen Sie die Medienquelle für das Erfassungsgerät. Weitere Informationen finden Sie unter Auflisten von [Video Erfassungs Geräten](enumerating-video-capture-devices.md).
2.  Aufrufen von [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) für die Medienquelle zum Abrufen des Präsentations Deskriptors.
3.  Aufrufen von [**imfpresentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) zum Abrufen des streamdeskriptors für den Videostream.
4.  Aufrufen von [**imfstreamdescriptor:: getmediatypeer Handler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) für den Datenstrom Deskriptor.
5.  Auflisten der Erfassungs Formate, wie unter Gewusst [wie: Festlegen des Video Erfassungs Formats](how-to-set-the-video-capture-format.md)beschrieben.
6.  Wählen Sie das gewünschte Ausgabeformat aus der Liste aus.
7.  Fragen Sie den Medientyp für den Bereich " [MF \_ MT \_ Frame \_ Rate \_ Range \_ Max](mf-mt-frame-rate-range-max.md) " und " [MF \_ MT \_ Frame \_ Rate \_ Range \_ Min](mf-mt-frame-rate-range-min.md) Attribute" ab. Diese Werte gibt den Bereich der unterstützten Frameraten an. Das Gerät unterstützt möglicherweise andere Frameraten innerhalb dieses Bereichs.
8.  Legen Sie das [**MF \_ MT- \_ Frame**](mf-mt-frame-rate-attribute.md) -Attribut für den Medientyp fest, um die gewünschte Frame Rate anzugeben.
9.  Aufrufen von [**imfmediatyphandler:: setcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) mit dem geänderten Medientyp.

Im folgenden Beispiel wird die Framerate auf die maximale Framerate festgelegt, die vom Gerät unterstützt wird:


```C++
HRESULT SetMaxFrameRate(IMFMediaSource *pSource, DWORD dwTypeIndex)
{
    IMFPresentationDescriptor *pPD = NULL;
    IMFStreamDescriptor *pSD = NULL;
    IMFMediaTypeHandler *pHandler = NULL;
    IMFMediaType *pType = NULL;

    HRESULT hr = pSource->CreatePresentationDescriptor(&pPD);
    if (FAILED(hr))
    {
        goto done;
    }

    BOOL fSelected;
    hr = pPD->GetStreamDescriptorByIndex(dwTypeIndex, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetCurrentMediaType(&pType);
    if (FAILED(hr))
    {
        goto done;
    }

    // Get the maximum frame rate for the selected capture format.

    // Note: To get the minimum frame rate, use the 
    // MF_MT_FRAME_RATE_RANGE_MIN attribute instead.

    PROPVARIANT var;
    if (SUCCEEDED(pType->GetItem(MF_MT_FRAME_RATE_RANGE_MAX, &var)))
    {
        hr = pType->SetItem(MF_MT_FRAME_RATE, var);

        PropVariantClear(&var);

        if (FAILED(hr))
        {
            goto done;
        }

        hr = pHandler->SetCurrentMediaType(pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> </dl>

 

 



