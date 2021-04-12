---
title: So lesen und schreiben Sie Videostreams mit nicht quadratischen Pixeln
description: So lesen und schreiben Sie Videostreams mit nicht quadratischen Pixeln
ms.assetid: fe66d13e-61cf-4bb6-9ca2-aafeabe320ec
keywords:
- Windows Media-Format-SDK, Lesen von Videostreams
- Windows Media-Format-SDK, Schreiben von Videostreams
- Windows Media-Format-SDK, Videostreams
- Windows Media-Format-SDK, nicht eckige Pixel
- Windows Media-Format-SDK, Pixel (ohne Quadrat)
- Advanced Systems Format (ASF), Lesen von Videostreams
- ASF (Advanced Systems Format), Lesen von Videostreams
- Advanced Systems Format (ASF), Schreiben von Videostreams
- ASF (Advanced Systems Format), Schreiben von Videostreams
- Advanced Systems Format (ASF), Videostreams
- ASF (Advanced Systems Format), Videostreams
- Advanced Systems Format (ASF), nicht quadratische Pixel
- ASF (Advanced Systems Format), nicht eckige Pixel
- Advanced Systems Format (ASF), Pixel (ohne Quadrat)
- ASF (Advanced Systems Format), Pixel (ohne Quadrat)
- Lesen von Videostreams
- Schreiben von Videostreams
- Videostreams, lesen
- Videostreams, schreiben
- Videostreams, nicht quadratische Pixel
- nicht quadratische Pixel
- Pixel (nicht quadratisch)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6b3e3ba67ba42dfc144e7f95ddd042dea0f84
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309927"
---
# <a name="to-read-and-write-video-streams-with-non-square-pixels"></a><span data-ttu-id="35b75-125">So lesen und schreiben Sie Videostreams mit nicht quadratischen Pixeln</span><span class="sxs-lookup"><span data-stu-id="35b75-125">To Read and Write Video Streams with Non-Square Pixels</span></span>

<span data-ttu-id="35b75-126">Computer Monitore haben Quadrat Pixel, aber andere Arten von Video Bildschirmen, einschließlich NTSC-Fernsehgeräten, haben rechteckige oder nicht eckige Pixel.</span><span class="sxs-lookup"><span data-stu-id="35b75-126">Computer monitors have square pixels, but other types of video screens, including NTSC televisions, have rectangular or non-square pixels.</span></span> <span data-ttu-id="35b75-127">Außerdem haben einige Eingabegeräte, z. b. "digitale Video (DV)", mehrere Geräte mit nicht quadratischen Pixeln abgerechnet.</span><span class="sxs-lookup"><span data-stu-id="35b75-127">Also, some input devices, such as Digital Video (DV) cameras, have charged couple devices with non-square pixels.</span></span> <span data-ttu-id="35b75-128">Wenn Sie Dateien schreiben, die entweder auf nicht quadratischen Pixel-Quelldaten basieren oder anderweitig für die Anzeige auf Geräten mit nicht quadratischen Pixeln vorgesehen sind, müssen die Pixel Seitenverhältnis-Informationen in der ASF-Datei enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="35b75-128">When you are writing files that are either based on non-square pixel source data or else intended for display on devices with non-square pixels, the pixel aspect ratio information must be included in the ASF file.</span></span> <span data-ttu-id="35b75-129">Leser Anwendungen müssen diese Informationen überprüfen und verwenden, um das Seitenverhältnis des Video Rechtecks nach Bedarf anzupassen.</span><span class="sxs-lookup"><span data-stu-id="35b75-129">Reader applications must examine that information and use it to adjust the aspect ratio of the video rectangle as necessary.</span></span>

## <a name="related-topics"></a><span data-ttu-id="35b75-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="35b75-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35b75-131">**Erweiterte Themen**</span><span class="sxs-lookup"><span data-stu-id="35b75-131">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="35b75-132">**Lesen von Streams mit nicht quadratischen Pixeln**</span><span class="sxs-lookup"><span data-stu-id="35b75-132">**Reading Streams with Non-Square Pixels**</span></span>](reading-streams-with-non-square-pixels.md)
</dt> <dt>

[<span data-ttu-id="35b75-133">**Schreiben von Streams mit nicht quadratischen Pixeln**</span><span class="sxs-lookup"><span data-stu-id="35b75-133">**Writing Streams with Non-Square Pixels**</span></span>](writing-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




