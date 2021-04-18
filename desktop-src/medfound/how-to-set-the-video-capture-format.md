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
# <a name="how-to-set-the-video-capture-format"></a><span data-ttu-id="8c830-104">Festlegen des Video Erfassungs Formats</span><span class="sxs-lookup"><span data-stu-id="8c830-104">How to Set the Video Capture Format</span></span>

<span data-ttu-id="8c830-105">Ein Video Erfassungsgerät kann mehrere Erfassungs Formate unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8c830-105">A video capture device might support several capture formats.</span></span> <span data-ttu-id="8c830-106">Formate unterscheiden sich in der Regel durch Komprimierungstyp, Farbraum (YUV oder RGB), Frame Größe oder Framerate.</span><span class="sxs-lookup"><span data-stu-id="8c830-106">Formats typically differ by compression type, color space (YUV or RGB), frame size, or frame rate.</span></span>

<span data-ttu-id="8c830-107">Die Liste der unterstützten Formate ist im *Präsentations Deskriptor* enthalten.</span><span class="sxs-lookup"><span data-stu-id="8c830-107">The list of supported formats is contained in the *presentation descriptor*.</span></span> <span data-ttu-id="8c830-108">Weitere Informationen finden Sie unter [Präsentations Deskriptoren](presentation-descriptors.md).</span><span class="sxs-lookup"><span data-stu-id="8c830-108">For more information, see [Presentation Descriptors](presentation-descriptors.md).</span></span>

<span data-ttu-id="8c830-109">So zählen Sie die unterstützten Formate auf:</span><span class="sxs-lookup"><span data-stu-id="8c830-109">To enumerate the supported formats:</span></span>

1.  <span data-ttu-id="8c830-110">Erstellen Sie die Medienquelle für das Erfassungsgerät.</span><span class="sxs-lookup"><span data-stu-id="8c830-110">Create the media source for the capture device.</span></span> <span data-ttu-id="8c830-111">Weitere Informationen finden Sie unter Auflisten von [Video Erfassungs Geräten](enumerating-video-capture-devices.md).</span><span class="sxs-lookup"><span data-stu-id="8c830-111">See [Enumerating Video Capture Devices](enumerating-video-capture-devices.md).</span></span>
2.  <span data-ttu-id="8c830-112">Aufrufen von [**imfmediasource:: foratepresentationdescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) für die Medienquelle zum Abrufen des Präsentations Deskriptors.</span><span class="sxs-lookup"><span data-stu-id="8c830-112">Call [**IMFMediaSource::CreatePresentationDescriptor**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-createpresentationdescriptor) on the media source to get the presentation descriptor.</span></span>
3.  <span data-ttu-id="8c830-113">Aufrufen von [**imfpresentationdescriptor:: getstreamdescriptorbyindex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) zum Abrufen des streamdeskriptors für den Videostream.</span><span class="sxs-lookup"><span data-stu-id="8c830-113">Call [**IMFPresentationDescriptor::GetStreamDescriptorByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfpresentationdescriptor-getstreamdescriptorbyindex) to get the stream descriptor for the video stream.</span></span>
4.  <span data-ttu-id="8c830-114">Aufrufen von [**imfstreamdescriptor:: getmediatypeer Handler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) für den Datenstrom Deskriptor.</span><span class="sxs-lookup"><span data-stu-id="8c830-114">Call [**IMFStreamDescriptor::GetMediaTypeHandler**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamdescriptor-getmediatypehandler) on the stream descriptor.</span></span>
5.  <span data-ttu-id="8c830-115">Aufrufen von [**imfmediatyethandler:: getmediatyetcount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) , um die Anzahl unterstützter Formate zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8c830-115">Call [**IMFMediaTypeHandler::GetMediaTypeCount**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypecount) to get the number of supported formats.</span></span>
6.  <span data-ttu-id="8c830-116">Aufrufen Sie in einer-Schleife [**imfmediatyphandler:: getmediatypeer byindex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) , um jedes Format abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8c830-116">In a loop, call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) to get each format.</span></span> <span data-ttu-id="8c830-117">Das Format wird durch einen *Medientyp* dargestellt.</span><span class="sxs-lookup"><span data-stu-id="8c830-117">The format is represented by a *media type*.</span></span> <span data-ttu-id="8c830-118">Weitere Informationen finden Sie unter [Video Medientypen](video-media-types.md).</span><span class="sxs-lookup"><span data-stu-id="8c830-118">For more information, see [Video Media Types](video-media-types.md).</span></span>

<span data-ttu-id="8c830-119">Im folgenden Beispiel werden die Erfassungs Formate für ein Gerät aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="8c830-119">The following example enumerates the capture formats for a device:</span></span>


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



<span data-ttu-id="8c830-120">Die `LogMediaType` in diesem Beispiel verwendete Funktion ist im Thema [Medientyp Debuggen von Code](media-type-debugging-code.md)aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c830-120">The `LogMediaType` function used in this example is listed in the topic [Media Type Debugging Code](media-type-debugging-code.md).</span></span>

<span data-ttu-id="8c830-121">So legen Sie das Erfassungs Format fest:</span><span class="sxs-lookup"><span data-stu-id="8c830-121">To set the capture format:</span></span>

1.  <span data-ttu-id="8c830-122">Einen Zeiger auf die [**imfmediatypeer Handler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) -Schnittstelle erhalten, wie im vorherigen Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c830-122">Get a pointer to the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface, as shown in the previous example.</span></span>
2.  <span data-ttu-id="8c830-123">Aufrufen von [**imfmediatypeer Handler:: getmediatypeer byindex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) zum Abrufen des gewünschten Formats, angegeben durch Index.</span><span class="sxs-lookup"><span data-stu-id="8c830-123">Call [**IMFMediaTypeHandler::GetMediaTypeByIndex**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-getmediatypebyindex) to get the desired format, specified by index.</span></span>
3.  <span data-ttu-id="8c830-124">Verwenden Sie [**imfmediatyphandler:: setcurrentmediatype**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) , um das Format festzulegen.</span><span class="sxs-lookup"><span data-stu-id="8c830-124">Call [**IMFMediaTypeHandler::SetCurrentMediaType**](/windows/desktop/api/mfidl/nf-mfidl-imfmediatypehandler-setcurrentmediatype) to set the format.</span></span>

<span data-ttu-id="8c830-125">Wenn Sie das Erfassungs Format nicht festlegen, wird das Standardformat des Geräts verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c830-125">If you do not set the capture format, the device will use its default format.</span></span>

<span data-ttu-id="8c830-126">Im folgenden Beispiel wird das Erfassungs Format festgelegt:</span><span class="sxs-lookup"><span data-stu-id="8c830-126">The following example sets the capture format:</span></span>


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



<span data-ttu-id="8c830-127">Die Reihenfolge, in der Formate zurückgegeben werden, hängt vom Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="8c830-127">The order in which formats are returned depends on the device.</span></span> <span data-ttu-id="8c830-128">In der Regel werden Sie zuerst nach Komprimierungstyp oder Farbraum gruppiert. und dann von der kleinsten Frame Größe zur größten Frame Größe innerhalb der einzelnen Gruppen.</span><span class="sxs-lookup"><span data-stu-id="8c830-128">Typically, they are grouped first by compression type or color space; and then from smallest frame size to largest frame size within each group.</span></span>

<span data-ttu-id="8c830-129">Die Framerate werden etwas anders behandelt als die anderen Format Attribute.</span><span class="sxs-lookup"><span data-stu-id="8c830-129">The frame rate is handled slightly differently than the other format attributes.</span></span> <span data-ttu-id="8c830-130">Weitere Informationen finden Sie unter Vorgehens [Weise beim Festlegen der Frame Rate der Video Aufzeichnung](how-to-set-the-video-capture-frame-rate.md).</span><span class="sxs-lookup"><span data-stu-id="8c830-130">For more information, see [How to Set the Video Capture Frame Rate](how-to-set-the-video-capture-frame-rate.md).</span></span>

> [!Note]  
> <span data-ttu-id="8c830-131">In einigen Geräten enthält die Format Liste einen doppelten Eintrag für jedes Format.</span><span class="sxs-lookup"><span data-stu-id="8c830-131">In some devices, the format list will contain a duplicate entry for each format.</span></span> <span data-ttu-id="8c830-132">Wenn das Gerät z. b. 15 unterschiedliche Erfassungs Formate unterstützt, enthält die Liste 30 Einträge.</span><span class="sxs-lookup"><span data-stu-id="8c830-132">For example, if the device supports 15 distinct capture formats, the list will contain 30 entries.</span></span> <span data-ttu-id="8c830-133">In jedem Paar wird für einen der Medientypen das Attribut [**MF \_ MT \_ am \_ \_ formatType**](mf-mt-am-format-type-attribute.md) gleich **Format \_ videoinfo** und für das andere der **MF \_ MT \_ am- \_ \_ Formattyp** gleich **Format \_ VideoInfo2** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8c830-133">Within each pair, one of the media types will have the attribute [**MF\_MT\_AM\_FORMAT\_TYPE**](mf-mt-am-format-type-attribute.md) equal to **FORMAT\_VideoInfo**, and the other will have **MF\_MT\_AM\_FORMAT\_TYPE** equal to **FORMAT\_VideoInfo2**.</span></span> <span data-ttu-id="8c830-134">(Diese beiden Werte sind in der Header Datei UUIDs. h definiert.) Der zweite Typ enthält möglicherweise auch zusätzliche Farbinformationen ([Erweiterte Farbinformationen](extended-color-information.md)) oder einen anderen Wert für das Zeilen Sprung ([**MF MT- \_ \_ Interlace- \_ Modus**](mf-mt-interlace-mode-attribute.md)).</span><span class="sxs-lookup"><span data-stu-id="8c830-134">(These two values are defined in the header file uuids.h.) The second type might also contain additional color information ([Extended Color Information](extended-color-information.md)) or show a different value for interlacing ([**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md)).</span></span> <span data-ttu-id="8c830-135">Diese doppelten Typen sind vorhanden, um ältere DirectShow-Anwendungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8c830-135">These duplicate types exist to support older DirectShow applications.</span></span> <span data-ttu-id="8c830-136">In einer Media Foundation Anwendung sollten Sie den Typ " **\_ videoinfo** " im Format ignorieren, wenn ein doppelter **Format \_ VideoInfo2** Type aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="8c830-136">In a Media Foundation application, you should ignore the **FORMAT\_VideoInfo** type whenever a duplicate **FORMAT\_VideoInfo2** type is listed.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8c830-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8c830-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c830-138">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="8c830-138">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



