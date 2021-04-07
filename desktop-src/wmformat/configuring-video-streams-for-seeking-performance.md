---
title: Konfigurieren von Videostreams zum Suchen der Leistung
description: Konfigurieren von Videostreams zum Suchen der Leistung
ms.assetid: 2df507f9-60a5-4489-b3db-7fe15604e625
keywords:
- Streams, Konfigurieren von Videostreams
- Codecs, Konfigurieren von Videostreams
- Videostreams, konfigurieren
- Videostreams, Leistung
- Leistung, Videostreams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33b4fc68e0b3a91cf135d29dc7123d5af88db84c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723437"
---
# <a name="configuring-video-streams-for-seeking-performance"></a><span data-ttu-id="055b7-108">Konfigurieren von Videostreams zum Suchen der Leistung</span><span class="sxs-lookup"><span data-stu-id="055b7-108">Configuring Video Streams for Seeking Performance</span></span>

<span data-ttu-id="055b7-109">Einige Wiedergabe Anwendungen führen viele Suchvorgänge in einzelnen Streams durch.</span><span class="sxs-lookup"><span data-stu-id="055b7-109">Some playback applications perform a lot of seeking on individual streams.</span></span> <span data-ttu-id="055b7-110">Die Suche ist ein Bereich, in dem die Leistung je nach den Einstellungen des Streams stark variieren kann.</span><span class="sxs-lookup"><span data-stu-id="055b7-110">Seeking is an area where performance can vary greatly depending upon the settings of the stream.</span></span> <span data-ttu-id="055b7-111">Wenn Sie wissen, dass Ihre Inhalte für die schnelle Suche optimiert werden müssen, können Sie Ihre Datenstrom Konfiguration anpassen, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="055b7-111">If you know your content needs to be optimized for quick seeking, you can tailor your stream configuration to improve performance.</span></span>

<span data-ttu-id="055b7-112">Der größte Faktor, der sich auf die Geschwindigkeit von Such Vorgängen in Videos auswirkt, ist der Abstand der Keyframes.</span><span class="sxs-lookup"><span data-stu-id="055b7-112">The biggest factor affecting the speed of seeking operations in video is the spacing of the key frames.</span></span> <span data-ttu-id="055b7-113">Da jeder Frame zwischen Keyframes basierend auf den zuvor enthaltenen Frames rekonstruiert werden muss, ergeben weit verbreitete Keyframes längere Suchzeiten.</span><span class="sxs-lookup"><span data-stu-id="055b7-113">Because every frame between key frames needs to be reconstructed based on the frames that come before it, widely spaced key frames result longer seek times.</span></span> <span data-ttu-id="055b7-114">Wenn z. b. ein Videostream mit 30 Frames pro Sekunde einen maximalen Keyframe-Abstand von 10 Sekunden aufweist, gibt es möglicherweise 300 Frames zwischen Keyframes.</span><span class="sxs-lookup"><span data-stu-id="055b7-114">For example, if a video stream with 30 frames per second has a maximum key-frame spacing of 10 seconds, there are potentially 300 frames between key frames.</span></span> <span data-ttu-id="055b7-115">Wenn Sie den letzten [*Delta Rahmen*](wmformat-glossary.md)suchen, müssen 299 Frames rekonstruiert werden, damit der Frame entpackt wird.</span><span class="sxs-lookup"><span data-stu-id="055b7-115">If you seek to the last [*delta frame*](wmformat-glossary.md), 299 frames have to be reconstructed for the frame to be decompressed.</span></span> <span data-ttu-id="055b7-116">Wenn jede Frame-Wiederherstellung 01 Sekunden gedauert hat, dauert die Suche fast 3 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="055b7-116">If each frame reconstruction took .01 second, the seek would take almost 3 seconds.</span></span> <span data-ttu-id="055b7-117">Wenn Sie die Effizienz der Suche erhöhen möchten, kann die Herabsetzung der Keyframe-Abstände helfen.</span><span class="sxs-lookup"><span data-stu-id="055b7-117">If you want to increase the efficiency of seeking, lowering the key-frame spacing can help.</span></span> <span data-ttu-id="055b7-118">Wenn Sie die Keyframes jedoch zu eng beieinander setzen, können Sie die Qualität verlieren.</span><span class="sxs-lookup"><span data-stu-id="055b7-118">However, if you set the key frames too close together, you can lose quality.</span></span>

<span data-ttu-id="055b7-119">Sie können den maximalen Keyframe-Abstand festlegen, indem Sie [**iwmvideomedia-Eigenschaften:: setmaxkeyframespacate**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="055b7-119">You can set the maximum key-frame spacing by calling [**IWMVideoMediaProps::SetMaxKeyFrameSpacing**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmvideomediaprops-setmaxkeyframespacing).</span></span> <span data-ttu-id="055b7-120">Die empfohlenen Werte, die auf der Bitrate des Streams basieren, sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="055b7-120">The recommended values, based on the bit rate of the stream, are listed in the following table.</span></span> <span data-ttu-id="055b7-121">Diese Werte stellen eine gute Balance bei der Suche nach Leistung und Qualität dar.</span><span class="sxs-lookup"><span data-stu-id="055b7-121">These values provide a good balance of seeking performance and quality.</span></span> <span data-ttu-id="055b7-122">Das SDK erzwingt keine Beschränkung für die Zeit zwischen Keyframes.</span><span class="sxs-lookup"><span data-stu-id="055b7-122">The SDK does not enforce any limit on the time between key frames.</span></span> <span data-ttu-id="055b7-123">Im Allgemeinen können sich Zeiten, die länger als 30 Sekunden sind, nachteilig auf die Suchzeiten auswirken, wenn der Inhalt über ein Netzwerk gestreamt wird und wenn der Inhalt lokal wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="055b7-123">In general, times longer than 30 seconds can adversely affect seek times both when the content is streamed over a network, and when it is played back locally.</span></span>



| <span data-ttu-id="055b7-124">Bitrate</span><span class="sxs-lookup"><span data-stu-id="055b7-124">Bit rate</span></span>             | <span data-ttu-id="055b7-125">Vorgeschlagene maximale Schlüssel Frame Abstände</span><span class="sxs-lookup"><span data-stu-id="055b7-125">Suggested maximum key-frame spacing</span></span> |
|----------------------|-------------------------------------|
| <span data-ttu-id="055b7-126">bis zu 300 KBit/s</span><span class="sxs-lookup"><span data-stu-id="055b7-126">22 Kbps to 300 Kbps</span></span>  | <span data-ttu-id="055b7-127">8 Sekunden</span><span class="sxs-lookup"><span data-stu-id="055b7-127">8 seconds</span></span>                           |
| <span data-ttu-id="055b7-128">300 KBit/s auf 600</span><span class="sxs-lookup"><span data-stu-id="055b7-128">300 Kbps to 600 Kbps</span></span> | <span data-ttu-id="055b7-129">6 Sekunden</span><span class="sxs-lookup"><span data-stu-id="055b7-129">6 seconds</span></span>                           |
| <span data-ttu-id="055b7-130">600 bis 2 Mbit/s</span><span class="sxs-lookup"><span data-stu-id="055b7-130">600 Kbps to 2 Mbps</span></span>   | <span data-ttu-id="055b7-131">4 Sekunden</span><span class="sxs-lookup"><span data-stu-id="055b7-131">4 seconds</span></span>                           |
| <span data-ttu-id="055b7-132">2 Mbit/s und höher</span><span class="sxs-lookup"><span data-stu-id="055b7-132">2 Mbps and higher</span></span>    | <span data-ttu-id="055b7-133">3 Sekunden</span><span class="sxs-lookup"><span data-stu-id="055b7-133">3 seconds</span></span>                           |



 

<span data-ttu-id="055b7-134">Weitere Informationen zum erzielen der optimalen Leistung beim Suchen von Videodateien finden Sie unter [erzielen der besten](getting-the-best-video-seeking-performance.md)Leistung beim Suchen von Videodateien.</span><span class="sxs-lookup"><span data-stu-id="055b7-134">For more information about getting the best performance when seeking video files, see [Getting the Best Video Seeking Performance](getting-the-best-video-seeking-performance.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="055b7-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="055b7-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="055b7-136">**Konfigurieren von Streams**</span><span class="sxs-lookup"><span data-stu-id="055b7-136">**Configuring Streams**</span></span>](configuring-streams.md)
</dt> </dl>

 

 




