---
title: Verwenden von unkomprimierten Audiodaten und Videostreams
description: Verwenden von unkomprimierten Audiodaten und Videostreams
ms.assetid: 1a8fe604-bd99-4ba1-878f-8e1fd89483b3
keywords:
- Streams, Konfigurieren von nicht komprimierten Audiodatenströmen
- Codecs, Konfigurieren von nicht komprimierten Audiodaten und Videostreams
- Videostreams, nicht komprimiert
- Audiostreams, nicht komprimiert
- nicht komprimierte Audiodaten und Videostreams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d00d81bd0a9f8c53751e404a0cfb0e55d57d4242
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106338440"
---
# <a name="using-uncompressed-audio-and-video-streams"></a><span data-ttu-id="41e77-108">Verwenden von unkomprimierten Audiodaten und Videostreams</span><span class="sxs-lookup"><span data-stu-id="41e77-108">Using Uncompressed Audio and Video Streams</span></span>

<span data-ttu-id="41e77-109">In den meisten Fällen sind bei nicht komprimierten Medien sehr hohe Speicher-und Übermittlungs Anforderungen zu erfüllen. für einige lokale Wiedergabe Szenarios ist die Qualitätsstufe jedoch wichtig genug, um die Verwendung der Komprimierung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="41e77-109">Under most circumstances, uncompressed media has prohibitively large storage and delivery requirements, but for some local playback scenarios, the quality level is important enough to warrant not using compression..</span></span>

<span data-ttu-id="41e77-110">Die Einstellungen für einen unkomprimierten Mediendaten Strom sollten die Einstellungen der Quell Medien widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="41e77-110">The settings for an uncompressed media stream should reflect the settings of the source media.</span></span> <span data-ttu-id="41e77-111">Wenn Sie einen unkomprimierten Stream konfigurieren, müssen Sie die Bitrate der Medien berechnen und den Stream entsprechend festlegen, indem Sie [**iwmstreamconfig:: setbitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="41e77-111">When configuring an uncompressed stream, you must calculate the bit rate of the media and set the stream appropriately by calling [**IWMStreamConfig::SetBitrate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbitrate).</span></span> <span data-ttu-id="41e77-112">Da nicht komprimierte Streams für das Streaming nicht nutzbar sind, sollten Sie das Puffer Fenster für nicht komprimierte Mediendaten Ströme immer auf NULL festlegen, indem Sie [**iwmstreamconfig:: setbufferwindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="41e77-112">Because uncompressed streams are not viable for streaming, you should always set the buffer window for uncompressed media streams to zero by calling [**IWMStreamConfig::SetBufferWindow**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setbufferwindow).</span></span>

<span data-ttu-id="41e77-113">Die folgenden Pixel Formate werden für unkomprimierte Videostreams unterstützt:</span><span class="sxs-lookup"><span data-stu-id="41e77-113">The following pixel formats are supported for uncompressed video streams:</span></span>

-   <span data-ttu-id="41e77-114">Wmmediasubtype \_ RGB555</span><span class="sxs-lookup"><span data-stu-id="41e77-114">WMMEDIASUBTYPE\_RGB555</span></span>
-   <span data-ttu-id="41e77-115">Wmmediasubtype \_ RGB24</span><span class="sxs-lookup"><span data-stu-id="41e77-115">WMMEDIASUBTYPE\_RGB24</span></span>
-   <span data-ttu-id="41e77-116">Wmmediasubtype \_ RGB32</span><span class="sxs-lookup"><span data-stu-id="41e77-116">WMMEDIASUBTYPE\_RGB32</span></span>
-   <span data-ttu-id="41e77-117">Wmmediasubtype \_ I420</span><span class="sxs-lookup"><span data-stu-id="41e77-117">WMMEDIASUBTYPE\_I420</span></span>
-   <span data-ttu-id="41e77-118">wmmediasubtype \_ IYUV</span><span class="sxs-lookup"><span data-stu-id="41e77-118">WMMEDIASUBTYPE\_IYUV</span></span>
-   <span data-ttu-id="41e77-119">Wmmediasubtype \_ YV12</span><span class="sxs-lookup"><span data-stu-id="41e77-119">WMMEDIASUBTYPE\_YV12</span></span>
-   <span data-ttu-id="41e77-120">Wmmediasubtype \_ im YUY2</span><span class="sxs-lookup"><span data-stu-id="41e77-120">WMMEDIASUBTYPE\_YUY2</span></span>
-   <span data-ttu-id="41e77-121">wmmediasubtype \_ UYVY</span><span class="sxs-lookup"><span data-stu-id="41e77-121">WMMEDIASUBTYPE\_UYVY</span></span>
-   <span data-ttu-id="41e77-122">wmmediasubtype \_ yvyu</span><span class="sxs-lookup"><span data-stu-id="41e77-122">WMMEDIASUBTYPE\_YVYU</span></span>

## <a name="related-topics"></a><span data-ttu-id="41e77-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="41e77-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41e77-124">**Allgemeine Konfiguration für alle Streams**</span><span class="sxs-lookup"><span data-stu-id="41e77-124">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="41e77-125">**Konfigurieren von Audiodatenströmen**</span><span class="sxs-lookup"><span data-stu-id="41e77-125">**Configuring Audio Streams**</span></span>](configuring-audio-streams.md)
</dt> <dt>

[<span data-ttu-id="41e77-126">**Konfigurieren von Streams**</span><span class="sxs-lookup"><span data-stu-id="41e77-126">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> <dt>

[<span data-ttu-id="41e77-127">**Konfigurieren von Videostreams**</span><span class="sxs-lookup"><span data-stu-id="41e77-127">**Configuring Video Streams**</span></span>](configuring-video-streams.md)
</dt> </dl>

 

 




