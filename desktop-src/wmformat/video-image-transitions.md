---
title: Video Bild Übergänge
description: Video Bild Übergänge
ms.assetid: 201ddbfb-567b-4893-b754-569f1e7d8466
keywords:
- Windows Media-Format-SDK, Video Bild Übergänge
- Advanced Systems Format (ASF), Video Bild Übergänge
- ASF (Advanced Systems Format), Video Bild Übergänge
- Video Bild Übergänge
- Windows Media Video 9 Abbild v2-Codec
- Codecs, Windows Media Video 9 Abbild v2-Codec
- Videostreams, Windows Media Video 9-Abbild v2-Codec
- Videostreams, Bild Übergänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfd02628a78196a73750c2c0ff6b9e9c3d6729c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036770"
---
# <a name="video-image-transitions"></a><span data-ttu-id="497ce-111">Video Bild Übergänge</span><span class="sxs-lookup"><span data-stu-id="497ce-111">Video Image Transitions</span></span>

<span data-ttu-id="497ce-112">Der Windows Media Video 9-Abbild v2-Codec animiert eine Reihe von Bildern, was zu einem Videostream führt.</span><span class="sxs-lookup"><span data-stu-id="497ce-112">The Windows Media Video 9 Image v2 codec animates a series of images, resulting in a video stream.</span></span> <span data-ttu-id="497ce-113">Der Codec kann zwei Abbilder gleichzeitig bearbeiten, diese miteinander kombinieren und einen Übergang von einem zum anderen entsprechend der von Ihnen bereitgestellten Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="497ce-113">The codec can manipulate two images at once, blending them together and creating a transition from one to the other according to the configuration you supply.</span></span> <span data-ttu-id="497ce-114">In diesem Abschnitt werden die unterstützten Übergänge und die erforderlichen Parameter beschrieben.</span><span class="sxs-lookup"><span data-stu-id="497ce-114">This section describes the supported transitions and the parameters they require.</span></span>

<span data-ttu-id="497ce-115">Die Übergänge sind in der folgenden Tabelle nach ihren globalen bezeichlern aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="497ce-115">The transitions are listed in the following table by their global identifiers.</span></span>



| <span data-ttu-id="497ce-116">Übergangs Bezeichner</span><span class="sxs-lookup"><span data-stu-id="497ce-116">Transition identifier</span></span>                                                                           | <span data-ttu-id="497ce-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="497ce-117">Description</span></span>                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="497ce-118">**WMT \_ Videoimage- \_ Übergangs \_ Bogen \_ Tie**</span><span class="sxs-lookup"><span data-stu-id="497ce-118">**WMT\_VIDEOIMAGE\_TRANSITION\_BOW\_TIE**</span></span>](wmt-videoimage-transition-bow-tie.md)              | <span data-ttu-id="497ce-119">Ein neues Bild wird in einer Reihe von Dreiecken auf gegenüberliegenden Seiten des Frames angezeigt.</span><span class="sxs-lookup"><span data-stu-id="497ce-119">New image is revealed in a set of triangles on opposite sides of the frame.</span></span>                                                                  |
| [<span data-ttu-id="497ce-120">**WMT \_ Videoimage- \_ Übergangs \_ Kreis**</span><span class="sxs-lookup"><span data-stu-id="497ce-120">**WMT\_VIDEOIMAGE\_TRANSITION\_CIRCLE**</span></span>](wmt-videoimage-transition-circle.md)                 | <span data-ttu-id="497ce-121">Ein neues Bild wird in einem Kreis angezeigt.</span><span class="sxs-lookup"><span data-stu-id="497ce-121">New image is revealed in a circle.</span></span>                                                                                                           |
| [<span data-ttu-id="497ce-122">**Kreuz Ausblenden des WMT- \_ Videobilds \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="497ce-122">**WMT\_VIDEOIMAGE\_TRANSITION\_CROSS\_FADE**</span></span>](wmt-videoimage-transition-cross-fade.md)        | <span data-ttu-id="497ce-123">Kein spezieller Übergang, die Blend-Koeffizienten der beiden Bilder bestimmen das Kreuz ausblenden (auflösen).</span><span class="sxs-lookup"><span data-stu-id="497ce-123">No special transition, the blend coefficients of the two images determine the cross-fade (dissolve).</span></span>                                         |
| [<span data-ttu-id="497ce-124">**Übergang von WMT \_ Videoimage \_ \_ Diagonal**</span><span class="sxs-lookup"><span data-stu-id="497ce-124">**WMT\_VIDEOIMAGE\_TRANSITION\_DIAGONAL**</span></span>](wmt-videoimage-transition-diagonal.md)             | <span data-ttu-id="497ce-125">Ein neues Bild wird entlang einer diagonalen Linie angezeigt, die in einer Ecke des Frames steht.</span><span class="sxs-lookup"><span data-stu-id="497ce-125">New image is revealed along a diagonal line originating in one corner of the frame.</span></span>                                                          |
| [<span data-ttu-id="497ce-126">**WMT \_ Videoimage- \_ Übergangs Raute \_**</span><span class="sxs-lookup"><span data-stu-id="497ce-126">**WMT\_VIDEOIMAGE\_TRANSITION\_DIAMOND**</span></span>](wmt-videoimage-transition-diamond.md)               | <span data-ttu-id="497ce-127">Ein neues Bild wird in einem Rautensymbol angezeigt.</span><span class="sxs-lookup"><span data-stu-id="497ce-127">New image is revealed in a diamond.</span></span>                                                                                                          |
| [<span data-ttu-id="497ce-128">**WMT \_ Videoimage \_ - \_ Übergang \_ in \_ Farbe ausblenden**</span><span class="sxs-lookup"><span data-stu-id="497ce-128">**WMT\_VIDEOIMAGE\_TRANSITION\_FADE\_TO\_COLOR**</span></span>](wmt-videoimage-transition-fade-to-color.md) | <span data-ttu-id="497ce-129">Löst von dem Bild bis zu einem Frame mit voll Tonfarbe auf.</span><span class="sxs-lookup"><span data-stu-id="497ce-129">Dissolves from the image to a frame of solid color.</span></span>                                                                                          |
| [<span data-ttu-id="497ce-130">**WMT \_ Videoimage- \_ Übergang mit \_ ausgefülltem \_ V**</span><span class="sxs-lookup"><span data-stu-id="497ce-130">**WMT\_VIDEOIMAGE\_TRANSITION\_FILLED\_V**</span></span>](wmt-videoimage-transition-filled-v.md)            | <span data-ttu-id="497ce-131">Ein neues Bild wird in einem Dreieck angezeigt, das von einer Seite des Frames stammt.</span><span class="sxs-lookup"><span data-stu-id="497ce-131">New image is revealed in a triangle originating from one side of the frame.</span></span>                                                                  |
| [<span data-ttu-id="497ce-132">**WMT \_ Videoimage- \_ Übergang \_ kippen**</span><span class="sxs-lookup"><span data-stu-id="497ce-132">**WMT\_VIDEOIMAGE\_TRANSITION\_FLIP**</span></span>](wmt-videoimage-transition-flip.md)                     | <span data-ttu-id="497ce-133">Das alte Bild wird auf einer y-Achse durch die Mitte des Frames gedreht.</span><span class="sxs-lookup"><span data-stu-id="497ce-133">Old image is rotated on a y-axis through the center of the frame.</span></span> <span data-ttu-id="497ce-134">Das neue Bild wird als Rückseite des alten Bilds angezeigt.</span><span class="sxs-lookup"><span data-stu-id="497ce-134">The new image is revealed as the back of the old image.</span></span>                    |
| [<span data-ttu-id="497ce-135">**WMT \_ Videoimage- \_ Übergangs \_ inmenge**</span><span class="sxs-lookup"><span data-stu-id="497ce-135">**WMT\_VIDEOIMAGE\_TRANSITION\_INSET**</span></span>](wmt-videoimage-transition-inset.md)                   | <span data-ttu-id="497ce-136">Ein neues Bild wird durch ein Rechteck angezeigt, das aus einer Ecke des Frames stammt.</span><span class="sxs-lookup"><span data-stu-id="497ce-136">New image is revealed by a rectangle originating from one corner of the frame.</span></span>                                                               |
| [<span data-ttu-id="497ce-137">**WMT \_ Videoimage- \_ Übergangs \_ IRIS**</span><span class="sxs-lookup"><span data-stu-id="497ce-137">**WMT\_VIDEOIMAGE\_TRANSITION\_IRIS**</span></span>](wmt-videoimage-transition-iris.md)                     | <span data-ttu-id="497ce-138">Ein neues Bild wird auf einer x-Achse und einer y-Achse angezeigt.</span><span class="sxs-lookup"><span data-stu-id="497ce-138">New image is revealed along an x-axis and a y-axis.</span></span>                                                                                          |
| [<span data-ttu-id="497ce-139">**WMT \_ Videoimage- \_ Übergangs \_ Seite \_ (Rollup)**</span><span class="sxs-lookup"><span data-stu-id="497ce-139">**WMT\_VIDEOIMAGE\_TRANSITION\_PAGE\_ROLL**</span></span>](wmt-videoimage-transition-page-roll.md)          | <span data-ttu-id="497ce-140">Das alte Bild wird in einem Seiten flippingeffekt transformiert und zeigt das neue Bild darunter.</span><span class="sxs-lookup"><span data-stu-id="497ce-140">Old image is transformed in a page-flipping effect, revealing the new image underneath.</span></span>                                                      |
| [<span data-ttu-id="497ce-141">**WMT \_ Videoimage- \_ Übergangs \_ Rechteck**</span><span class="sxs-lookup"><span data-stu-id="497ce-141">**WMT\_VIDEOIMAGE\_TRANSITION\_RECTANGLE**</span></span>](wmt-videoimage-transition-rectangle.md)           | <span data-ttu-id="497ce-142">Ein neues Bild wird durch ein Rechteck innerhalb des Frames angezeigt.</span><span class="sxs-lookup"><span data-stu-id="497ce-142">New image is revealed by a rectangle within the frame.</span></span>                                                                                       |
| [<span data-ttu-id="497ce-143">**WMT \_ Videoimage- \_ Übergang \_ offenlegen**</span><span class="sxs-lookup"><span data-stu-id="497ce-143">**WMT\_VIDEOIMAGE\_TRANSITION\_REVEAL**</span></span>](wmt-videoimage-transition-reveal.md)                 | <span data-ttu-id="497ce-144">Ein neues Bild wird an einer geraden Linie angezeigt, die von einer Seite des Frames stammt.</span><span class="sxs-lookup"><span data-stu-id="497ce-144">New image is revealed along a straight line originating from one side of the frame.</span></span>                                                          |
| [<span data-ttu-id="497ce-145">**Folie für WMT \_ Videoimage- \_ Übergang \_**</span><span class="sxs-lookup"><span data-stu-id="497ce-145">**WMT\_VIDEOIMAGE\_TRANSITION\_SLIDE**</span></span>](wmt-videoimage-transition-slide.md)                   | <span data-ttu-id="497ce-146">Das alte Bild wird aus dem Frame heraus bewegt und zeigt das neue Bild unterhalb an.</span><span class="sxs-lookup"><span data-stu-id="497ce-146">Old image slides out of the frame, revealing the new image underneath.</span></span>                                                                       |
| [<span data-ttu-id="497ce-147">**Teilung des WMT \_ Videoimage- \_ Übergangs \_**</span><span class="sxs-lookup"><span data-stu-id="497ce-147">**WMT\_VIDEOIMAGE\_TRANSITION\_SPLIT**</span></span>](wmt-videoimage-transition-split.md)                   | <span data-ttu-id="497ce-148">Ein neues Bild wird durch eine horizontale oder vertikale Aufteilung im alten Bild angezeigt.</span><span class="sxs-lookup"><span data-stu-id="497ce-148">New image is revealed by a horizontal or vertical split in the old image.</span></span> <span data-ttu-id="497ce-149">Die Teilung wird entlang einer geraden Linie angezeigt, beginnend innerhalb des Frames.</span><span class="sxs-lookup"><span data-stu-id="497ce-149">The split appears along a straight line starting inside the frame.</span></span> |
| [<span data-ttu-id="497ce-150">**WMT \_ Videoimage \_ \_ -Übergangs Stern**</span><span class="sxs-lookup"><span data-stu-id="497ce-150">**WMT\_VIDEOIMAGE\_TRANSITION\_STAR**</span></span>](wmt-videoimage-transition-star.md)                     | <span data-ttu-id="497ce-151">Ein neues Bild wird von einem fünf-Spitze-Stern innerhalb des Frames angezeigt.</span><span class="sxs-lookup"><span data-stu-id="497ce-151">New image is revealed by a five-pointed star inside the frame.</span></span>                                                                               |
| [<span data-ttu-id="497ce-152">**WMT \_ Videoimage- \_ Übergangs \_ Rad**</span><span class="sxs-lookup"><span data-stu-id="497ce-152">**WMT\_VIDEOIMAGE\_TRANSITION\_WHEEL**</span></span>](wmt-videoimage-transition-wheel.md)                   | <span data-ttu-id="497ce-153">Ein neues Bild wird von vier rotierenden Spokes mit einem gemeinsamen Pivotpunkt offengelegt.</span><span class="sxs-lookup"><span data-stu-id="497ce-153">New image is revealed by four rotating spokes with a common pivot point.</span></span>                                                                     |



 

<span data-ttu-id="497ce-154">Jeder Übergang wird in einem eigenen Thema ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="497ce-154">Each transition is fully described in its own topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="497ce-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="497ce-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="497ce-156">**Programmierverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="497ce-156">**Programming Reference**</span></span>](programming-reference.md)
</dt> <dt>

[<span data-ttu-id="497ce-157">**WMT \_ Videoimage \_ SAMPLE2**</span><span class="sxs-lookup"><span data-stu-id="497ce-157">**WMT\_VIDEOIMAGE\_SAMPLE2**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)
</dt> </dl>

 

 




