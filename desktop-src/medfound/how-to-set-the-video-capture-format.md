---
description: Ein Video Erfassungsgerät kann mehrere Erfassungs Formate unterstützen. Formate unterscheiden sich in der Regel durch Komprimierungstyp, Farbraum (YUV oder RGB), Frame Größe oder Framerate.
ms.assetid: 479abaea-f310-4139-9967-f24b03c34558
title: Festlegen des Video Erfassungs Formats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c27cb9c20cbf989ab5db3564733dc96860c7bcb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368260"
---
# <a name="how-to-set-the-video-capture-format"></a>Festlegen des Video Erfassungs Formats

Ein Video Erfassungsgerät kann mehrere Erfassungs Formate unterstützen. Formate unterscheiden sich in der Regel durch Komprimierungstyp, Farbraum (YUV oder RGB), Frame Größe oder Framerate.

Die Liste der unterstützten Formate ist im *Präsentations Deskriptor* enthalten. Weitere Informationen finden Sie unter [Präsentations Deskriptoren](presentation-descriptors.md).

So zählen Sie die unterstützten Formate auf:

1.  Erstellen Sie die Medienquelle für das Erfassungsgerät. Weitere Informationen finden Sie unter Auflisten von [Video Erfassungs Geräten](enumerating-video-capture-devices.md).
2.  Aufrufen von [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) für die Medienquelle zum Abrufen des Präsentations Deskriptors.
3.  Aufrufen von [**imfpresentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) zum Abrufen des streamdeskriptors für den Videostream.
4.  Aufrufen von [**imfstreamdescriptor:: getmediatypeer Handler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) für den Datenstrom Deskriptor.
5.  Aufrufen von [**imfmediatyethandler:: getmediatyetcount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) , um die Anzahl unterstützter Formate zu erhalten.
6.  Aufrufen Sie in einer-Schleife [**imfmediatyphandler:: getmediatypeer byindex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) , um jedes Format abzurufen. Das Format wird durch einen *Medientyp* dargestellt. Weitere Informationen finden Sie unter [Video Medientypen](video-media-types.md).

Im folgenden Beispiel werden die Erfassungs Formate für ein Gerät aufgelistet:


```C++
HRESULT EnumerateCaptureFormats(IMFMediaSource *pSource)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    DWORD cTypes = 0;
    hr = pHandler->GetMediaTypeCount(&cTypes);
    if (FAILED(hr))
    {
        goto done;
    }

    for (DWORD i = 0; i < cTypes; i++)
    {
        hr = pHandler->GetMediaTypeByIndex(i, &pType);
        if (FAILED(hr))
        {
            goto done;
        }

        LogMediaType(pType);
        OutputDebugString(L"\n");

        SafeRelease(&pType);
    }

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



Die `LogMediaType` in diesem Beispiel verwendete Funktion ist im Thema [Medientyp Debuggen von Code](media-type-debugging-code.md)aufgeführt.

So legen Sie das Erfassungs Format fest:

1.  Einen Zeiger auf die [**imfmediatypeer Handler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) -Schnittstelle erhalten, wie im vorherigen Beispiel gezeigt.
2.  Aufrufen von [**imfmediatypeer Handler:: getmediatypeer byindex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) zum Abrufen des gewünschten Formats, angegeben durch Index.
3.  Verwenden Sie [**imfmediatyphandler:: setcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) , um das Format festzulegen.

Wenn Sie das Erfassungs Format nicht festlegen, wird das Standardformat des Geräts verwendet.

Im folgenden Beispiel wird das Erfassungs Format festgelegt:


```C++
HRESULT SetDeviceFormat(IMFMediaSource *pSource, DWORD dwFormatIndex)
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
    hr = pPD->GetStreamDescriptorByIndex(0, &fSelected, &pSD);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pSD->GetMediaTypeHandler(&pHandler);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->GetMediaTypeByIndex(dwFormatIndex, &pType);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pHandler->SetCurrentMediaType(pType);

done:
    SafeRelease(&pPD);
    SafeRelease(&pSD);
    SafeRelease(&pHandler);
    SafeRelease(&pType);
    return hr;
}
```



Die Reihenfolge, in der Formate zurückgegeben werden, hängt vom Gerät ab. In der Regel werden Sie zuerst nach Komprimierungstyp oder Farbraum gruppiert. und dann von der kleinsten Frame Größe zur größten Frame Größe innerhalb der einzelnen Gruppen.

Die Framerate werden etwas anders behandelt als die anderen Format Attribute. Weitere Informationen finden Sie unter Vorgehens [Weise beim Festlegen der Frame Rate der Video Aufzeichnung](how-to-set-the-video-capture-frame-rate.md).

> [!Note]  
> In einigen Geräten enthält die Format Liste einen doppelten Eintrag für jedes Format. Wenn das Gerät z. b. 15 unterschiedliche Erfassungs Formate unterstützt, enthält die Liste 30 Einträge. In jedem Paar wird für einen der Medientypen das Attribut [**MF \_ MT \_ am \_ \_ formatType**](mf-mt-am-format-type-attribute.md) gleich **Format \_ videoinfo** und für das andere der **MF \_ MT \_ am- \_ \_ Formattyp** gleich **Format \_ VideoInfo2** angezeigt. (Diese beiden Werte sind in der Header Datei UUIDs. h definiert.) Der zweite Typ enthält möglicherweise auch zusätzliche Farbinformationen ([Erweiterte Farbinformationen](extended-color-information.md)) oder einen anderen Wert für das Zeilen Sprung ([**MF MT- \_ \_ Interlace- \_ Modus**](mf-mt-interlace-mode-attribute.md)). Diese doppelten Typen sind vorhanden, um ältere DirectShow-Anwendungen zu unterstützen. In einer Media Foundation Anwendung sollten Sie den Typ " **\_ videoinfo** " im Format ignorieren, wenn ein doppelter **Format \_ VideoInfo2** Type aufgeführt ist.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Video Erfassung](video-capture.md)
</dt> </dl>

 

 



