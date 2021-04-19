---
title: Konfigurieren von Videostreams
description: Konfigurieren von Videostreams
ms.assetid: caffdfc1-3c35-4b7b-8643-5a9095cc11f6
keywords:
- Streams, Konfigurieren von Videostreams
- Codecs, Konfigurieren von Videostreams
- Videostreams, konfigurieren
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d2389026dc1061064c5e687da60c3350ad94a4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341702"
---
# <a name="configuring-video-streams"></a><span data-ttu-id="1be22-106">Konfigurieren von Videostreams</span><span class="sxs-lookup"><span data-stu-id="1be22-106">Configuring Video Streams</span></span>

<span data-ttu-id="1be22-107">Videostreams sind in Ihrer Konfiguration flexibler als Audiodatenströme.</span><span class="sxs-lookup"><span data-stu-id="1be22-107">Video streams are more flexible in their configuration than audio streams.</span></span> <span data-ttu-id="1be22-108">Dies liegt daran, dass die Eigenschaften der Frames, aus denen sich das Video besteht, von einer Datei zur nächsten variieren können.</span><span class="sxs-lookup"><span data-stu-id="1be22-108">This is because the properties of the frames that make up the video can vary widely from one file to the next.</span></span> <span data-ttu-id="1be22-109">Wenn Sie das Codec-Format für den Codec abrufen, den Sie verwenden, müssen Sie für videostreamkonfigurationsobjekte die folgenden Werte festlegen.</span><span class="sxs-lookup"><span data-stu-id="1be22-109">When you retrieve the codec format for the codec you are using, you must set the following values for video stream configuration objects.</span></span>



| <span data-ttu-id="1be22-110">Wert</span><span class="sxs-lookup"><span data-stu-id="1be22-110">Value</span></span>                                 | <span data-ttu-id="1be22-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1be22-111">Description</span></span>                                                                                                                                                                                                                                                                 |
|---------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1be22-112">Bitrate</span><span class="sxs-lookup"><span data-stu-id="1be22-112">Bit rate</span></span>                              | <span data-ttu-id="1be22-113">Nennen Sie [**iwmstreamconfig:: setbitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) , um auf den gewünschten Wert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1be22-113">Call [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate) to set to the desired value.</span></span> <span data-ttu-id="1be22-114">Der Videocodec versucht, die Medien zu komprimieren, um ihre Spezifikationen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="1be22-114">The video codec will try to compress the media to meet your specifications.</span></span> <span data-ttu-id="1be22-115">Wenn Ihre Werte zu niedrig sind, wird das resultierende komprimierte Video stark beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="1be22-115">If your values are too low, the resulting compressed video will be very degraded.</span></span>           |
| <span data-ttu-id="1be22-116">Puffer Fenster</span><span class="sxs-lookup"><span data-stu-id="1be22-116">Buffer window</span></span>                         | <span data-ttu-id="1be22-117">Nennen Sie [**iwmstreamconfig:: setbufferwindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) , um auf den gewünschten Wert festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1be22-117">Call [**IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow) to set to the desired value.</span></span> <span data-ttu-id="1be22-118">Der Videocodec versucht, die Medien zu komprimieren, um ihre Spezifikationen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="1be22-118">The video codec will try to compress the media to meet your specifications.</span></span> <span data-ttu-id="1be22-119">Wenn Ihre Werte zu niedrig sind, wird das resultierende komprimierte Video stark beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="1be22-119">If your values are too low, the resulting compressed video will be very degraded.</span></span> |
| <span data-ttu-id="1be22-120">**Wmvideoinfoheader. rcSource**</span><span class="sxs-lookup"><span data-stu-id="1be22-120">**WMVIDEOINFOHEADER.rcSource**</span></span>        | <span data-ttu-id="1be22-121">Die linke obere Ecke muss auf 0, 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1be22-121">The upper left corner must be set to 0,0.</span></span> <span data-ttu-id="1be22-122">Die untere rechte Ecke muss auf die Frame Dimensionen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1be22-122">The lower right corner must be set to the frame dimensions.</span></span> <span data-ttu-id="1be22-123">Beispielsweise sind in einem 640 x480-Stream diese Einstellungen 0, 0640480.</span><span class="sxs-lookup"><span data-stu-id="1be22-123">For example, in a 640x480 stream, these settings would be 0,0,640,480.</span></span>                                                                                                |
| <span data-ttu-id="1be22-124">**Wmvideoinfoheader. rctarget**</span><span class="sxs-lookup"><span data-stu-id="1be22-124">**WMVIDEOINFOHEADER.rcTarget**</span></span>        | <span data-ttu-id="1be22-125">Muss mit **rcSource** verglichen werden.</span><span class="sxs-lookup"><span data-stu-id="1be22-125">Must match **rcSource**.</span></span>                                                                                                                                                                                                                                                    |
| <span data-ttu-id="1be22-126">**Wmvideoinfoheader. dwbitrate**</span><span class="sxs-lookup"><span data-stu-id="1be22-126">**WMVIDEOINFOHEADER.dwBitRate**</span></span>       | <span data-ttu-id="1be22-127">Muss mit der für den Stream festgelegten Bitrate identisch sein.</span><span class="sxs-lookup"><span data-stu-id="1be22-127">Must match the bit rate set for the stream.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="1be22-128">**Wmvideoinfoheader. Avgtimeperframe**</span><span class="sxs-lookup"><span data-stu-id="1be22-128">**WMVIDEOINFOHEADER.AvgTimePerFrame**</span></span> | <span data-ttu-id="1be22-129">Legen Sie auf die ungefähre Zeit pro Frame fest.</span><span class="sxs-lookup"><span data-stu-id="1be22-129">Set to the approximate time per frame.</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="1be22-130">**BITMAPINFOHEADER. biwidth**</span><span class="sxs-lookup"><span data-stu-id="1be22-130">**BITMAPINFOHEADER.biWidth**</span></span>          | <span data-ttu-id="1be22-131">Legen Sie auf die Breite der gewünschten Frame Größe in Pixel fest.</span><span class="sxs-lookup"><span data-stu-id="1be22-131">Set to the width, in pixels, of the desired frame size.</span></span>                                                                                                                                                                                                                     |
| <span data-ttu-id="1be22-132">**BITMAPINFOHEADER. biheight**</span><span class="sxs-lookup"><span data-stu-id="1be22-132">**BITMAPINFOHEADER.biHeight**</span></span>         | <span data-ttu-id="1be22-133">Legen Sie auf die Höhe der gewünschten Frame Größe in Pixel fest.</span><span class="sxs-lookup"><span data-stu-id="1be22-133">Set to the height, in pixels, of the desired frame size.</span></span>                                                                                                                                                                                                                    |



 

<span data-ttu-id="1be22-134">Video Inhalte werden nur dann ordnungsgemäß abgespielt, wenn Sie in einer Größe codiert sind, die für Breite und Höhe ein Vielfaches von vier ist.</span><span class="sxs-lookup"><span data-stu-id="1be22-134">Video content does not play correctly unless it is encoded to a size that is a multiple of four for both width and height.</span></span> <span data-ttu-id="1be22-135">Die Ausnahme ist ein nicht komprimiertes [*RGB*](wmformat-glossary.md) -Video, das eine beliebige Größe aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="1be22-135">The exception is [*RGB*](wmformat-glossary.md) uncompressed video, which can be any size.</span></span> <span data-ttu-id="1be22-136">Wenn Sie versuchen, eine Größe festzulegen, die kein Vielfaches von vier ist, wird einer der folgenden Fehler vom Writer zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="1be22-136">If you try to set a size that is not a multiple of four, one of the following errors will be returned by the writer:</span></span>

-   <span data-ttu-id="1be22-137">NS \_ E ( \_ ungültiges \_ Eingabe \_ Format)</span><span class="sxs-lookup"><span data-stu-id="1be22-137">NS\_E\_INVALID\_INPUT\_FORMAT</span></span>
-   <span data-ttu-id="1be22-138">\_Ungültiges NS E- \_ \_ Ausgabe \_ Format</span><span class="sxs-lookup"><span data-stu-id="1be22-138">NS\_E\_INVALID\_OUTPUT\_FORMAT</span></span>
-   <span data-ttu-id="1be22-139">NS \_ E \_ invalidprofile</span><span class="sxs-lookup"><span data-stu-id="1be22-139">NS\_E\_INVALIDPROFILE</span></span>

<span data-ttu-id="1be22-140">Wenn Sie die variablenbitrate-Codierung verwenden, müssen Sie möglicherweise weitere Anpassungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="1be22-140">If you are using variable bit rate encoding, you may need to make other adjustments.</span></span> <span data-ttu-id="1be22-141">Weitere Informationen finden Sie unter [Konfigurieren von VBR-Streams](configuring-vbr-streams.md).</span><span class="sxs-lookup"><span data-stu-id="1be22-141">For more information, see [Configuring VBR Streams](configuring-vbr-streams.md).</span></span>

<span data-ttu-id="1be22-142">Einige Windows Media Video Codecs unterstützen mehrere Komplexitäts Ebenen.</span><span class="sxs-lookup"><span data-stu-id="1be22-142">Some Windows Media Video codecs support multiple complexity levels.</span></span> <span data-ttu-id="1be22-143">Komplexitäts Ebenen bestimmen die Algorithmen, die der Codec beim Codieren eines Videostreams verwendet.</span><span class="sxs-lookup"><span data-stu-id="1be22-143">Complexity levels determine the algorithms that the codec will use when encoding a video stream.</span></span> <span data-ttu-id="1be22-144">Die Verwendung einer hohen Komplexitäts Stufe erfordert mehr Verarbeitungsleistung für die Codierung und Decodierung.</span><span class="sxs-lookup"><span data-stu-id="1be22-144">Using a high complexity level will require more processing power for encoding and decoding.</span></span>

<span data-ttu-id="1be22-145">Jeder Codec, der Komplexitäts Einstellungen unterstützt, macht die folgenden Einstellungen verfügbar, die Sie mit der [**IWMCodecInfo3:: getcodecprop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) -Methode abrufen können.</span><span class="sxs-lookup"><span data-stu-id="1be22-145">Each codec that supports complexity settings exposes the following settings that you can retrieve with the [**IWMCodecInfo3::GetCodecProp**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmcodecinfo3-getcodecprop) method.</span></span>



| <span data-ttu-id="1be22-146">Einstellung</span><span class="sxs-lookup"><span data-stu-id="1be22-146">Setting</span></span>                 | <span data-ttu-id="1be22-147">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1be22-147">Description</span></span>                                         |
|-------------------------|-----------------------------------------------------|
| <span data-ttu-id="1be22-148">g \_ wszcomplexitymax</span><span class="sxs-lookup"><span data-stu-id="1be22-148">g\_wszComplexityMax</span></span>     | <span data-ttu-id="1be22-149">Die vom Codec unterstützte maximale Qualitätsstufe.</span><span class="sxs-lookup"><span data-stu-id="1be22-149">The maximum quality level supported by the codec.</span></span>   |
| <span data-ttu-id="1be22-150">g \_ wszcomplexityoffline</span><span class="sxs-lookup"><span data-stu-id="1be22-150">g\_wszComplexityOffline</span></span> | <span data-ttu-id="1be22-151">Die empfohlene Qualitätsstufe für die Offline Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="1be22-151">The suggested quality level for offline playback.</span></span>   |
| <span data-ttu-id="1be22-152">g \_ wszcomplexitylive</span><span class="sxs-lookup"><span data-stu-id="1be22-152">g\_wszComplexityLive</span></span>    | <span data-ttu-id="1be22-153">Die empfohlene Qualitätsstufe für die Streaming-Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="1be22-153">The suggested quality level for streaming playback.</span></span> |



 

<span data-ttu-id="1be22-154">Um die Komplexität für einen Videostream in einem Profil festzulegen, verwenden Sie die [**iwmpropertyvault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) -Methode mithilfe der Eigenschaft g \_ wszkomplexitäts.</span><span class="sxs-lookup"><span data-stu-id="1be22-154">To set the complexity for a video stream in a profile, use the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method using the property g\_wszComplexity.</span></span> <span data-ttu-id="1be22-155">Der von Ihnen festgelegte Wert muss kleiner oder gleich der maximalen unterstützten Komplexität für den Codec sein.</span><span class="sxs-lookup"><span data-stu-id="1be22-155">The value you set must be less than or equal to the maximum supported complexity for the codec.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1be22-156">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1be22-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1be22-157">**Allgemeine Konfiguration für alle Streams**</span><span class="sxs-lookup"><span data-stu-id="1be22-157">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="1be22-158">**Konfigurieren von Streams**</span><span class="sxs-lookup"><span data-stu-id="1be22-158">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="1be22-159">**Video Komplexitäts Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="1be22-159">**Video Complexity Settings**</span></span>](video-complexity-settings.md)
</dt> </dl>

 

 




