---
description: Ein Videoaufnahmegerät unterstützt möglicherweise mehrere Aufzeichnungsformate. Formate unterscheiden sich in der Regel nach Komprimierungstyp, Farbraum (YUV oder RGB), Framegröße oder Bildfrequenz.
ms.assetid: 479abaea-f310-4139-9967-f24b03c34558
title: Festlegen des Videoaufnahmeformats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0968560772345bea91f5acfb79e7157a6376f388a5c0065634a273196b7552cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974399"
---
# <a name="how-to-set-the-video-capture-format"></a>Festlegen des Videoaufnahmeformats

Ein Videoaufnahmegerät unterstützt möglicherweise mehrere Aufzeichnungsformate. Formate unterscheiden sich in der Regel nach Komprimierungstyp, Farbraum (YUV oder RGB), Framegröße oder Bildfrequenz.

Die Liste der unterstützten Formate ist im *Präsentationsdeskriptor* enthalten. Weitere Informationen finden Sie unter [Präsentationsdeskriptoren.](presentation-descriptors.md)

So enumerieren Sie die unterstützten Formate:

1.  Erstellen Sie die Medienquelle für das Erfassungsgerät. Weitere Informationen finden Sie unter [Enumerating Video Capture Devices (Aufzählen von Videoaufnahmegeräten).](enumerating-video-capture-devices.md)
2.  Rufen Sie [**ÜBER DIE MEDIENQUELLE::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) für die Medienquelle auf, um den Präsentationsdeskriptor abzurufen.
3.  Rufen Sie [**DIE DATEI PRESENTPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) auf, um den Streamdeskriptor für den Videostream abzurufen.
4.  Rufen Sie IM STREAM-Deskriptor [**DIESSTREAMDESCRIPTOR::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) auf.
5.  Rufen Sie [**DENMEDIATypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) auf, um die Anzahl der unterstützten Formate abzurufen.
6.  Rufen Sie in einer Schleife [**DEN SCHLEIFEMEDIATypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) auf, um jedes Format abzurufen. Das Format wird durch einen *Medientyp* dargestellt. Weitere Informationen finden Sie unter [Videomedientypen.](video-media-types.md)

Im folgenden Beispiel werden die Erfassungsformate für ein Gerät aufzählt:


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



Die `LogMediaType` in diesem Beispiel verwendete Funktion ist im Thema [Medientypdebuggingcode](media-type-debugging-code.md)aufgeführt.

So legen Sie das Erfassungsformat fest:

1.  Abrufen eines Zeigers auf die [**INTERFACESMediaTypeHandler-Schnittstelle,**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) wie im vorherigen Beispiel gezeigt.
2.  Rufen Sie DAS GEWÜNSCHTE Format auf, das vom Index angegeben wird, indem [**Sie DENMEDIATypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) aufrufen.
3.  Rufen Sie DAS FORMAT [**AUFMEDIATypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) auf.

Wenn Sie das Erfassungsformat nicht festlegen, verwendet das Gerät das Standardformat.

Im folgenden Beispiel wird das Erfassungsformat festgelegt:


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



Die Reihenfolge, in der Formate zurückgegeben werden, hängt vom Gerät ab. In der Regel werden sie zuerst nach Komprimierungstyp oder Farbraum gruppiert. und dann von der kleinsten Framegröße zur größten Framegröße innerhalb jeder Gruppe.

Die Bildfrequenz wird etwas anders behandelt als die anderen Formatattribute. Weitere Informationen finden Sie unter [Festlegen der Videoaufnahme-Framerate.](how-to-set-the-video-capture-frame-rate.md)

> [!Note]  
> Auf einigen Geräten enthält die Formatliste einen doppelten Eintrag für jedes Format. Wenn das Gerät beispielsweise 15 verschiedene Erfassungsformate unterstützt, enthält die Liste 30 Einträge. Innerhalb jedes Paars hat einer der Medientypen das Attribut [**MF MT AM FORMAT \_ \_ \_ \_ TYPE**](mf-mt-am-format-type-attribute.md) gleich **FORMAT \_ VideoInfo** und der andere hat **MF MT AM FORMAT \_ \_ \_ \_ TYPE** gleich **FORMAT \_ VideoInfo2**. (Diese beiden Werte werden in der Headerdatei uuids.h definiert.) Der zweite Typ kann auch zusätzliche Farbinformationen enthalten ([Erweiterte Farbinformationen](extended-color-information.md)) oder einen anderen Wert für das Interlacing anzeigen ([**MF MT \_ \_ INTERLACE \_ MODE**](mf-mt-interlace-mode-attribute.md)). Diese doppelten Typen sind vorhanden, um ältere DirectShow-Anwendungen zu unterstützen. In einer Media Foundation Anwendung sollten Sie den **Format \_ VideoInfo-Typ** ignorieren, wenn ein doppelter **FORMAT \_ VideoInfo2-Typ** aufgeführt wird.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videoaufnahme](video-capture.md)
</dt> </dl>

 

 



