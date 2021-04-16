---
description: Konfigurieren des Video Ausgabeformats
ms.assetid: 1969072e-575e-49b4-88db-4c7e7a5a1c37
title: Konfigurieren des Video Ausgabeformats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d09ac64d7f43e6c39377277544867491a93a6f3e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104557878"
---
# <a name="configure-the-video-output-format"></a><span data-ttu-id="5c8f3-103">Konfigurieren des Video Ausgabeformats</span><span class="sxs-lookup"><span data-stu-id="5c8f3-103">Configure the Video Output Format</span></span>

> [!Note]  
> <span data-ttu-id="5c8f3-104">Die in diesem Thema beschriebene Funktionalität ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-104">The functionality described in this topic is deprecated.</span></span> <span data-ttu-id="5c8f3-105">Um das Ausgabeformat eines Aufzeichnungs Geräts zu konfigurieren, muss eine Anwendung die [**am \_ \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur verwenden, die von [**iamstreamconfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) im *PMT* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-105">To configure a capture device's output format, an application should use the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure returned by [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) in the *pmt* parameter.</span></span>

 

<span data-ttu-id="5c8f3-106">Ein Erfassungsgerät kann verschiedene Ausgabeformate unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-106">A capture device can support a range of output formats.</span></span> <span data-ttu-id="5c8f3-107">Ein Gerät kann z. b. 16-Bit-RGB, 32-Bit RGB und yuyv unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-107">For example, a device might support 16-bit RGB, 32-bit RGB, and YUYV.</span></span> <span data-ttu-id="5c8f3-108">Innerhalb jedes dieser Formate kann das Gerät einen Bereich von Frame Größen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-108">Within each of these formats, the device can support a range of frame sizes.</span></span>

<span data-ttu-id="5c8f3-109">In einem WDM-Gerät wird die [**iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) -Schnittstelle verwendet, um zu melden, welche Formate das Gerät unterstützt, und um das Format festzulegen.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-109">In a WDM device, the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface is used to report which formats the device supports, and to set the format.</span></span> <span data-ttu-id="5c8f3-110">(Verwenden Sie für ältere VFW-Geräte das Dialogfeld VFW des Video Formats, wie in [Dialogfeldern zum Anzeigen der Vfw-Erfassung](display-vfw-capture-dialog-boxes.md)beschrieben.) Die **iamstreamconfig** -Schnittstelle wird in der Erfassungs-PIN, der Vorschau-PIN oder beiden der Erfassungs Filter verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-110">(For legacy VFW devices, use the Video Format VFW dialog box, as described in [Display VFW Capture Dialog Boxes](display-vfw-capture-dialog-boxes.md).) The **IAMStreamConfig** interface is exposed on the capture filter's capture pin, preview pin, or both.</span></span> <span data-ttu-id="5c8f3-111">Verwenden Sie die [**ICaptureGraphBuilder2:: findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) -Methode, um den Schnittstellen Zeiger zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="5c8f3-111">Use the [**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface) method to get the interface pointer:</span></span>


```C++
IAMStreamConfig *pConfig = NULL;
hr = pBuild->FindInterface(
    &PIN_CATEGORY_PREVIEW, // Preview pin.
    0,    // Any media type.
    pCap, // Pointer to the capture filter.
    IID_IAMStreamConfig, (void**)&pConfig);
```



<span data-ttu-id="5c8f3-112">Das Gerät verfügt über eine Liste der von ihm unterstützten Medientypen.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-112">The device has a list of media types that it supports.</span></span> <span data-ttu-id="5c8f3-113">Für jeden Medientyp stellt das Gerät auch eine Reihe von Funktionen bereit.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-113">For each media type, the device also provides a set of capabilities.</span></span> <span data-ttu-id="5c8f3-114">Dazu zählen der Bereich der Frame Größen, die für dieses Format verfügbar sind, wie gut das Gerät das Bildstrecken oder verkleinern kann, und der Bereich der Frameraten.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-114">These include the range of frame sizes that are available for that format, how well the device can stretch or shrink the image, and the range of frame rates.</span></span>

<span data-ttu-id="5c8f3-115">Um die Anzahl der Medientypen abzurufen, müssen Sie die [**iamstreamconfig:: getnumoffunktionalitäten**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-115">To get the number of media types, call the [**IAMStreamConfig::GetNumberOfCapabilities**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getnumberofcapabilities) method.</span></span> <span data-ttu-id="5c8f3-116">Die-Methode gibt zwei Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="5c8f3-116">The method returns two values:</span></span>

-   <span data-ttu-id="5c8f3-117">Die Anzahl der Medientypen.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-117">The number of media types.</span></span>
-   <span data-ttu-id="5c8f3-118">Die Größe der-Struktur, die die Funktions Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-118">The size of the structure that holds the capabilities information.</span></span>

<span data-ttu-id="5c8f3-119">Der Größen Wert ist erforderlich, da die [**iamstreamconfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) -Schnittstelle sowohl für Audiodaten als auch für Video verwendet wird (und auf andere Medientypen erweitert werden kann).</span><span class="sxs-lookup"><span data-stu-id="5c8f3-119">The size value is necessary because the [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig) interface is used for both audio and video (and could be extended to other media types).</span></span> <span data-ttu-id="5c8f3-120">Für das Video werden die Funktionen mithilfe der [**\_ videolstream \_ - \_ Konfigurations**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) Ober Struktur beschrieben, während die Audiostruktur die Struktur der [**audiodatenstream-Konfigurations Ober \_ \_ \_ Grenzen**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-120">For video, the capabilities are described using the [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure, while audio uses the [**AUDIO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-audio_stream_config_caps) structure.</span></span>

<span data-ttu-id="5c8f3-121">Um die Medientypen aufzulisten, müssen Sie die [**iamstreamconfig:: getstreamcaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) -Methode mit einem NULL basierten Index aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-121">To enumerate the media types, call the [**IAMStreamConfig::GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method with a zero-based index.</span></span> <span data-ttu-id="5c8f3-122">Die **getstreamcaps** -Methode gibt einen Medientyp und die entsprechende Funktionsstruktur zurück:</span><span class="sxs-lookup"><span data-stu-id="5c8f3-122">The **GetStreamCaps** method returns a media type and the corresponding capability structure:</span></span>


```C++
int iCount = 0, iSize = 0;
hr = pConfig->GetNumberOfCapabilities(&iCount, &iSize);

// Check the size to make sure we pass in the correct structure.
if (iSize == sizeof(VIDEO_STREAM_CONFIG_CAPS))
{
    // Use the video capabilities structure.

    for (int iFormat = 0; iFormat < iCount; iFormat++)
    {
        VIDEO_STREAM_CONFIG_CAPS scc;
        AM_MEDIA_TYPE *pmtConfig;
        hr = pConfig->GetStreamCaps(iFormat, &pmtConfig, (BYTE*)&scc);
        if (SUCCEEDED(hr))
        {
            /* Examine the format, and possibly use it. */

            // Delete the media type when you are done.
            DeleteMediaType(pmtConfig);
        }
}
```



<span data-ttu-id="5c8f3-123">Beachten Sie, wie die-Strukturen für die [**getstreamcaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) -Methode zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-123">Note how the structures are allocated for the [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="5c8f3-124">Die-Methode ordnet die Medientyp Struktur zu, während der Aufrufer die Funktionsstruktur ordnet.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-124">The method allocates the media type structure, whereas the caller allocates the capabilities structure.</span></span> <span data-ttu-id="5c8f3-125">Wandelt die Funktionsstruktur in einen Byte Array Zeiger um.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-125">Coerce the capabilities structure to a byte array pointer.</span></span> <span data-ttu-id="5c8f3-126">Nachdem Sie den Medientyp abgeschlossen haben, löschen Sie die [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur zusammen mit dem Format Block des Medientyps.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-126">After you are done with the media type, delete the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure, along with the media type's format block.</span></span>

<span data-ttu-id="5c8f3-127">Sie können das Gerät so konfigurieren, dass es ein in der [**getstreamcaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) -Methode zurück gegebenes Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-127">You can configure the device to use a format returned in the [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) method.</span></span> <span data-ttu-id="5c8f3-128">Nennen Sie einfach [**iamstreamconfig:: SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) mit dem Medientyp:</span><span class="sxs-lookup"><span data-stu-id="5c8f3-128">Simply call [**IAMStreamConfig::SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) with the media type:</span></span>


```C++
hr = pConfig->SetFormat(pmtConfig);
```



<span data-ttu-id="5c8f3-129">Wenn die PIN nicht verbunden ist, wird versucht, dieses Format zu verwenden, wenn eine Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-129">If the pin is not connected, it will attempt to use this format when it does connect.</span></span> <span data-ttu-id="5c8f3-130">Wenn die PIN bereits verbunden ist, wird versucht, die Verbindung unter Verwendung des neuen Formats wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-130">If the pin is already connected, it attempts to reconnect using the new format.</span></span> <span data-ttu-id="5c8f3-131">In beiden Fällen ist es möglich, dass der Downstream-Filter das Format ablehnt.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-131">In either case, it is possible that the downstream filter will reject the format.</span></span>

<span data-ttu-id="5c8f3-132">Sie können den Medientyp auch ändern, bevor Sie ihn an die [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) -Methode übergeben.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-132">You can also modify the media type before passing it to the [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) method.</span></span> <span data-ttu-id="5c8f3-133">An dieser Stelle kommt die Struktur der [**Video Daten \_ Strom-Konfigurations Ober \_ \_ Grenzen**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) ins Spiel.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-133">This is where the [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure comes in.</span></span> <span data-ttu-id="5c8f3-134">Es beschreibt alle gültigen Möglichkeiten, den Medientyp zu ändern.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-134">It describes all of the valid ways to change the media type.</span></span> <span data-ttu-id="5c8f3-135">Um diese Informationen verwenden zu können, müssen Sie die Details dieses bestimmten Medientyps verstehen.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-135">To use this information, you must understand the details of that particular media type.</span></span>

<span data-ttu-id="5c8f3-136">Nehmen wir beispielsweise an, dass [**getstreamcaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) ein 24-Bit-RGB-Format mit einer Frame Größe von 320 x 240 Pixel zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-136">For example, suppose that [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps) returns a 24-bit RGB format, with a frame size of 320 x 240 pixels.</span></span> <span data-ttu-id="5c8f3-137">Sie erhalten diese Informationen, indem Sie den Haupttyp, den Untertyp und den Format Block des Medientyps untersuchen:</span><span class="sxs-lookup"><span data-stu-id="5c8f3-137">You can get this information by examining the major type, subtype, and format block of the media type:</span></span>


```C++
if ((pmtConfig.majortype == MEDIATYPE_Video) &&
    (pmtConfig.subtype == MEDIASUBTYPE_RGB24) &&
    (pmtConfig.formattype == FORMAT_VideoInfo) &&
    (pmtConfig.cbFormat >= sizeof (VIDEOINFOHEADER)) &&
    (pmtConfig.pbFormat != NULL))
{
    VIDEOINFOHEADER *pVih = (VIDEOINFOHEADER*)pmtConfig.pbFormat;
    // pVih contains the detailed format information.
    LONG lWidth = pVih->bmiHeader.biWidth;
    LONG lHeight = pVih->bmiHeader.biHeight;
}
```



<span data-ttu-id="5c8f3-138">Die Struktur der [**\_ \_ videostreamkonfigurationscaps \_**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) gibt die minimale und maximale Breite und Höhe an, die für diesen Medientyp verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-138">The [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) structure gives the minimum and maximum width and height that can be used for this media type.</span></span> <span data-ttu-id="5c8f3-139">Außerdem erhalten Sie die "Schritt"-Größe, mit der die Inkremente definiert werden, um die Sie die Breite oder Höhe anpassen können.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-139">It also gives you the "step" size, which defines the increments by which you can adjust the width or height.</span></span> <span data-ttu-id="5c8f3-140">Das Gerät könnte z. b. Folgendes zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="5c8f3-140">For example, the device might return the following:</span></span>

-   <span data-ttu-id="5c8f3-141">Minoutputsize: 160 x 120</span><span class="sxs-lookup"><span data-stu-id="5c8f3-141">MinOutputSize: 160 x 120</span></span>
-   <span data-ttu-id="5c8f3-142">Maxoutputsize: 320 x 240</span><span class="sxs-lookup"><span data-stu-id="5c8f3-142">MaxOutputSize: 320 x 240</span></span>
-   <span data-ttu-id="5c8f3-143">Outputgranularityx: 8 Pixel (horizontale Schrittgröße)</span><span class="sxs-lookup"><span data-stu-id="5c8f3-143">OutputGranularityX: 8 pixels (horizontal step size)</span></span>
-   <span data-ttu-id="5c8f3-144">Outputgranularityy: 8 Pixel (vertikale Schrittgröße)</span><span class="sxs-lookup"><span data-stu-id="5c8f3-144">OutputGranularityY: 8 pixels (vertical step size)</span></span>

<span data-ttu-id="5c8f3-145">Wenn Sie diese Zahlen haben, können Sie die Breite auf alles im Bereich festlegen (160, 168, 176,... 304, 312, 320) und die Höhe auf alles im Bereich (120, 128, 136,... 104, 112, 120).</span><span class="sxs-lookup"><span data-stu-id="5c8f3-145">Given these numbers, you could set the width to anything in the range (160, 168, 176, ... 304, 312, 320) and the height to anything in the range (120, 128, 136, ... 104, 112, 120).</span></span> <span data-ttu-id="5c8f3-146">Dieser Prozess wird anhand des folgenden Diagramms veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-146">The following diagram illustrates this process.</span></span>

![Video Formatgrößen](images/strmcap3.png)

<span data-ttu-id="5c8f3-148">Um eine neue Frame Größe festzulegen, ändern Sie [**die \_ am \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) -Struktur, die in [**getstreamcaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps)zurückgegeben wird, direkt.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-148">To set a new frame size, directly modify the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure returned in [**GetStreamCaps**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getstreamcaps):</span></span>


```C++
pVih->bmiHeader.biWidth = 160;
pVih->bmiHeader.biHeight = 120;
pVih->bmiHeader.biSizeImage = DIBSIZE(pVih->bmiHeader);
```



<span data-ttu-id="5c8f3-149">Übergeben Sie den Medientyp dann an die [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) -Methode, wie zuvor beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-149">Then pass the media type to the [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat) method, as described previously.</span></span>

<span data-ttu-id="5c8f3-150">Die **minframeinterval** -und **maxframeinterval** -Member von [**Videodaten Strom- \_ \_ Konfigurations \_ Caps**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) sind die Mindest-und höchst Länge jedes Video Rahmens, den Sie wie folgt in die Frameraten umwandeln können:</span><span class="sxs-lookup"><span data-stu-id="5c8f3-150">The **MinFrameInterval** and **MaxFrameInterval** members of [**VIDEO\_STREAM\_CONFIG\_CAPS**](/windows/win32/api/strmif/ns-strmif-video_stream_config_caps) are the minimum and maximum length of each video frame, which you can translate into frame rates as follows:</span></span>

`frames per second = 10,000,000 / frame duration`

<span data-ttu-id="5c8f3-151">Um eine bestimmte Framerate anzufordern, ändern Sie den Wert von **avgtimeperframe** in der [**videoinfoheader**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) -oder [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Struktur im Medientyp.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-151">To request a particular frame rate, modify the value of **AvgTimePerFrame** in the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure in the media type.</span></span> <span data-ttu-id="5c8f3-152">Das Gerät unterstützt möglicherweise nicht alle möglichen Werte zwischen dem minimal-und Maximalwert, sodass der Treiber den nächstgelegenen Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-152">The device may not support every possible value between the minimum and maximum, so the driver will use the closest value that it can.</span></span> <span data-ttu-id="5c8f3-153">Um festzustellen, welchen Wert der Treiber tatsächlich verwendet hat, müssen Sie [**iamstreamconfig:: GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) aufrufen, nachdem Sie [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat)aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-153">To see what value the driver actually used, call [**IAMStreamConfig::GetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-getformat) after you call [**SetFormat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamconfig-setformat).</span></span>

<span data-ttu-id="5c8f3-154">Einige Treiber melden möglicherweise **maxlonglong** (0x7FFFFFFFFFFFFFFF) als Wert von **maxframeinterval**, was bedeutet, dass es keine maximale Dauer gibt.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-154">Some drivers may report **MAXLONGLONG** (0x7FFFFFFFFFFFFFFF) for the value of **MaxFrameInterval**, which in effect means there is no maximum duration.</span></span> <span data-ttu-id="5c8f3-155">Möglicherweise möchten Sie jedoch eine minimale Frame Rate in der Anwendung erzwingen, z. b. 1 fps.</span><span class="sxs-lookup"><span data-stu-id="5c8f3-155">However, you might want to enforce a minimum frame rate in your application, such as 1 fps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5c8f3-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c8f3-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c8f3-157">Informationen zu Medientypen</span><span class="sxs-lookup"><span data-stu-id="5c8f3-157">About Media Types</span></span>](about-media-types.md)
</dt> <dt>

[<span data-ttu-id="5c8f3-158">Konfigurieren eines Video Erfassungs Geräts</span><span class="sxs-lookup"><span data-stu-id="5c8f3-158">Configuring a Video Capture Device</span></span>](configuring-a-video-capture-device.md)
</dt> </dl>

 

 



