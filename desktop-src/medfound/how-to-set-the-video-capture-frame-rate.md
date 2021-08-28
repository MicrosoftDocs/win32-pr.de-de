---
description: Ein Videoaufnahmegerät unterstützt möglicherweise eine Reihe von Bildfrequenzen.
ms.assetid: 9578e60d-0339-4382-b798-2d31d2ddbe76
title: Festlegen der Videoaufnahme-Bildfrequenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b0e80c26c5a53a89cbc87ca509f25db1ebccf4571b4dda2e83ea63717c7d91a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827970"
---
# <a name="how-to-set-the-video-capture-frame-rate"></a>Festlegen der Videoaufnahme-Bildfrequenz

Ein Videoaufnahmegerät unterstützt möglicherweise eine Reihe von Bildfrequenzen. Wenn diese Informationen verfügbar sind, werden die minimalen und maximalen Bildraten als Medientypattribute gespeichert:



| attribute                                                         | Beschreibung         |
|-------------------------------------------------------------------|---------------------|
| [MF \_ MT \_ FRAME \_ RATE \_ RANGE \_ MAX](mf-mt-frame-rate-range-max.md) | Maximale Bildfrequenz. |
| [MF \_ MT \_ FRAME \_ RATE \_ RANGE \_ MIN](mf-mt-frame-rate-range-min.md) | Minimale Bildfrequenz. |



 

Der Bereich kann je nach Erfassungsformat variieren. Bei größeren Rahmengrößen kann beispielsweise die maximale Bildfrequenz reduziert werden.

So legen Sie die Bildfrequenz fest:

1.  Erstellen Sie die Medienquelle für das Erfassungsgerät. Weitere Informationen finden Sie unter [Enumerating Video Capture Devices (Aufzählen von Videoaufnahmegeräten).](enumerating-video-capture-devices.md)
2.  Rufen Sie [**ÜBER DIE MEDIENQUELLE::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) für die Medienquelle auf, um den Präsentationsdeskriptor abzurufen.
3.  Rufen Sie [**DIE DATEI PRESENTPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) auf, um den Streamdeskriptor für den Videostream abzurufen.
4.  Rufen Sie IM STREAM-Deskriptor [**DIESSTREAMDESCRIPTOR::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) auf.
5.  Aufzählen der Aufzeichnungsformate, wie unter [Festlegen des Videoaufnahmeformats](how-to-set-the-video-capture-format.md)beschrieben.
6.  Wählen Sie das gewünschte Ausgabeformat aus der Liste aus.
7.  Fragen Sie den Medientyp nach den Attributen [MF MT FRAME RATE RANGE \_ \_ \_ \_ \_ MAX](mf-mt-frame-rate-range-max.md) und [MF MT FRAME RATE RANGE \_ \_ \_ \_ \_ MIN](mf-mt-frame-rate-range-min.md) ab. Diese Werte geben den Bereich der unterstützten Frameraten an. Das Gerät unterstützt möglicherweise andere Bildfrequenzen innerhalb dieses Bereichs.
8.  Legen Sie das [**MF \_ MT \_ FRAME-Attribut**](mf-mt-frame-rate-attribute.md) für den Medientyp fest, um die gewünschte Bildfrequenz anzugeben.
9.  Rufen Sie [**ÜBERMEDIATypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) den geänderten Medientyp auf.

Im folgenden Beispiel wird die Bildfrequenz auf die maximale Bildfrequenz festgelegt, die das Gerät unterstützt:


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

[Videoaufnahme](video-capture.md)
</dt> </dl>

 

 



