---
description: Zeigt, wie Sie die DXVA-Video Verarbeitung verwenden.
ms.assetid: 1465bd41-94f9-4e19-8236-00e7a2d6f54a
title: DXVA2_VideoProc Beispiel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8497a241baf07b76148a5bc2e7ddb4dd5e878e86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342498"
---
# <a name="dxva2_videoproc-sample"></a><span data-ttu-id="af2f4-103">DXVA2 \_ videoproc-Beispiel</span><span class="sxs-lookup"><span data-stu-id="af2f4-103">DXVA2\_VideoProc Sample</span></span>

<span data-ttu-id="af2f4-104">Zeigt, wie Sie die [DXVA-Video Verarbeitung](dxva-video-processing.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="af2f4-104">Shows how to use [DXVA Video Processing](dxva-video-processing.md).</span></span>

<span data-ttu-id="af2f4-105">Dieses Beispiel generiert Programm gesteuert Videos mit einem primären Stream und einem substream.</span><span class="sxs-lookup"><span data-stu-id="af2f4-105">This sample programmatically generates video with a primary stream and a substream.</span></span> <span data-ttu-id="af2f4-106">Der primäre Stream zeigt SMPTE-Farb leisten an, und der unter Datenstrom ist ein semitransparentes Rechteck.</span><span class="sxs-lookup"><span data-stu-id="af2f4-106">The primary stream displays SMPTE color bars, and the substream is a semi-transparent rectangle.</span></span> <span data-ttu-id="af2f4-107">Anschließend wird das Video mithilfe eines DXVA-Video Prozessors verarbeitet und angezeigt.</span><span class="sxs-lookup"><span data-stu-id="af2f4-107">The video is then processed and displayed using a DXVA video processor.</span></span> <span data-ttu-id="af2f4-108">Der Benutzer kann die planaren Alpha Werte, die Quell-und Ziel Rechtecke, Farbanpassungen und den Farbbereich ändern.</span><span class="sxs-lookup"><span data-stu-id="af2f4-108">The user can change the planar alpha values, source and destination rectangles, color adjustments, and color space.</span></span>

![Screenshot des dxva2 \- videoproc-Beispiels](images/dxva2-videoproc.png)

## <a name="apis-demonstrated"></a><span data-ttu-id="af2f4-110">Gezeigte APIs</span><span class="sxs-lookup"><span data-stu-id="af2f4-110">APIs Demonstrated</span></span>

<span data-ttu-id="af2f4-111">In diesem Beispiel werden die folgenden DXVA-Schnittstellen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="af2f4-111">This sample demonstrates the following DXVA interfaces:</span></span>

-   [<span data-ttu-id="af2f4-112">**Idirectxvideoprocess-Service**</span><span class="sxs-lookup"><span data-stu-id="af2f4-112">**IDirectXVideoProcessorService**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice)
-   [<span data-ttu-id="af2f4-113">**Idirectxvideoprocessor**</span><span class="sxs-lookup"><span data-stu-id="af2f4-113">**IDirectXVideoProcessor**</span></span>](/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessor)

## <a name="usage"></a><span data-ttu-id="af2f4-114">Verbrauch</span><span class="sxs-lookup"><span data-stu-id="af2f4-114">Usage</span></span>

<span data-ttu-id="af2f4-115">Mit dem DXVA2 \_ videoproc-Beispiel wird eine Windows-Anwendung erstellt.</span><span class="sxs-lookup"><span data-stu-id="af2f4-115">The DXVA2\_VideoProc sample builds a Windows application.</span></span>

<span data-ttu-id="af2f4-116">Befehlszeilenoptionen:</span><span class="sxs-lookup"><span data-stu-id="af2f4-116">Command line options:</span></span>



| <span data-ttu-id="af2f4-117">Option</span><span class="sxs-lookup"><span data-stu-id="af2f4-117">Option</span></span> | <span data-ttu-id="af2f4-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af2f4-118">Description</span></span>                                                                          |
|--------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="af2f4-119">-hh</span><span class="sxs-lookup"><span data-stu-id="af2f4-119">-hh</span></span>    | <span data-ttu-id="af2f4-120">Zwingt die Anwendung, ein Hardware Direct3D Gerät und ein Hardware-DXVA-Gerät zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="af2f4-120">Forces the application to use a hardware Direct3D device and a hardware DXVA device.</span></span> |
| <span data-ttu-id="af2f4-121">-HS</span><span class="sxs-lookup"><span data-stu-id="af2f4-121">-hs</span></span>    | <span data-ttu-id="af2f4-122">Zwingt die Anwendung, ein Hardware Direct3D Gerät und ein DXVA-Software Gerät zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="af2f4-122">Forces the application to use a hardware Direct3D device and a software DXVA device.</span></span> |
| <span data-ttu-id="af2f4-123">-ss</span><span class="sxs-lookup"><span data-stu-id="af2f4-123">-ss</span></span>    | <span data-ttu-id="af2f4-124">Zwingt die Anwendung, ein Software Direct3D Gerät und ein DXVA-Software Gerät zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="af2f4-124">Forces the application to use a software Direct3D device and a software DXVA device.</span></span> |



 

<span data-ttu-id="af2f4-125">Tastaturbefehle:</span><span class="sxs-lookup"><span data-stu-id="af2f4-125">Keyboard commands:</span></span>



| <span data-ttu-id="af2f4-126">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="af2f4-126">Key</span></span>       | <span data-ttu-id="af2f4-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af2f4-127">Description</span></span>                                             |
|-----------|---------------------------------------------------------|
| <span data-ttu-id="af2f4-128">ALT+EINGABE</span><span class="sxs-lookup"><span data-stu-id="af2f4-128">ALT+ENTER</span></span> | <span data-ttu-id="af2f4-129">Wechseln zwischen dem Fenstermodus und dem Vollbildmodus.</span><span class="sxs-lookup"><span data-stu-id="af2f4-129">Switch between windowed mode and full-screen mode.</span></span>      |
| <span data-ttu-id="af2f4-130">F1 – F8</span><span class="sxs-lookup"><span data-stu-id="af2f4-130">F1–F8</span></span>     | <span data-ttu-id="af2f4-131">Geben Sie einen der Modi in der folgenden Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="af2f4-131">Enter one of the modes shown in the following table.</span></span>    |
| <span data-ttu-id="af2f4-132">ENDE</span><span class="sxs-lookup"><span data-stu-id="af2f4-132">END</span></span>       | <span data-ttu-id="af2f4-133">Aktivieren oder Deaktivieren der Debugprotokollierung für gelöschte Frames.</span><span class="sxs-lookup"><span data-stu-id="af2f4-133">Enable or disable debugging logging for dropped frames.</span></span> |
| <span data-ttu-id="af2f4-134">POS1</span><span class="sxs-lookup"><span data-stu-id="af2f4-134">HOME</span></span>      | <span data-ttu-id="af2f4-135">Setzen Sie einen Parameter auf seinen Anfangswert zurück.</span><span class="sxs-lookup"><span data-stu-id="af2f4-135">Reset a parameter to its initial value.</span></span>                 |



 

<span data-ttu-id="af2f4-136">Jeder der Funktionstasten (F1 bis F8) wechselt zu einem Modus, in dem die Pfeiltasten zum Anpassen eines bestimmten renderingparameters verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="af2f4-136">Each of the function keys F1 through F8 switches to a mode in which the arrow keys can be used to adjust a particular rendering parameter.</span></span> <span data-ttu-id="af2f4-137">Außerdem wird die Farbe des Substreams geändert.</span><span class="sxs-lookup"><span data-stu-id="af2f4-137">In addition, the color of the substream changes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af2f4-138">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="af2f4-138">Key</span></span></th>
<th><span data-ttu-id="af2f4-139">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af2f4-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="af2f4-140">F1</span><span class="sxs-lookup"><span data-stu-id="af2f4-140">F1</span></span></td>
<td><span data-ttu-id="af2f4-141">Passen Sie die Alpha Werte an.</span><span class="sxs-lookup"><span data-stu-id="af2f4-141">Adjust the alpha values.</span></span><br/>
<ul>
<li><span data-ttu-id="af2f4-142">UP: Vergrößern Sie das planare Alpha beider Streams.</span><span class="sxs-lookup"><span data-stu-id="af2f4-142">UP: Increase the planar alpha of both streams.</span></span></li>
<li><span data-ttu-id="af2f4-143">Down: verringern Sie den planaren Alpha beider Streams.</span><span class="sxs-lookup"><span data-stu-id="af2f4-143">DOWN: Decrease the planar alpha of both streams.</span></span></li>
<li><span data-ttu-id="af2f4-144">Right: Vergrößern Sie das Pixel Alpha des Substreams.</span><span class="sxs-lookup"><span data-stu-id="af2f4-144">RIGHT: Increase the pixel alpha of the substream.</span></span></li>
<li><span data-ttu-id="af2f4-145">Left: verringern Sie das Pixel Alpha des Substreams.</span><span class="sxs-lookup"><span data-stu-id="af2f4-145">LEFT: Decrease the pixel alpha of the substream.</span></span></li>
</ul>
<span data-ttu-id="af2f4-146">Substreamfarbe: weiß</span><span class="sxs-lookup"><span data-stu-id="af2f4-146">Substream color: White</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af2f4-147">F2</span><span class="sxs-lookup"><span data-stu-id="af2f4-147">F2</span></span></td>
<td><span data-ttu-id="af2f4-148">Passen Sie den Quellbereich (Zoom) des primären Streams an.</span><span class="sxs-lookup"><span data-stu-id="af2f4-148">Adjust the primary stream's source area (zoom).</span></span><br/>
<ul>
<li><span data-ttu-id="af2f4-149">UP: vertikal vergrößern (vergrößern).</span><span class="sxs-lookup"><span data-stu-id="af2f4-149">UP: Increase vertically (zoom in).</span></span></li>
<li><span data-ttu-id="af2f4-150">Down: Vertikal verkleinern (verkleinern).</span><span class="sxs-lookup"><span data-stu-id="af2f4-150">DOWN: Decrease vertically (zoom out).</span></span></li>
<li><span data-ttu-id="af2f4-151">Right: horizontal vergrößern (vergrößern).</span><span class="sxs-lookup"><span data-stu-id="af2f4-151">RIGHT: Increase horizontally (zoom in).</span></span></li>
<li><span data-ttu-id="af2f4-152">Left: Horizontal verkleinern (verkleinern).</span><span class="sxs-lookup"><span data-stu-id="af2f4-152">LEFT: Decrease horizontally (zoom out).</span></span></li>
</ul>
<span data-ttu-id="af2f4-153">Substreamfarbe: rot</span><span class="sxs-lookup"><span data-stu-id="af2f4-153">Substream color: Red</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af2f4-154">F3</span><span class="sxs-lookup"><span data-stu-id="af2f4-154">F3</span></span></td>
<td><span data-ttu-id="af2f4-155">Verschieben Sie den Quellbereich des primären Streams.</span><span class="sxs-lookup"><span data-stu-id="af2f4-155">Move the primary stream's source area.</span></span><br/>
<ul>
<li><span data-ttu-id="af2f4-156">Aufwärts: nach oben verschieben.</span><span class="sxs-lookup"><span data-stu-id="af2f4-156">UP: Move up.</span></span></li>
<li><span data-ttu-id="af2f4-157">Down: nach unten verschieben.</span><span class="sxs-lookup"><span data-stu-id="af2f4-157">DOWN: Move down.</span></span></li>
<li><span data-ttu-id="af2f4-158">Right: nach rechts verschieben.</span><span class="sxs-lookup"><span data-stu-id="af2f4-158">RIGHT: Move right.</span></span></li>
<li><span data-ttu-id="af2f4-159">Left: nach links verschieben.</span><span class="sxs-lookup"><span data-stu-id="af2f4-159">LEFT: Move left.</span></span></li>
</ul>
<span data-ttu-id="af2f4-160">Substreamfarbe: gelb</span><span class="sxs-lookup"><span data-stu-id="af2f4-160">Substream color: Yellow</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af2f4-161">F4</span><span class="sxs-lookup"><span data-stu-id="af2f4-161">F4</span></span></td>
<td><span data-ttu-id="af2f4-162">Passen Sie den Zielbereich des primären Streams an.</span><span class="sxs-lookup"><span data-stu-id="af2f4-162">Adjust the primary stream's destination area.</span></span><br/>
<ul>
<li><span data-ttu-id="af2f4-163">UP: vertikal vergrößern.</span><span class="sxs-lookup"><span data-stu-id="af2f4-163">UP: Increase vertically.</span></span></li>
<li><span data-ttu-id="af2f4-164">Down: Vertikal verkleinern.</span><span class="sxs-lookup"><span data-stu-id="af2f4-164">DOWN: Decrease vertically.</span></span></li>
<li><span data-ttu-id="af2f4-165">Right: horizontal vergrößern.</span><span class="sxs-lookup"><span data-stu-id="af2f4-165">RIGHT: Increase horizontally.</span></span></li>
<li><span data-ttu-id="af2f4-166">Left: verringern Sie den horizontalen.</span><span class="sxs-lookup"><span data-stu-id="af2f4-166">LEFT: Decrease horizontally.</span></span></li>
</ul>
<span data-ttu-id="af2f4-167">Substreamfarbe: grün</span><span class="sxs-lookup"><span data-stu-id="af2f4-167">Substream color: Green</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af2f4-168">F5</span><span class="sxs-lookup"><span data-stu-id="af2f4-168">F5</span></span></td>
<td><span data-ttu-id="af2f4-169">Verschieben Sie den Zielbereich des primären Streams.</span><span class="sxs-lookup"><span data-stu-id="af2f4-169">Move the primary stream's destination area.</span></span><br/>
<ul>
<li><span data-ttu-id="af2f4-170">Aufwärts: nach oben verschieben.</span><span class="sxs-lookup"><span data-stu-id="af2f4-170">UP: Move up.</span></span></li>
<li><span data-ttu-id="af2f4-171">Down: nach unten verschieben.</span><span class="sxs-lookup"><span data-stu-id="af2f4-171">DOWN: Move down.</span></span></li>
<li><span data-ttu-id="af2f4-172">Right: nach rechts verschieben.</span><span class="sxs-lookup"><span data-stu-id="af2f4-172">RIGHT: Move right.</span></span></li>
<li><span data-ttu-id="af2f4-173">Left: nach links verschieben.</span><span class="sxs-lookup"><span data-stu-id="af2f4-173">LEFT: Move left.</span></span></li>
</ul>
<span data-ttu-id="af2f4-174">Substreamfarbe: Cyan</span><span class="sxs-lookup"><span data-stu-id="af2f4-174">Substream color: Cyan</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af2f4-175">F6</span><span class="sxs-lookup"><span data-stu-id="af2f4-175">F6</span></span></td>
<td><span data-ttu-id="af2f4-176">Ändern Sie die Hintergrundfarbe oder den Farb Raum.</span><span class="sxs-lookup"><span data-stu-id="af2f4-176">Change background color or color space.</span></span><br/>
<ul>
<li><span data-ttu-id="af2f4-177">Nach oben, nach unten: Durchlaufen von Farbräumen.</span><span class="sxs-lookup"><span data-stu-id="af2f4-177">UP, DOWN: Cycle through color spaces.</span></span></li>
<li><span data-ttu-id="af2f4-178">Right, Left: Durchlaufen der Hintergrundfarben.</span><span class="sxs-lookup"><span data-stu-id="af2f4-178">RIGHT, LEFT: Cycle through background colors.</span></span></li>
</ul>
<span data-ttu-id="af2f4-179">Substreamfarbe: blau</span><span class="sxs-lookup"><span data-stu-id="af2f4-179">Substream color: Blue</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="af2f4-180">F7</span><span class="sxs-lookup"><span data-stu-id="af2f4-180">F7</span></span></td>
<td><span data-ttu-id="af2f4-181">Anpassen von Helligkeit und Kontrast.</span><span class="sxs-lookup"><span data-stu-id="af2f4-181">Adjust brightness and contrast.</span></span><br/>
<ul>
<li><span data-ttu-id="af2f4-182">UP: erhöhen Sie die Helligkeit.</span><span class="sxs-lookup"><span data-stu-id="af2f4-182">UP: Increase brightness.</span></span></li>
<li><span data-ttu-id="af2f4-183">Down: Helligkeit verringern.</span><span class="sxs-lookup"><span data-stu-id="af2f4-183">DOWN: Decrease brightness.</span></span></li>
<li><span data-ttu-id="af2f4-184">Right: Vergrößern des kontra stists.</span><span class="sxs-lookup"><span data-stu-id="af2f4-184">RIGHT: Increase contrast.</span></span></li>
<li><span data-ttu-id="af2f4-185">Left: Kontrast verringern.</span><span class="sxs-lookup"><span data-stu-id="af2f4-185">LEFT: Decrease contrast.</span></span></li>
</ul>
<span data-ttu-id="af2f4-186">Substreamfarbe: Magenta</span><span class="sxs-lookup"><span data-stu-id="af2f4-186">Substream color: Magenta</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="af2f4-187">F8</span><span class="sxs-lookup"><span data-stu-id="af2f4-187">F8</span></span></td>
<td><span data-ttu-id="af2f4-188">Anpassen von Hue und Sättigung.</span><span class="sxs-lookup"><span data-stu-id="af2f4-188">Adjust hue and saturation.</span></span><br/>
<ul>
<li><span data-ttu-id="af2f4-189">UP: erhöhen Sie den Farbton.</span><span class="sxs-lookup"><span data-stu-id="af2f4-189">UP: Increase hue.</span></span></li>
<li><span data-ttu-id="af2f4-190">Down: verringern Sie den Farbton.</span><span class="sxs-lookup"><span data-stu-id="af2f4-190">DOWN: Decrease hue.</span></span></li>
<li><span data-ttu-id="af2f4-191">Right: erhöhen Sie die Sättigung.</span><span class="sxs-lookup"><span data-stu-id="af2f4-191">RIGHT: Increase saturation.</span></span></li>
<li><span data-ttu-id="af2f4-192">Left: verringern Sie die Sättigung.</span><span class="sxs-lookup"><span data-stu-id="af2f4-192">LEFT: Decrease saturation.</span></span></li>
</ul>
<span data-ttu-id="af2f4-193">Substreamfarbe: schwarz</span><span class="sxs-lookup"><span data-stu-id="af2f4-193">Substream color: Black</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="af2f4-194">Wenn Sie die Start Taste drücken, werden die Parameter für diesen Modus in jedem Modus auf ihre Anfangswerte zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="af2f4-194">In each mode, pressing the HOME key resets the parameters for that mode to their initial values.</span></span>

## <a name="requirements"></a><span data-ttu-id="af2f4-195">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="af2f4-195">Requirements</span></span>



| <span data-ttu-id="af2f4-196">Produkt</span><span class="sxs-lookup"><span data-stu-id="af2f4-196">Product</span></span>                                                        | <span data-ttu-id="af2f4-197">Version</span><span class="sxs-lookup"><span data-stu-id="af2f4-197">Version</span></span>   |
|----------------------------------------------------------------|-----------|
| [<span data-ttu-id="af2f4-198">Windows SDK</span><span class="sxs-lookup"><span data-stu-id="af2f4-198">Windows SDK</span></span>](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | <span data-ttu-id="af2f4-199">Windows 7</span><span class="sxs-lookup"><span data-stu-id="af2f4-199">Windows 7</span></span> |



 

## <a name="downloading-the-sample"></a><span data-ttu-id="af2f4-200">Herunterladen des Beispiels</span><span class="sxs-lookup"><span data-stu-id="af2f4-200">Downloading the Sample</span></span>

<span data-ttu-id="af2f4-201">Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="af2f4-201">This sample is available in the [Windows classic samples github repository](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/evrpresenter).</span></span>

## <a name="related-topics"></a><span data-ttu-id="af2f4-202">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="af2f4-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af2f4-203">DirectX-Video Beschleunigung 2,0</span><span class="sxs-lookup"><span data-stu-id="af2f4-203">DirectX Video Acceleration 2.0</span></span>](directx-video-acceleration-2-0.md)
</dt> <dt>

[<span data-ttu-id="af2f4-204">DXVA-Video Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="af2f4-204">DXVA Video Processing</span></span>](dxva-video-processing.md)
</dt> <dt>

[<span data-ttu-id="af2f4-205">Media Foundation-SDK-Beispiele</span><span class="sxs-lookup"><span data-stu-id="af2f4-205">Media Foundation SDK Samples</span></span>](media-foundation-sdk-samples.md)
</dt> </dl>

 

 




