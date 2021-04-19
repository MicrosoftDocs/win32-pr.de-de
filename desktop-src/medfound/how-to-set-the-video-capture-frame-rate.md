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
# <a name="how-to-set-the-video-capture-frame-rate"></a><span data-ttu-id="417ef-103">Festlegen der Frame Rate für die Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="417ef-103">How to Set the Video Capture Frame Rate</span></span>

<span data-ttu-id="417ef-104">Ein Video Erfassungsgerät unterstützt möglicherweise einen Bereich von Frameraten.</span><span class="sxs-lookup"><span data-stu-id="417ef-104">A video capture device might support a range of frame rates.</span></span> <span data-ttu-id="417ef-105">Wenn diese Informationen verfügbar sind, werden die minimalen und maximalen Frameraten als Medientyp Attribute gespeichert:</span><span class="sxs-lookup"><span data-stu-id="417ef-105">If this information is available, the minimum and maximum frame rates are stored as media type attributes:</span></span>



| <span data-ttu-id="417ef-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="417ef-106">Attribute</span></span>                                                         | <span data-ttu-id="417ef-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="417ef-107">Description</span></span>         |
|-------------------------------------------------------------------|---------------------|
| [<span data-ttu-id="417ef-108">maximal zulässige Anzahl von MF- \_ MT- \_ Frame \_ Raten \_ \_</span><span class="sxs-lookup"><span data-stu-id="417ef-108">MF\_MT\_FRAME\_RATE\_RANGE\_MAX</span></span>](mf-mt-frame-rate-range-max.md) | <span data-ttu-id="417ef-109">Maximale Framerate.</span><span class="sxs-lookup"><span data-stu-id="417ef-109">Maximum frame rate.</span></span> |
| [<span data-ttu-id="417ef-110">Bereich für die Anzahl von MF \_ MT- \_ Frame \_ Raten \_ \_</span><span class="sxs-lookup"><span data-stu-id="417ef-110">MF\_MT\_FRAME\_RATE\_RANGE\_MIN</span></span>](mf-mt-frame-rate-range-min.md) | <span data-ttu-id="417ef-111">Minimale Framerate.</span><span class="sxs-lookup"><span data-stu-id="417ef-111">Minimum frame rate.</span></span> |



 

<span data-ttu-id="417ef-112">Der Bereich kann je nach Erfassungs Format variieren.</span><span class="sxs-lookup"><span data-stu-id="417ef-112">The range can vary depending on the capture format.</span></span> <span data-ttu-id="417ef-113">Beispielsweise kann bei größeren Frame Größen die maximale Framerate reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="417ef-113">For example, at larger frame sizes, the maximum frame rate might be reduced.</span></span>

<span data-ttu-id="417ef-114">So legen Sie die Framerate fest:</span><span class="sxs-lookup"><span data-stu-id="417ef-114">To set the frame rate:</span></span>

1.  <span data-ttu-id="417ef-115">Erstellen Sie die Medienquelle für das Erfassungsgerät.</span><span class="sxs-lookup"><span data-stu-id="417ef-115">Create the media source for the capture device.</span></span> <span data-ttu-id="417ef-116">Weitere Informationen finden Sie unter Auflisten von [Video Erfassungs Geräten](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="417ef-116">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="417ef-117">Aufrufen von [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) für die Medienquelle zum Abrufen des Präsentations Deskriptors.</span><span class="sxs-lookup"><span data-stu-id="417ef-117">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source to get the presentation descriptor.</span></span>
3.  <span data-ttu-id="417ef-118">Aufrufen von [**imfpresentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) zum Abrufen des streamdeskriptors für den Videostream.</span><span class="sxs-lookup"><span data-stu-id="417ef-118">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to get the stream descriptor for the video stream.</span></span>
4.  <span data-ttu-id="417ef-119">Aufrufen von [**imfstreamdescriptor:: getmediatypeer Handler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) für den Datenstrom Deskriptor.</span><span class="sxs-lookup"><span data-stu-id="417ef-119">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span>
5.  <span data-ttu-id="417ef-120">Auflisten der Erfassungs Formate, wie unter Gewusst [wie: Festlegen des Video Erfassungs Formats](how-to-set-the-video-capture-format.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="417ef-120">Enumerate the capture formats, as described in [How to Set the Video Capture Format](how-to-set-the-video-capture-format.md).</span></span>
6.  <span data-ttu-id="417ef-121">Wählen Sie das gewünschte Ausgabeformat aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="417ef-121">Select the desired output format from the list.</span></span>
7.  <span data-ttu-id="417ef-122">Fragen Sie den Medientyp für den Bereich " [MF \_ MT \_ Frame \_ Rate \_ Range \_ Max](mf-mt-frame-rate-range-max.md) " und " [MF \_ MT \_ Frame \_ Rate \_ Range \_ Min](mf-mt-frame-rate-range-min.md) Attribute" ab.</span><span class="sxs-lookup"><span data-stu-id="417ef-122">Query the media type for the [MF\_MT\_FRAME\_RATE\_RANGE\_MAX](mf-mt-frame-rate-range-max.md) and [MF\_MT\_FRAME\_RATE\_RANGE\_MIN](mf-mt-frame-rate-range-min.md) attributes.</span></span> <span data-ttu-id="417ef-123">Diese Werte gibt den Bereich der unterstützten Frameraten an.</span><span class="sxs-lookup"><span data-stu-id="417ef-123">This values give the range of supported frame rates.</span></span> <span data-ttu-id="417ef-124">Das Gerät unterstützt möglicherweise andere Frameraten innerhalb dieses Bereichs.</span><span class="sxs-lookup"><span data-stu-id="417ef-124">The device might support other frame rates within this range.</span></span>
8.  <span data-ttu-id="417ef-125">Legen Sie das [**MF \_ MT- \_ Frame**](mf-mt-frame-rate-attribute.md) -Attribut für den Medientyp fest, um die gewünschte Frame Rate anzugeben.</span><span class="sxs-lookup"><span data-stu-id="417ef-125">Set the [**MF\_MT\_FRAME**](mf-mt-frame-rate-attribute.md) attribute on the media type to specify the desired frame rate.</span></span>
9.  <span data-ttu-id="417ef-126">Aufrufen von [**imfmediatyphandler:: setcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) mit dem geänderten Medientyp.</span><span class="sxs-lookup"><span data-stu-id="417ef-126">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) with the modified media type.</span></span>

<span data-ttu-id="417ef-127">Im folgenden Beispiel wird die Framerate auf die maximale Framerate festgelegt, die vom Gerät unterstützt wird:</span><span class="sxs-lookup"><span data-stu-id="417ef-127">The following example sets the frame rate equal to the maximum frame rate that the device supports:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="417ef-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="417ef-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="417ef-129">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="417ef-129">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



