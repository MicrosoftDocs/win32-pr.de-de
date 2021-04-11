---
title: Implementieren eines Video DSP-Plug-ins
description: Implementieren eines Video DSP-Plug-ins
ms.assetid: 36c06c57-7623-430b-8280-9dba7b0a2e9b
keywords:
- Windows Media Player-Plug-ins, videodsp
- Plug-ins, videodsp
- Plug-Ins für die digitale Signalverarbeitung, Implementieren von Code
- DSP-Plug-ins, Implementieren von Code
- Plug-Ins für die digitale Signalverarbeitung, Ändern von Beispielcode
- DSP-Plug-ins, Ändern von Beispielcode
- Plug-Ins für die digitale Signalverarbeitung, Video Implementierung
- DSP-Plug-ins, Video Implementierung
- Video DSP-Plug-ins, Implementieren von Code
- Video DSP-Plug-ins, Ändern von Beispielcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f1b819f328fc586d21208c00b6f0d03dca4fe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310259"
---
# <a name="implementing-a-video-dsp-plug-in"></a><span data-ttu-id="ce6ef-113">Implementieren eines Video DSP-Plug-ins</span><span class="sxs-lookup"><span data-stu-id="ce6ef-113">Implementing a Video DSP Plug-in</span></span>

<span data-ttu-id="ce6ef-114">Computer-Videoanzeige Adapter unterstützen eine Reihe von Videoformaten.</span><span class="sxs-lookup"><span data-stu-id="ce6ef-114">Computer video display adapters support a set of video formats.</span></span> <span data-ttu-id="ce6ef-115">Digitale Video Codecs unterstützen auch eine Reihe von Videoformaten.</span><span class="sxs-lookup"><span data-stu-id="ce6ef-115">Digital video codecs also support a set of video formats.</span></span> <span data-ttu-id="ce6ef-116">Wenn Sie versuchen, eine bestimmte Videodatei wiederzugeben, muss Windows Media Player ein Format auswählen, das für das Rendering verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce6ef-116">When attempting to play a particular video file, Windows Media Player must choose a format to use for rendering.</span></span> <span data-ttu-id="ce6ef-117">Der Player versucht, die beste Übereinstimmung zwischen den vom Videocodec unterstützten Formaten und den vom Videoanzeige Adapter unterstützten Formaten zu finden, d. –. dem, der die höchste Qualität ergibt.</span><span class="sxs-lookup"><span data-stu-id="ce6ef-117">The Player attempts to find the best match between the formats supported by the video codec and the formats supported by the video display adapter—that is, the one that yields the highest quality.</span></span>

<span data-ttu-id="ce6ef-118">Um ein Windows Media Player DSP-Plug-in zu erstellen, das Video verarbeitet, müssen Sie zunächst entscheiden, welche Videoformate Sie für das Plug-in erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="ce6ef-118">To create a Windows Media Player DSP plug-in that processes video, you'll first need to decide which video formats you'd like your plug-in to process.</span></span> <span data-ttu-id="ce6ef-119">Das Beispiel-Video-DSP-Plug-in funktioniert mit den folgenden Videoformaten:</span><span class="sxs-lookup"><span data-stu-id="ce6ef-119">The sample video DSP plug-in works with the following video formats:</span></span>

-   <span data-ttu-id="ce6ef-120">NV12</span><span class="sxs-lookup"><span data-stu-id="ce6ef-120">NV12</span></span>
-   <span data-ttu-id="ce6ef-121">YV12</span><span class="sxs-lookup"><span data-stu-id="ce6ef-121">YV12</span></span>
-   <span data-ttu-id="ce6ef-122">Im YUY2</span><span class="sxs-lookup"><span data-stu-id="ce6ef-122">YUY2</span></span>
-   <span data-ttu-id="ce6ef-123">UYVY</span><span class="sxs-lookup"><span data-stu-id="ce6ef-123">UYVY</span></span>
-   <span data-ttu-id="ce6ef-124">RGB32</span><span class="sxs-lookup"><span data-stu-id="ce6ef-124">RGB32</span></span>
-   <span data-ttu-id="ce6ef-125">RGB24</span><span class="sxs-lookup"><span data-stu-id="ce6ef-125">RGB24</span></span>
-   <span data-ttu-id="ce6ef-126">RGB555</span><span class="sxs-lookup"><span data-stu-id="ce6ef-126">RGB555</span></span>
-   <span data-ttu-id="ce6ef-127">RGB565</span><span class="sxs-lookup"><span data-stu-id="ce6ef-127">RGB565</span></span>

<span data-ttu-id="ce6ef-128">Die Formate, die Sie für die Verarbeitung auswählen, werden Ihnen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce6ef-128">Which formats you choose to process is up to you.</span></span> <span data-ttu-id="ce6ef-129">Sie können Formate aus dem Plug-in-Beispiel entfernen, sodass Sie nicht länger unterstützt werden, und Sie können Code hinzufügen, um zusätzliche Formate zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="ce6ef-129">You can remove formats from the sample plug-in so that they aren't supported any longer and you can add code to process additional formats.</span></span>

<span data-ttu-id="ce6ef-130">Die folgenden Abschnitte enthalten zusätzliche Informationen, die Sie kennen sollten, bevor Sie Ihr eigenes Video DSP-Plug-in für Windows Media Player erstellen:</span><span class="sxs-lookup"><span data-stu-id="ce6ef-130">The following sections provide additional information you should know before creating your own video DSP plug-in for Windows Media Player:</span></span>

-   [<span data-ttu-id="ce6ef-131">Aushandlung des Video Formats im Beispiel-Video-DSP-Plug-in</span><span class="sxs-lookup"><span data-stu-id="ce6ef-131">Video Format Negotiation in the Sample Video DSP Plug-in</span></span>](video-format-negotiation-in-the-sample-video-dsp-plug-in.md)
-   [<span data-ttu-id="ce6ef-132">DoProcess Output im Beispiel-Video-DSP-Plug-in</span><span class="sxs-lookup"><span data-stu-id="ce6ef-132">DoProcessOutput in the Sample Video DSP Plug-in</span></span>](doprocessoutput-in-the-sample-video-dsp-plug-in.md)
-   [<span data-ttu-id="ce6ef-133">Verarbeiten des Videos</span><span class="sxs-lookup"><span data-stu-id="ce6ef-133">Processing the Video</span></span>](processing-the-video.md)

## <a name="related-topics"></a><span data-ttu-id="ce6ef-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce6ef-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce6ef-135">**Implementieren des DSP-Codes**</span><span class="sxs-lookup"><span data-stu-id="ce6ef-135">**Implementing Your DSP Code**</span></span>](implementing-your-dsp-code.md)
</dt> </dl>

 

 




