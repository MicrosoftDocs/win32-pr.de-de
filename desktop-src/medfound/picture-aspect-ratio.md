---
description: In diesem Thema werden zwei verwandte Konzepte, das Bildseiten Verhältnis und das Pixel Seitenverhältnis beschrieben.
ms.assetid: 384bdeaa-5360-42af-9f95-b791af2dcafc
title: Bildseiten Verhältnis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e81f1b8e26af753a5c8c1bc7ecb09d8a658582
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215020"
---
# <a name="picture-aspect-ratio"></a><span data-ttu-id="bfdbe-103">Bildseiten Verhältnis</span><span class="sxs-lookup"><span data-stu-id="bfdbe-103">Picture Aspect Ratio</span></span>

<span data-ttu-id="bfdbe-104">In diesem Thema werden zwei verwandte Konzepte, das Bildseiten Verhältnis und das Pixel Seitenverhältnis beschrieben.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-104">This topic describes two related concepts, picture aspect ratio and pixel aspect ratio.</span></span> <span data-ttu-id="bfdbe-105">Anschließend wird beschrieben, wie diese Konzepte in Microsoft Media Foundation mithilfe von Medientypen ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-105">It then describes how these concepts are expressed in Microsoft Media Foundation using media types.</span></span>

-   [<span data-ttu-id="bfdbe-106">Bildseiten Verhältnis</span><span class="sxs-lookup"><span data-stu-id="bfdbe-106">Picture Aspect Ratio</span></span>](#picture-aspect-ratio)
    -   [<span data-ttu-id="bfdbe-107">Letterbox</span><span class="sxs-lookup"><span data-stu-id="bfdbe-107">Letterboxing</span></span>](#letterboxing)
    -   [<span data-ttu-id="bfdbe-108">Schwenken und überprüfen</span><span class="sxs-lookup"><span data-stu-id="bfdbe-108">Pan-and-Scan</span></span>](#pan-and-scan)
-   [<span data-ttu-id="bfdbe-109">Pixel Seitenverhältnis</span><span class="sxs-lookup"><span data-stu-id="bfdbe-109">Pixel Aspect Ratio</span></span>](#pixel-aspect-ratio)
-   [<span data-ttu-id="bfdbe-110">Arbeiten mit Seitenverhältnissen</span><span class="sxs-lookup"><span data-stu-id="bfdbe-110">Working with Aspect Ratios</span></span>](#working-with-aspect-ratios)
-   [<span data-ttu-id="bfdbe-111">Code Beispiele</span><span class="sxs-lookup"><span data-stu-id="bfdbe-111">Code Examples</span></span>](#code-examples)
    -   [<span data-ttu-id="bfdbe-112">Suchen des Anzeige Bereichs</span><span class="sxs-lookup"><span data-stu-id="bfdbe-112">Finding the Display Area</span></span>](#finding-the-display-area)
    -   [<span data-ttu-id="bfdbe-113">Zwischen Pixel-Seitenverhältnissen</span><span class="sxs-lookup"><span data-stu-id="bfdbe-113">Converting Between Pixel Aspect Ratios</span></span>](#converting-between-pixel-aspect-ratios)
    -   [<span data-ttu-id="bfdbe-114">Berechnen des Bereichs "Briefkasten"</span><span class="sxs-lookup"><span data-stu-id="bfdbe-114">Calculating the Letterbox Area</span></span>](#calculating-the-letterbox-area)
-   [<span data-ttu-id="bfdbe-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bfdbe-115">Related topics</span></span>](#related-topics)

## <a name="picture-aspect-ratio"></a><span data-ttu-id="bfdbe-116">Bildseiten Verhältnis</span><span class="sxs-lookup"><span data-stu-id="bfdbe-116">Picture Aspect Ratio</span></span>

<span data-ttu-id="bfdbe-117">*Bildseiten Verhältnis* definiert die Form des angezeigten Video Bilds.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-117">*Picture aspect ratio* defines the shape of the displayed video image.</span></span> <span data-ttu-id="bfdbe-118">Das Seitenverhältnis des Bilds ist als "x:y" gekennzeichnet, wobei "x:y" das Verhältnis der Bildbreite zur Bildhöhe ist.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-118">Picture aspect ratio is notated X:Y, where X:Y is the ratio of picture width to picture height.</span></span> <span data-ttu-id="bfdbe-119">Bei den meisten Videostandards wird das Seitenverhältnis von 4:3 oder 16:9 verwendet.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-119">Most video standards use either 4:3 or 16:9 picture aspect ratio.</span></span> <span data-ttu-id="bfdbe-120">Das 16:9-Seitenverhältnis wird häufig als " *Breitbild*" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-120">The 16:9 aspect ratio is commonly called *widescreen*.</span></span> <span data-ttu-id="bfdbe-121">Der Kino Film verwendet häufig ein Seitenverhältnis von 1:85:1 oder 1:66:1.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-121">Cinema film often uses a 1:85:1 or 1:66:1 aspect ratio.</span></span> <span data-ttu-id="bfdbe-122">Das Seitenverhältnis des Bilds wird auch als *Seitenverhältnis anzeigen* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-122">Picture aspect ratio is also called *display aspect ratio* (DAR).</span></span>

![Diagramm, das 4:3-und 16:9-Seitenverhältnisse anzeigt](images/aspect-ratio01.png)

<span data-ttu-id="bfdbe-124">Manchmal hat das Video Bild nicht dieselbe Form wie der Anzeigebereich.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-124">Sometimes the video image does not have the same shape as the display area.</span></span> <span data-ttu-id="bfdbe-125">Beispielsweise kann ein 4:3-Video in einem Breitbild (16 × 9) angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-125">For example, a 4:3 video might be shown on a widescreen (16×9) television.</span></span> <span data-ttu-id="bfdbe-126">In Computer Videos wird das Video möglicherweise in einem Fenster angezeigt, das eine beliebige Größe aufweist.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-126">In computer video, the video might be shown inside a window that has an arbitrary size.</span></span> <span data-ttu-id="bfdbe-127">In diesem Fall gibt es drei Möglichkeiten, wie das Bild im Anzeigebereich angepasst werden kann:</span><span class="sxs-lookup"><span data-stu-id="bfdbe-127">In that case, there are three ways the image can be made to fit within the display area:</span></span>

-   <span data-ttu-id="bfdbe-128">Strecken Sie das Bild entlang einer Achse, sodass es an den Anzeigebereich angepasst ist.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-128">Stretch the image along one axis to fit the display area.</span></span>
-   <span data-ttu-id="bfdbe-129">Skalieren Sie das Bild so, dass es in den Anzeigebereich passt, während Sie das ursprüngliche Bildseiten Verhältnis beibehalten.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-129">Scale the image to fit the display area, while maintaining the original picture aspect ratio.</span></span>
-   <span data-ttu-id="bfdbe-130">Zuschneiden des Bilds.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-130">Crop the image.</span></span>

<span data-ttu-id="bfdbe-131">Das Strecken des Bilds an den Anzeigebereich ist fast immer falsch, da es das richtige Bildseiten Verhältnis nicht beibehält.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-131">Stretching the image to fit the display area is almost always wrong, because it does not preserve the correct picture aspect ratio.</span></span>

### <a name="letterboxing"></a><span data-ttu-id="bfdbe-132">Letterbox</span><span class="sxs-lookup"><span data-stu-id="bfdbe-132">Letterboxing</span></span>

<span data-ttu-id="bfdbe-133">Der Prozess der Skalierung eines Bildschirm Bilds an eine 4:3-Anzeige wird im nächsten Diagramm als *Letterbox* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-133">The process of scaling a widescreen image to fit a 4:3 display is called *letterboxing*, shown in the next diagram.</span></span> <span data-ttu-id="bfdbe-134">Die resultierenden rechteckigen Bereiche am oberen und unteren Rand des Bilds sind in der Regel mit schwarz gefüllt, auch wenn andere Farben verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-134">The resulting rectanglular areas at the top and bottom of the image are typically filled with black, although other colors can be used.</span></span>

![Diagramm mit der korrekten Methode zum Briefkasten](images/aspect-ratio02.png)

<span data-ttu-id="bfdbe-136">Der umgekehrte Fall, das Skalieren eines 4:3-Bilds an eine Bildschirm Abbildung zeigt, wird manchmal als *Pillarboxing* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-136">The reverse case, scaling a 4:3 image to fit a widescreen display, is sometimes called *pillarboxing*.</span></span> <span data-ttu-id="bfdbe-137">Der Begriff " *Letterbox* " wird jedoch auch allgemein verwendet, um ein Video Bild so zu skalieren, dass es an einen beliebigen Anzeigebereich angepasst wird.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-137">However, the term *letterbox* is also used in a general sense, to mean scaling a video image to fit any given display area.</span></span>

![Diagramm mit Pillarboxing](images/aspect-ratio03.png)

### <a name="pan-and-scan"></a><span data-ttu-id="bfdbe-139">Schwenken und überprüfen</span><span class="sxs-lookup"><span data-stu-id="bfdbe-139">Pan-and-Scan</span></span>

<span data-ttu-id="bfdbe-140">"Pan-and-Scan" ist ein Verfahren, bei dem ein Breitbild auf einen vier × 3-rechteckigen Bereich zugeschnitten wird, um auf einem 4:3-Display Gerät angezeigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-140">Pan-and-scan is a technique whereby a widescreen image is cropped to a 4×3 rectangular area, for display on a 4:3 display device.</span></span> <span data-ttu-id="bfdbe-141">Das resultierende Bild füllt die gesamte Anzeige aus, ohne dass schwarze Letterbox-Bereiche erforderlich sind, aber Teile des ursprünglichen Bilds werden aus dem Bild herausgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-141">The resulting image fills the entire display, without requiring black letterbox areas, but portions of the original image are cropped out of the picture.</span></span> <span data-ttu-id="bfdbe-142">Der Bereich, der zugeschnitten wird, kann sich von Frame zu Frame bewegen, während sich der Bereich des Interesses verschiebt.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-142">The area that is cropped can move from frame to frame, as the area of interest shifts.</span></span> <span data-ttu-id="bfdbe-143">Der Begriff "Pan" in "Pan *-and-Scan* " bezieht sich auf den Schwenk Effekt, der durch das Verschieben des Bereichs "schwenken" und "Scannen" verursacht wird.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-143">The term "pan" in *pan-and-scan* refers to the panning effect that is caused by moving the pan-and-scan area.</span></span>

![Diagramm mit Pan-and-Scan](images/aspect-ratio04.png)

## <a name="pixel-aspect-ratio"></a><span data-ttu-id="bfdbe-145">Pixel Seitenverhältnis</span><span class="sxs-lookup"><span data-stu-id="bfdbe-145">Pixel Aspect Ratio</span></span>

<span data-ttu-id="bfdbe-146">*Pixel Seitenverhältnis* (par) misst die Form eines Pixels.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-146">*Pixel aspect ratio* (PAR) measures the shape of a pixel.</span></span>

<span data-ttu-id="bfdbe-147">Wenn ein digitales Bild aufgezeichnet wird, wird das Bild sowohl vertikal als auch horizontal entnommen. Dies führt zu einem rechteckigen Array von quantifizierten Beispielen, die als *Pixel* oder *Pels* bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-147">When a digital image is captured, the image is sampled both vertically and horizontally, resulting in a rectangular array of quantized samples, called *pixels* or *pels*.</span></span> <span data-ttu-id="bfdbe-148">Die Form des Stichproben Rasters bestimmt die Form der Pixel im digitalisierten Bild.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-148">The shape of the sampling grid determines the shape of the pixels in the digitized image.</span></span>

<span data-ttu-id="bfdbe-149">Im folgenden finden Sie ein Beispiel, in dem kleine Zahlen verwendet werden, um die mathematische Mathematik beizubehalten.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-149">Here is an example that uses small numbers to keep the math simple.</span></span> <span data-ttu-id="bfdbe-150">Angenommen, das ursprüngliche Bild ist quadratisch (das Bildseiten Verhältnis ist 1:1); angenommen, das Stichproben Raster enthält 12 Elemente, die in einem 4 × 3-Raster angeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-150">Suppose that the original image is square (that is, the picture aspect ratio is 1:1); and suppose the sampling grid contains 12 elements, arranged in a 4×3 grid.</span></span> <span data-ttu-id="bfdbe-151">Die Form jedes resultierenden Pixels ist größer als die Breite.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-151">The shape of each resulting pixel will be taller than it is wide.</span></span> <span data-ttu-id="bfdbe-152">Insbesondere ist die Form jedes Pixels 3 × 4.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-152">Specifically, the shape of each pixel will be 3×4.</span></span> <span data-ttu-id="bfdbe-153">Pixel, die nicht quadratisch sind, werden als *nicht quadratische Pixel* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-153">Pixels that are not square are called *non-square pixels*.</span></span>

![Diagramm mit einem nicht quadratischen Stichproben Raster](images/aspect-ratio05.png)

<span data-ttu-id="bfdbe-155">Das Pixel Seitenverhältnis gilt auch für das Anzeigegerät.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-155">Pixel aspect ratio also applies to the display device.</span></span> <span data-ttu-id="bfdbe-156">Die physische Form des Anzeige Geräts und die Auflösung des physischen Pixels (über-und Abgleich) bestimmen das par des Anzeige Geräts.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-156">The physical shape of the display device and the physical pixel resolution (across and down) determine the PAR of the display device.</span></span> <span data-ttu-id="bfdbe-157">Computer Monitore verwenden im allgemeinen quadratische Pixel.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-157">Computer monitors generally use square pixels.</span></span> <span data-ttu-id="bfdbe-158">Wenn das Bild par und das Anzeige-par nicht übereinstimmen, muss das Bild in einer Dimension, entweder vertikal oder horizontal, skaliert werden, damit es ordnungsgemäß angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-158">If the image PAR and the display PAR do not match, the image must be scaled in one dimension, either vertically or horizontally, in order to display correctly.</span></span> <span data-ttu-id="bfdbe-159">Die folgende Formel bezieht sich auf par, das Anzeige Seitenverhältnis (dar) und die Bildgröße in Pixel:</span><span class="sxs-lookup"><span data-stu-id="bfdbe-159">The following formula relates PAR, display aspect ratio (DAR), and image size in pixels:</span></span>

<span data-ttu-id="bfdbe-160">*Dar* = (*Bildbreite in Pixel*  /  *Bildhöhe in Pixel*) × *par*</span><span class="sxs-lookup"><span data-stu-id="bfdbe-160">*DAR* = (*image width in pixels* / *image height in pixels*) × *PAR*</span></span>

<span data-ttu-id="bfdbe-161">Beachten Sie, dass Bildbreite und Bildhöhe in dieser Formel auf das Bild im Speicher verweisen, nicht auf das angezeigte Bild.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-161">Note that image width and image height in this formula refer to the image in memory, not the displayed image.</span></span>

<span data-ttu-id="bfdbe-162">Im folgenden finden Sie ein Beispiel für eine reale Darstellung: NTSC-M-Analog Video enthält 480-Scan Zeilen im aktiven Bildbereich.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-162">Here is a real-world example: NTSC-M analog video contains 480 scan lines in the active image area.</span></span> <span data-ttu-id="bfdbe-163">"ITU-R Rec. BT. 601" gibt eine horizontale Samplingrate von 704 sichtbaren Pixeln pro Zeile an und ergibt ein digitales Bild mit 704 x 480 Pixeln.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-163">ITU-R Rec. BT.601 specifies a horizontal sampling rate of 704 visible pixels per line, yielding a digital image with 704 x 480 pixels.</span></span> <span data-ttu-id="bfdbe-164">Das gewünschte Bildseiten Verhältnis ist 4:3 und ergibt ein par von 10:11.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-164">The intended picture aspect ratio is 4:3, yielding a PAR of 10:11.</span></span>

-   <span data-ttu-id="bfdbe-165">DAR: 4:3</span><span class="sxs-lookup"><span data-stu-id="bfdbe-165">DAR: 4:3</span></span>
-   <span data-ttu-id="bfdbe-166">Breite in Pixel: 704</span><span class="sxs-lookup"><span data-stu-id="bfdbe-166">Width in pixels: 704</span></span>
-   <span data-ttu-id="bfdbe-167">Höhe in Pixel: 480</span><span class="sxs-lookup"><span data-stu-id="bfdbe-167">Height in pixels: 480</span></span>
-   <span data-ttu-id="bfdbe-168">Par: 10/11</span><span class="sxs-lookup"><span data-stu-id="bfdbe-168">PAR: 10/11</span></span>

<span data-ttu-id="bfdbe-169">4/3 = (704/420) x (10/11)</span><span class="sxs-lookup"><span data-stu-id="bfdbe-169">4/3 = (704/420) x (10/11)</span></span>

<span data-ttu-id="bfdbe-170">Um dieses Bild ordnungsgemäß auf einem Anzeigegerät mit quadratischen Pixeln anzuzeigen, müssen Sie entweder die Breite um 10/11 oder die Höhe um 11/10 skalieren.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-170">To display this image correctly on a display device with square pixels, you must scale either the width by 10/11 or the height by 11/10.</span></span>

## <a name="working-with-aspect-ratios"></a><span data-ttu-id="bfdbe-171">Arbeiten mit Seitenverhältnissen</span><span class="sxs-lookup"><span data-stu-id="bfdbe-171">Working with Aspect Ratios</span></span>

<span data-ttu-id="bfdbe-172">Die korrekte Form eines Video Frames wird durch das *Pixel Seitenverhältnis* (par) und den *Anzeigebereich* definiert.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-172">The correct shape of a video frame is defined by the *pixel aspect ratio* (PAR) and the *display area*.</span></span>

-   <span data-ttu-id="bfdbe-173">Der par-Typ definiert die Form der Pixel in einem Bild.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-173">The PAR defines the shape of the pixels in an image.</span></span> <span data-ttu-id="bfdbe-174">Quadratische Pixel haben ein Seitenverhältnis von 1:1.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-174">Square pixels have an aspect ratio of 1:1.</span></span> <span data-ttu-id="bfdbe-175">Jedes andere Seitenverhältnis beschreibt ein nicht quadratisches Pixel.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-175">Any other aspect ratio describes a non-square pixel.</span></span> <span data-ttu-id="bfdbe-176">Beispielsweise verwendet NTSC TV eine 10:11-par-.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-176">For example, NTSC television uses a 10:11 PAR.</span></span> <span data-ttu-id="bfdbe-177">Wenn Sie das Video auf einem Computermonitor präsentieren, hat die Anzeige quadratische Pixel (1:1 PAR).</span><span class="sxs-lookup"><span data-stu-id="bfdbe-177">Assuming that you are presenting the video on a computer monitor, the display will have square pixels (1:1 PAR).</span></span> <span data-ttu-id="bfdbe-178">Der Inhalt des Quell Inhalts ist im MF-Attribut [**\_ Pixel- \_ \_ Seiten \_ Verhältnis**](mf-mt-pixel-aspect-ratio-attribute.md) für den Medientyp angegeben.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-178">The PAR of the source content is given in the [**MF\_MT\_PIXEL\_ASPECT\_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md) attribute on the media type.</span></span>
-   <span data-ttu-id="bfdbe-179">Der Anzeigebereich ist der Bereich des Video Bilds, das angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-179">The display area is the region of the video image that is intended to be shown.</span></span> <span data-ttu-id="bfdbe-180">Es gibt zwei relevante Anzeige Bereiche, die im Medientyp angegeben werden können:</span><span class="sxs-lookup"><span data-stu-id="bfdbe-180">There are two relevant display areas that might be specified in the media type:</span></span>
    -   <span data-ttu-id="bfdbe-181">Pan-and-Scan-blenden.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-181">Pan-and-scan aperture.</span></span> <span data-ttu-id="bfdbe-182">Die Pan-and-Scan-Öffnung ist ein 4 × 3-Videobereich, der im Pan/Scan-Modus angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-182">The pan-and-scan aperture is a 4×3 region of video that should be displayed in pan/scan mode.</span></span> <span data-ttu-id="bfdbe-183">Es wird verwendet, um breit Bildinhalte in einer 4 × 3-Anzeige ohne Letterboxing anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-183">It is used to show wide-screen content on a 4×3 display without letterboxing.</span></span> <span data-ttu-id="bfdbe-184">Die "Pan-and-Scan"- **Öffnung ist im** MF-Attribut " [**MF \_ MT \_ Pan \_ Scan \_ Aperture**](mf-mt-pan-scan-aperture-attribute.md) " angegeben und sollte nur verwendet werden, wenn das MF MT-Attribut für die Überprüfung [**\_ \_ \_ \_ aktiviert**](mf-mt-pan-scan-enabled-attribute.md) ist.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-184">The pan-and-scan aperture is given in the [**MF\_MT\_PAN\_SCAN\_APERTURE**](mf-mt-pan-scan-aperture-attribute.md) attribute and should be used only when the [**MF\_MT\_PAN\_SCAN\_ENABLED**](mf-mt-pan-scan-enabled-attribute.md) attribute is **TRUE**.</span></span>
    -   <span data-ttu-id="bfdbe-185">Anzeige Öffnung.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-185">Display aperture.</span></span> <span data-ttu-id="bfdbe-186">Diese Öffnung ist in einigen Videostandards definiert.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-186">This aperture is defined in some video standards.</span></span> <span data-ttu-id="bfdbe-187">Alles außerhalb der Anzeige Öffnung ist der Overscan-Bereich und sollte nicht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-187">Anything outside of the display aperture is the overscan region and should not be displayed.</span></span> <span data-ttu-id="bfdbe-188">Beispielsweise beträgt das NTSC-Fernsehen 720 × 480 Pixel mit einer Anzeige Öffnung von 704 × 480.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-188">For example, NTSC television is 720×480 pixels with a display aperture of 704×480.</span></span> <span data-ttu-id="bfdbe-189">Die Anzeige Öffnung ist im MF-Master-Attribut für die [**\_ \_ minimale \_ Anzeige \_ Öffnung**](mf-mt-minimum-display-aperture-attribute.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-189">The display aperture is given in the [**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**](mf-mt-minimum-display-aperture-attribute.md) attribute.</span></span> <span data-ttu-id="bfdbe-190">Wenn Sie vorhanden ist, sollte Sie verwendet werden, wenn der Pan-and-Scan-Modus **false** ist.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-190">If present, it should be used when pan-and-scan mode is **FALSE**.</span></span>

<span data-ttu-id="bfdbe-191">Wenn der Pan-and-can-Modus **false** ist und keine Anzeige Öffnung definiert ist, sollte der gesamte Videoframe angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-191">If pan-and-can mode is **FALSE** and no display aperture is defined, the entire video frame should be displayed.</span></span> <span data-ttu-id="bfdbe-192">Dies gilt auch für die meisten Videoinhalte außer für Fernseh-und DVD-Videos.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-192">In fact, this is the case for most video content other than television and DVD video.</span></span> <span data-ttu-id="bfdbe-193">Das Seitenverhältnis des gesamten Bilds wird als (*Anzeige Bereichs Breite* Anzeige  /  *Bereichs Höhe*) × *par* berechnet.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-193">The aspect ratio of the entire picture is calculated as (*display area width* / *display area height*) × *PAR*.</span></span>

## <a name="code-examples"></a><span data-ttu-id="bfdbe-194">Codebeispiele</span><span class="sxs-lookup"><span data-stu-id="bfdbe-194">Code Examples</span></span>

### <a name="finding-the-display-area"></a><span data-ttu-id="bfdbe-195">Suchen des Anzeige Bereichs</span><span class="sxs-lookup"><span data-stu-id="bfdbe-195">Finding the Display Area</span></span>

<span data-ttu-id="bfdbe-196">Der folgende Code zeigt, wie Sie den Anzeigebereich vom Medientyp aus aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-196">The following code shows how to get the display area from the media type.</span></span>


```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height);

HRESULT GetVideoDisplayArea(IMFMediaType *pType, MFVideoArea *pArea)
{
    HRESULT hr = S_OK;
    BOOL bPanScan = FALSE;
    UINT32 width = 0, height = 0;

    bPanScan = MFGetAttributeUINT32(pType, MF_MT_PAN_SCAN_ENABLED, FALSE);

    // In pan-and-scan mode, try to get the pan-and-scan region.
    if (bPanScan)
    {
        hr = pType->GetBlob(MF_MT_PAN_SCAN_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);
    }

    // If not in pan-and-scan mode, or the pan-and-scan region is not set, 
    // get the minimimum display aperture.

    if (!bPanScan || hr == MF_E_ATTRIBUTENOTFOUND)
    {
        hr = pType->GetBlob(MF_MT_MINIMUM_DISPLAY_APERTURE, (UINT8*)pArea, 
            sizeof(MFVideoArea), NULL);

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            // Minimum display aperture is not set.

            // For backward compatibility with some components, 
            // check for a geometric aperture. 

            hr = pType->GetBlob(MF_MT_GEOMETRIC_APERTURE, (UINT8*)pArea, 
                sizeof(MFVideoArea), NULL);
        }

        // Default: Use the entire video area.

        if (hr == MF_E_ATTRIBUTENOTFOUND)
        {
            hr = MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, &width, &height);

            if (SUCCEEDED(hr))
            {
                *pArea = MakeArea(0.0, 0.0, width, height);
            }
        }
    }
    return hr;
}
```




```C++
MFOffset MakeOffset(float v)
{
    MFOffset offset;
    offset.value = short(v);
    offset.fract = WORD(65536 * (v-offset.value));
    return offset;
}
```




```C++
MFVideoArea MakeArea(float x, float y, DWORD width, DWORD height)
{
    MFVideoArea area;
    area.OffsetX = MakeOffset(x);
    area.OffsetY = MakeOffset(y);
    area.Area.cx = width;
    area.Area.cy = height;
    return area;
}
```



### <a name="converting-between-pixel-aspect-ratios"></a><span data-ttu-id="bfdbe-197">Zwischen Pixel-Seitenverhältnissen</span><span class="sxs-lookup"><span data-stu-id="bfdbe-197">Converting Between Pixel Aspect Ratios</span></span>

<span data-ttu-id="bfdbe-198">Der folgende Code zeigt, wie ein Rechteck von einem Pixel Seitenverhältnis (par) in ein anderes konvertiert wird, während gleichzeitig das Bildseiten Verhältnis beibehalten wird.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-198">The following code shows how to convert a rectangle from one pixel aspect ratio (PAR) to another, while preserving the picture aspect ratio.</span></span>


```C++
//-----------------------------------------------------------------------------
// Converts a rectangle from one pixel aspect ratio (PAR) to another PAR.
// Returns the corrected rectangle.
//
// For example, a 720 x 486 rect with a PAR of 9:10, when converted to 1x1 PAR,
// must be stretched to 720 x 540.
//-----------------------------------------------------------------------------

RECT CorrectAspectRatio(const RECT& src, const MFRatio& srcPAR, const MFRatio& destPAR)
{
    // Start with a rectangle the same size as src, but offset to (0,0).
    RECT rc = {0, 0, src.right - src.left, src.bottom - src.top};

    // If the source and destination have the same PAR, there is nothing to do.
    // Otherwise, adjust the image size, in two steps:
    //  1. Transform from source PAR to 1:1
    //  2. Transform from 1:1 to destination PAR.

    if ((srcPAR.Numerator != destPAR.Numerator) || 
        (srcPAR.Denominator != destPAR.Denominator))
    {
        // Correct for the source's PAR.

        if (srcPAR.Numerator > srcPAR.Denominator)
        {
            // The source has "wide" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, srcPAR.Numerator, srcPAR.Denominator);
        }
        else if (srcPAR.Numerator < srcPAR.Denominator)
        {
            // The source has "tall" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, srcPAR.Denominator, srcPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.

        // Next, correct for the target's PAR. This is the inverse operation of 
        // the previous.

        if (destPAR.Numerator > destPAR.Denominator)
        {
            // The destination has "wide" pixels, so stretch the height.
            rc.bottom = MulDiv(rc.bottom, destPAR.Numerator, destPAR.Denominator);
        }
        else if (destPAR.Numerator < destPAR.Denominator)
        {
            // The destination has "tall" pixels, so stretch the width.
            rc.right = MulDiv(rc.right, destPAR.Denominator, destPAR.Numerator);
        }
        // else: PAR is 1:1, which is a no-op.
    }
    return rc;
}
```



### <a name="calculating-the-letterbox-area"></a><span data-ttu-id="bfdbe-199">Berechnen des Bereichs "Briefkasten"</span><span class="sxs-lookup"><span data-stu-id="bfdbe-199">Calculating the Letterbox Area</span></span>

<span data-ttu-id="bfdbe-200">Der folgende Code berechnet den Briefkasten Bereich bei Angabe eines Quell-und Ziel Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-200">The following code calculates the letterbox area, given a source and destination rectangle.</span></span> <span data-ttu-id="bfdbe-201">Es wird davon ausgegangen, dass beide Rechtecke denselben Wert aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bfdbe-201">It is assumed that both rectangles have the same PAR.</span></span>


```C++
RECT LetterBoxRect(const RECT& rcSrc, const RECT& rcDst)
{
    // Compute source/destination ratios.
    int iSrcWidth  = rcSrc.right - rcSrc.left;
    int iSrcHeight = rcSrc.bottom - rcSrc.top;

    int iDstWidth  = rcDst.right - rcDst.left;
    int iDstHeight = rcDst.bottom - rcDst.top;

    int iDstLBWidth;
    int iDstLBHeight;

    if (MulDiv(iSrcWidth, iDstHeight, iSrcHeight) <= iDstWidth) 
    {
        // Column letterboxing ("pillar box")
        iDstLBWidth  = MulDiv(iDstHeight, iSrcWidth, iSrcHeight);
        iDstLBHeight = iDstHeight;
    }
    else 
    {
        // Row letterboxing.
        iDstLBWidth  = iDstWidth;
        iDstLBHeight = MulDiv(iDstWidth, iSrcHeight, iSrcWidth);
    }

    // Create a centered rectangle within the current destination rect

    LONG left = rcDst.left + ((iDstWidth - iDstLBWidth) / 2);
    LONG top = rcDst.top + ((iDstHeight - iDstLBHeight) / 2);

    RECT rc;
    SetRect(&rc, left, top, left + iDstLBWidth, top + iDstLBHeight);
    return rc;
}
```



## <a name="related-topics"></a><span data-ttu-id="bfdbe-202">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bfdbe-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfdbe-203">Medientypen</span><span class="sxs-lookup"><span data-stu-id="bfdbe-203">Media Types</span></span>](media-types.md)
</dt> <dt>

[<span data-ttu-id="bfdbe-204">Video Medientypen</span><span class="sxs-lookup"><span data-stu-id="bfdbe-204">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="bfdbe-205">**minimale Anzahl von MF- \_ MT- \_ \_ anzeigen \_**</span><span class="sxs-lookup"><span data-stu-id="bfdbe-205">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="bfdbe-206">**MF- \_ MT- \_ Schwenken- \_ Überprüfung \_**</span><span class="sxs-lookup"><span data-stu-id="bfdbe-206">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)
</dt> <dt>

[<span data-ttu-id="bfdbe-207">**MF- \_ MT- \_ Schwenken- \_ Scan \_ aktiviert**</span><span class="sxs-lookup"><span data-stu-id="bfdbe-207">**MF\_MT\_PAN\_SCAN\_ENABLED**</span></span>](mf-mt-pan-scan-enabled-attribute.md)
</dt> <dt>

[<span data-ttu-id="bfdbe-208">**Verhältnis der MF- \_ MT- \_ Pixel \_ Seite \_**</span><span class="sxs-lookup"><span data-stu-id="bfdbe-208">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)
</dt> </dl>

 

 



