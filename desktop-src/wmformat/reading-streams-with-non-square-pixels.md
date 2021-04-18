---
title: Lesen von Streams mit nicht quadratischen Pixeln
description: Lesen von Streams mit nicht quadratischen Pixeln
ms.assetid: 32114c81-cb78-43de-9ea7-f210056f5aab
keywords:
- Windows Media-Format-SDK, Lesen von Videostreams
- Windows Media-Format-SDK, Videostreams
- Windows Media-Format-SDK, nicht eckige Pixel
- Windows Media-Format-SDK, Pixel (ohne Quadrat)
- Advanced Systems Format (ASF), Lesen von Videostreams
- ASF (Advanced Systems Format), Lesen von Videostreams
- Advanced Systems Format (ASF), Videostreams
- ASF (Advanced Systems Format), Videostreams
- Advanced Systems Format (ASF), nicht quadratische Pixel
- ASF (Advanced Systems Format), nicht eckige Pixel
- Advanced Systems Format (ASF), Pixel (ohne Quadrat)
- ASF (Advanced Systems Format), Pixel (ohne Quadrat)
- Lesen von Videostreams
- Videostreams, lesen
- Videostreams, nicht quadratische Pixel
- nicht quadratische Pixel
- Pixel (nicht quadratisch)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfc14019e9822aefedb7600adc4209317293b2f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338223"
---
# <a name="reading-streams-with-non-square-pixels"></a><span data-ttu-id="5791b-120">Lesen von Streams mit nicht quadratischen Pixeln</span><span class="sxs-lookup"><span data-stu-id="5791b-120">Reading Streams with Non-Square Pixels</span></span>

<span data-ttu-id="5791b-121">Reader-Anwendungen, die nicht quadratische Pixel ordnungsgemäß verarbeiten müssen, sollten sowohl die Attribute auf Streamebene im ASF-Header als auch die Dateneinheiten Erweiterungen in jedem Beispiel untersuchen.</span><span class="sxs-lookup"><span data-stu-id="5791b-121">Reader applications that need to correctly handle non-square pixels should examine both the stream-level attributes in the ASF header and the data unit extensions on each sample.</span></span> <span data-ttu-id="5791b-122">Es gibt zwei Fälle, in denen das Ausgabe Rechteck so angepasst werden muss, dass es nicht quadratische Pixel kompensiert.</span><span class="sxs-lookup"><span data-stu-id="5791b-122">There are two cases when the output rectangle must be adjusted to compensate for non-square pixels.</span></span>

<span data-ttu-id="5791b-123">Wenn der Quell Inhalt von einem Gerät, wie z. b. einer DV-Kamera (Digital Video), mit nicht quadratischen Pixeln in seinem CCD aufgezeichnet wurde, muss eine Reader-Anwendung das Videoausgabe Rechteck anpassen, damit das Bild auf einem Computermonitor mit quadratischen Pixeln ordnungsgemäß angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5791b-123">When the source content has been captured from a device such as a DV (digital video) camera with non-square pixels in its CCD, a reader application must adjust its video output rectangle so that the image displays correctly on a computer monitor with square pixels.</span></span>

<span data-ttu-id="5791b-124">Wenn die Reader-Anwendung Videos ausgibt, die auf einem NTSC-Fernsehgerät wiedergegeben werden, z. b. über eine e-Video-out-Verbindung auf der Grafikkarte, müssen Sie das Video Rechteck anpassen, damit das Bild auf den nicht quadratischen Pixeln des Fernseh ERS ordnungsgemäß angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="5791b-124">When your reader application outputs video that will be played back on an NTSC television, for example through an S-Video out connection on the video card, you must adjust the video rectangle so that the image displays correctly on the television's non-square pixels.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5791b-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5791b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5791b-126">**So lesen und schreiben Sie Videostreams mit nicht quadratischen Pixeln**</span><span class="sxs-lookup"><span data-stu-id="5791b-126">**To Read and Write Video Streams with Non-Square Pixels**</span></span>](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




