---
title: Informationen zum Beispiel-Video-DSP-Plug-in
description: Informationen zum Beispiel-Video-DSP-Plug-in
ms.assetid: f2ba8e9d-a0e4-4679-99dc-2bfe9e451ffd
keywords:
- Windows Media Player-Plug-ins, Beispiele
- Plug-ins, Beispiele
- Plug-Ins für die digitale Signalverarbeitung, Beispiele
- DSP-Plug-ins, Beispiele
- Windows Media Player-Plug-ins, videodsp
- Plug-ins, videodsp
- Plug-Ins für die digitale Signalverarbeitung, Videobeispiele
- DSP-Plug-ins, Videobeispiele
- Beispiele, DSP-Plug-ins
- Video DSP-Plug-ins, Beispiele
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ede2eda82c834cefad0e31009805f24941cd4a6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338161"
---
# <a name="about-the-sample-video-dsp-plug-in"></a><span data-ttu-id="c6eef-113">Informationen zum Beispiel-Video-DSP-Plug-in</span><span class="sxs-lookup"><span data-stu-id="c6eef-113">About the Sample Video DSP Plug-in</span></span>

<span data-ttu-id="c6eef-114">Das Beispiel-Video-DSP-Plug-in bietet eine einfache Verarbeitungs Implementierung, die die Farbsättigung des Videos um einen vom Benutzer auf der Eigenschaften Seite bereitgestellten Faktor skaliert.</span><span class="sxs-lookup"><span data-stu-id="c6eef-114">The sample video DSP plug-in provides a simple processing implementation that scales the color saturation of the video by a factor provided by the user in the property page.</span></span> <span data-ttu-id="c6eef-115">Das Plug-in akzeptiert Werte zwischen 0 (null) und 1.</span><span class="sxs-lookup"><span data-stu-id="c6eef-115">The plug-in accepts values between zero and 1.</span></span> <span data-ttu-id="c6eef-116">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="c6eef-116">The default value is 1.</span></span> <span data-ttu-id="c6eef-117">Der Wert 1 hat keine Auswirkung auf das Videobild. andere Skalierungsfaktoren desättizieren die Bildfarbe.</span><span class="sxs-lookup"><span data-stu-id="c6eef-117">A value of 1 has no effect upon the video image; other scale factors desaturate the image color.</span></span> <span data-ttu-id="c6eef-118">Beispielsweise ergibt der Wert 0,5 eine Farbsättigung von 50%.</span><span class="sxs-lookup"><span data-stu-id="c6eef-118">For instance, a value of .5 would result in 50 percent color saturation.</span></span> <span data-ttu-id="c6eef-119">Der Wert 0 (null) führt zu Graustufen Videos.</span><span class="sxs-lookup"><span data-stu-id="c6eef-119">A value of zero results in grayscale video.</span></span>

<span data-ttu-id="c6eef-120">Das Beispiel-Video-DSP-Plug-in funktioniert mit den folgenden Videoformaten:</span><span class="sxs-lookup"><span data-stu-id="c6eef-120">The sample video DSP plug-in works with the following video formats:</span></span>

-   <span data-ttu-id="c6eef-121">NV12</span><span class="sxs-lookup"><span data-stu-id="c6eef-121">NV12</span></span>
-   <span data-ttu-id="c6eef-122">YV12</span><span class="sxs-lookup"><span data-stu-id="c6eef-122">YV12</span></span>
-   <span data-ttu-id="c6eef-123">Im YUY2</span><span class="sxs-lookup"><span data-stu-id="c6eef-123">YUY2</span></span>
-   <span data-ttu-id="c6eef-124">UYVY</span><span class="sxs-lookup"><span data-stu-id="c6eef-124">UYVY</span></span>
-   <span data-ttu-id="c6eef-125">RGB32</span><span class="sxs-lookup"><span data-stu-id="c6eef-125">RGB32</span></span>
-   <span data-ttu-id="c6eef-126">RGB24</span><span class="sxs-lookup"><span data-stu-id="c6eef-126">RGB24</span></span>
-   <span data-ttu-id="c6eef-127">RGB555</span><span class="sxs-lookup"><span data-stu-id="c6eef-127">RGB555</span></span>
-   <span data-ttu-id="c6eef-128">RGB565</span><span class="sxs-lookup"><span data-stu-id="c6eef-128">RGB565</span></span>

## <a name="related-topics"></a><span data-ttu-id="c6eef-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c6eef-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6eef-130">**Aufbau eines DSP-Plug-ins**</span><span class="sxs-lookup"><span data-stu-id="c6eef-130">**Building a DSP Plug-in**</span></span>](building-a-dsp-plug-in.md)
</dt> </dl>

 

 




