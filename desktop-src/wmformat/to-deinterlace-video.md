---
title: Zum deinterlace-Video
description: Zum deinterlace-Video
ms.assetid: 60e6af09-fde1-4e4a-b54c-4923c0549b6b
keywords:
- Windows Media-Format-SDK, Deinterlacing-Video
- SDK für Windows Media-Format, Inverse Telecine
- Windows Media-Format-SDK, telecine
- Advanced Systems Format (ASF), Deinterlacing-Video
- ASF (Advanced Systems Format), Deinterlacing-Video
- Advanced Systems Format (ASF), Inverse Telecine
- ASF (Advanced Systems Format), Inverse Telecine
- Advanced Systems Format (ASF), telecine
- ASF (Advanced Systems Format), telecine
- Deinterlacing-Video
- Inverse Telecine, Informationen zu
- Telecine, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 580b8425e5807fefdfa889fcd08deedb4143cf39
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038570"
---
# <a name="to-deinterlace-video"></a><span data-ttu-id="2138d-115">Zum deinterlace-Video</span><span class="sxs-lookup"><span data-stu-id="2138d-115">To Deinterlace Video</span></span>

<span data-ttu-id="2138d-116">Einige Videoquellen, z. b. Video Erfassungs Karten, liefern Videodaten für die Zeilen Sprung Anzeige.</span><span class="sxs-lookup"><span data-stu-id="2138d-116">Some sources of video, such as video capture cards, deliver video data for interlaced display.</span></span> <span data-ttu-id="2138d-117">Jeder Frame mit Zeilen Sprung Video besteht aus zwei Feldern.</span><span class="sxs-lookup"><span data-stu-id="2138d-117">Each frame of interlaced video is made up of two fields.</span></span> <span data-ttu-id="2138d-118">Das oberste Feld enthält die erste Zeile des Videos und anschließend jede andere Zeile.</span><span class="sxs-lookup"><span data-stu-id="2138d-118">The top field contains the first line of video and every other line thereafter.</span></span> <span data-ttu-id="2138d-119">Das untere Feld enthält die zweite Zeile des Videos und anschließend jede andere Zeile.</span><span class="sxs-lookup"><span data-stu-id="2138d-119">The bottom field contains the second line of video and every other line thereafter.</span></span> <span data-ttu-id="2138d-120">Ein Feld enthält also alle gerade nummerierten Zeilen, das andere enthält alle ungeraden nummerierten Zeilen.</span><span class="sxs-lookup"><span data-stu-id="2138d-120">So one field contains all of the even numbered lines and the other contains all of the odd numbered lines.</span></span> <span data-ttu-id="2138d-121">Die Felder, die einen Frame bilden, stellen etwas andere Präsentations Zeiten dar, sodass Sie bei überlappenden Daten kein statisches Bild bilden.</span><span class="sxs-lookup"><span data-stu-id="2138d-121">The fields that make up a frame represent slightly different presentation times so that, when interleaved, they do not form a static image.</span></span>

<span data-ttu-id="2138d-122">Wenn Sie ein Video auf einem Computermonitor anzeigen möchten, sollte jeder Frame des Videos als ein Bild angezeigt werden (diese Methode zum Anzeigen eines gesamten Frame Bilds wird als *progressives* Video bezeichnet). Wenn Sie das Video mit Zeilen Sprung progressiv anzeigen, werden die Frames aufgrund des Zeitunterschieds zwischen den beiden Feldern möglicherweise nicht richtig angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2138d-122">When you want to display video on a computer monitor, each frame of the video should be displayed as one image (this method of displaying video one whole frame at a time is called *progressive* video.) If you display interlaced video progressively, the frames may not look right, because of the time difference between the two fields.</span></span> <span data-ttu-id="2138d-123">Der Windows Media Video Codec und der Windows Media Video Advanced Profile Codec unterstützen beide eine Vorverarbeitungs Funktion, mit der Zeilen Sprung Inhalte in progressive Frames konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="2138d-123">The Windows Media Video codec and the Windows Media Video Advanced Profile codec both support a preprocessing feature that converts interlaced content into progressive frames.</span></span>

<span data-ttu-id="2138d-124">Um das Eingabe Video "Codec Deinterlacing" zu erhalten, geben Sie die [**IWMWriterAdvanced2::**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) \*-Methode ein.</span><span class="sxs-lookup"><span data-stu-id="2138d-124">To have the codec deinterlace input video, call the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method.</span></span> <span data-ttu-id="2138d-125">Die zu verwendende Einstellung ist g \_ wszdeinterlacemode.</span><span class="sxs-lookup"><span data-stu-id="2138d-125">The setting to use is g\_wszDeinterlaceMode.</span></span> <span data-ttu-id="2138d-126">Legen Sie den Deinterlacing-Modus auf einen der folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="2138d-126">Set the deinterlacing mode to one of the following values.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2138d-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2138d-127">Value</span></span></th>
<th><span data-ttu-id="2138d-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2138d-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2138d-129">WM_DM_NOTINTERLACED</span><span class="sxs-lookup"><span data-stu-id="2138d-129">WM_DM_NOTINTERLACED</span></span></td>
<td><span data-ttu-id="2138d-130">Die Eingabe ist progressiv.</span><span class="sxs-lookup"><span data-stu-id="2138d-130">Input is progressive.</span></span> <span data-ttu-id="2138d-131">Verwenden Sie diese Einstellung, um Deinterlacing zu beenden, wenn Sie zuvor den Deinterlacing-Modus auf einen anderen Wert festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="2138d-131">Use this setting to stop deinterlacing when you have previously set the deinterlacing mode to another value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2138d-132">WM_DM_DEINTERLACE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="2138d-132">WM_DM_DEINTERLACE_NORMAL</span></span></td>
<td><span data-ttu-id="2138d-133">Wählen Sie diesen Modus aus, um die geraden und ungeraden Felder eines Zeilen Sprung Rahmens (mit einem Bewegungs Kompensationsmechanismus) zu mischen. Davon</span><span class="sxs-lookup"><span data-stu-id="2138d-133">Select this mode to blend the even and odd fields of an interlaced frame (using a motion compensation mechanism).Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="2138d-134">Die interspitze Artefakte der progressiven Anzeige werden erheblich reduziert.</span><span class="sxs-lookup"><span data-stu-id="2138d-134">The interlace artifacts of the progressive display are significantly reduced.</span></span></li>
<li><span data-ttu-id="2138d-135">Der Windows Media Video Codec erzeugt komprimierte Videos mit höherer Qualität.</span><span class="sxs-lookup"><span data-stu-id="2138d-135">The Windows Media Video codec produces higher quality compressed video.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2138d-136">WM_DM_DEINTERLACE_HALFSIZE</span><span class="sxs-lookup"><span data-stu-id="2138d-136">WM_DM_DEINTERLACE_HALFSIZE</span></span></td>
<td><span data-ttu-id="2138d-137">Wählen Sie diesen Modus aus, wenn die Ausgabeauflösung die Hälfte oder weniger der Eingabe Auflösung ist.</span><span class="sxs-lookup"><span data-stu-id="2138d-137">Select this mode when the output resolution is half, or less, of the input resolution.</span></span> <span data-ttu-id="2138d-138">Verwenden Sie diesen Modus z. b., wenn die Eingabe Videoauflösung 640 x 480 Pixel und die Ausgabevideo Auflösung 320 x 240 Pixel ist. Davon</span><span class="sxs-lookup"><span data-stu-id="2138d-138">For example, use this mode when the input video resolution is 640 x 480 pixels and the output video resolution is 320 x 240 pixels.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="2138d-139">Die interspitze Artefakte der progressiven Anzeige werden erheblich reduziert.</span><span class="sxs-lookup"><span data-stu-id="2138d-139">The interlace artifacts of the progressive display are significantly reduced.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2138d-140">WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</span><span class="sxs-lookup"><span data-stu-id="2138d-140">WM_DM_DEINTERLACE_HALFSIZEDOUBLERATE</span></span></td>
<td><span data-ttu-id="2138d-141">Wählen Sie diesen Modus aus, wenn die Ausgabeauflösung die Hälfte oder weniger der Eingabe Auflösung und die Ausgabe <a href="wmformat-glossary.md"><em>Frame Rate</em></a> doppelt so hoch ist.</span><span class="sxs-lookup"><span data-stu-id="2138d-141">Select this mode when the output resolution is half, or less, of the input resolution and the output <a href="wmformat-glossary.md"><em>frame rate</em></a> is twice as high.</span></span> <span data-ttu-id="2138d-142">Verwenden Sie diesen Modus z. b., wenn die Eingabe Videoauflösung 640 x 480 Pixel bei 30 überschneidenden Frames/Sek. und die Ausgabevideo Auflösung 320 x 240 Pixel bei 60 Frames/Sek. Davon</span><span class="sxs-lookup"><span data-stu-id="2138d-142">For example, use this mode when the input video resolution is 640 x 480 pixels at 30 interlaced frames/sec and the output video resolution is 320 x 240 pixels at 60 frames/sec.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="2138d-143">Dies erzeugt progressive Frames mit hoher Qualität, da jedes Feld in einen Frame konvertiert wird, sodass keine Informationen in die Mischung einbezogen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2138d-143">This produces progressive frames of high quality, because each field is converted to a frame and so there is no need to blend any information.</span></span></li>
<li><span data-ttu-id="2138d-144">Die vollständige Bewegung der Zeilen Sprung Felder wird aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2138d-144">The full motion of the interlaced fields is captured.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2138d-145">WM_DM_DEINTERLACE_INVERSETELECINE</span><span class="sxs-lookup"><span data-stu-id="2138d-145">WM_DM_DEINTERLACE_INVERSETELECINE</span></span></td>
<td><span data-ttu-id="2138d-146">Wählen Sie diesen Modus aus, um ein Video mit einer Textliste von 30 Frames/s in die 24 Frames/Sek. des ursprünglichen Films zu konvertieren. Davon</span><span class="sxs-lookup"><span data-stu-id="2138d-146">Select this mode to convert telecined 30 frames/sec video into the 24 frames/sec of the original film.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="2138d-147">Die Komprimierungs Qualität verbessert sich erheblich, da nur 24 Frames/Sek. anstelle von 30 Frames/Sek. erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="2138d-147">The compression quality improves significantly because only 24 frames/sec instead of 30 frames/sec need to be encoded.</span></span></li>
<li><span data-ttu-id="2138d-148">Da das Ergebnis progressiv ist, werden die gleichen Komprimierungs-und Anzeige Vorteile von Deinterlacing erkannt.</span><span class="sxs-lookup"><span data-stu-id="2138d-148">Because the result is progressive, the same compression and display benefits of deinterlacing are realized.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2138d-149">WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</span><span class="sxs-lookup"><span data-stu-id="2138d-149">WM_DM_DEINTERLACE_VERTICALHALFSIZEDOUBLERATE</span></span></td>
<td><span data-ttu-id="2138d-150">Wählen Sie diesen Modus aus, wenn die vertikale Ausgabeauflösung mindestens die Hälfte der Eingabe vertikalen Auflösung und die Ausgabe <a href="wmformat-glossary.md"><em>Frame Rate</em></a> doppelt so hoch ist.</span><span class="sxs-lookup"><span data-stu-id="2138d-150">Select this mode when the vertical output resolution is half, or less, of the input vertical resolution and the output <a href="wmformat-glossary.md"><em>frame rate</em></a> is twice as high.</span></span> <span data-ttu-id="2138d-151">Beispielsweise ist die Eingabe vertikale Videoauflösung 640 x 480 Pixel bei 30 Zeilen Sprung Bildern/Sek. und die vertikale Ausgabe des vertikalen Videos beträgt 320 x 240 Pixel bei 60 Frames/Sek. Davon</span><span class="sxs-lookup"><span data-stu-id="2138d-151">For example, the input vertical video resolution is 640 x 480 pixels at 30 interlaced frames/sec and the output vertical video resolution is 320 x 240 pixels at 60 frames/sec.Benefits:</span></span><br/>
<ul>
<li><span data-ttu-id="2138d-152">Dies erzeugt progressive Frames mit hoher Qualität, da jedes Feld in einen Frame konvertiert wird, sodass keine Informationen in die Mischung einbezogen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2138d-152">This produces progressive frames of high quality, because each field is converted to a frame and so there is no need to blend any information.</span></span></li>
<li><span data-ttu-id="2138d-153">Die vollständige Bewegung der Zeilen Sprung Felder wird aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2138d-153">The full motion of the interlaced fields is captured.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2138d-154">Legen Sie für gemischten Inhalt den Deinterlacing-Modus nach Bedarf fest, bevor Sie die Beispiele eines neuen Typs übergeben.</span><span class="sxs-lookup"><span data-stu-id="2138d-154">For mixed content, set the deinterlacing mode as needed before passing samples of a new type.</span></span> <span data-ttu-id="2138d-155">Wenn Sie z. b. die Codierung mit progressiver Eingabe starten möchten, müssen Sie keinen Deinterlacing-Modus festlegen.</span><span class="sxs-lookup"><span data-stu-id="2138d-155">For example, to start encoding with progressive input, you don't need to set any deinterlacing mode.</span></span> <span data-ttu-id="2138d-156">Wenn einige Beispiele ein normales Deinterlacing erfordern, müssen Sie den Deinterlacing-Modus auf WM \_ DM \_ deinterlace \_ Normal festlegen.</span><span class="sxs-lookup"><span data-stu-id="2138d-156">If some samples then require normal deinterlacing, you must set the deinterlacing mode to WM\_DM\_DEINTERLACE\_NORMAL.</span></span> <span data-ttu-id="2138d-157">Um zusätzliche Progressive Beispiele zu verarbeiten, müssen Sie den Deinterlacing-Modus auf WM \_ DM \_ notinterlacing festlegen.</span><span class="sxs-lookup"><span data-stu-id="2138d-157">To then process additional progressive samples you must set the deinterlacing mode to WM\_DM\_NOTINTERLACED.</span></span>

## <a name="inverse-telecine-settings"></a><span data-ttu-id="2138d-158">Umgekehrte telecine-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="2138d-158">Inverse Telecine Settings</span></span>

<span data-ttu-id="2138d-159">Eine Beschreibung der Inverse Telecine finden [Sie unter So verwenden Sie die umgekehrte telecine](to-use-inverse-telecine.md).</span><span class="sxs-lookup"><span data-stu-id="2138d-159">For a description of inverse telecine, see [To Use Inverse Telecine](to-use-inverse-telecine.md).</span></span>

<span data-ttu-id="2138d-160">Wenn Sie den Deinterlacing-Modus auf WM \_ DM \_ deinterlace \_ inversetelecine festgelegt haben, können Sie das telecine-Muster des ersten Eingabe Rahmens durch Aufrufen von [**IWMWriterAdvanced2:: setinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)angeben.</span><span class="sxs-lookup"><span data-stu-id="2138d-160">If you set the deinterlacing mode to WM\_DM\_DEINTERLACE\_INVERSETELECINE, you can specify the telecine pattern of the first input frame by calling the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting).</span></span> <span data-ttu-id="2138d-161">Die zu verwendende Einstellung ist g \_ wszinitialpatternforinvertartelecine.</span><span class="sxs-lookup"><span data-stu-id="2138d-161">The setting to use is g\_wszInitialPatternForInverseTelecine.</span></span> <span data-ttu-id="2138d-162">Legen Sie das Anfangs Muster auf einen der folgenden Werte fest.</span><span class="sxs-lookup"><span data-stu-id="2138d-162">Set the initial pattern to one of the following values.</span></span>



| <span data-ttu-id="2138d-163">Wert</span><span class="sxs-lookup"><span data-stu-id="2138d-163">Value</span></span>                                              | <span data-ttu-id="2138d-164">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2138d-164">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2138d-165">WM- \_ DM- \_ Aktivierung ( \_ \_ kohärenter \_ Modus)</span><span class="sxs-lookup"><span data-stu-id="2138d-165">WM\_DM\_IT\_DISABLE\_COHERENT\_MODE</span></span>                | <span data-ttu-id="2138d-166">Gibt an, dass die Eingabemedien den telecine-Prozess durchlaufen haben, die Rahmen jedoch nicht mehr in einem vorhersagbaren Muster vorliegen.</span><span class="sxs-lookup"><span data-stu-id="2138d-166">Specifies that the input media has gone through the telecine process but that the frames are no longer in a predictable pattern.</span></span> <span data-ttu-id="2138d-167">Dies weist normalerweise darauf hin, dass das Medium nach der telecine-Verarbeitung bearbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="2138d-167">This usually indicates that the media was edited after the telecine processing.</span></span> <span data-ttu-id="2138d-168">Wenn Sie diese Einstellung verwenden, versucht der Codec, die ursprünglichen Frames eigenständig zu rekonstruieren.</span><span class="sxs-lookup"><span data-stu-id="2138d-168">When you use this setting, the codec attempts to reconstruct the original frames on its own.</span></span> |
| <span data-ttu-id="2138d-169">WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ AA \_ Top</span><span class="sxs-lookup"><span data-stu-id="2138d-169">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_AA\_TOP</span></span>    | <span data-ttu-id="2138d-170">Gibt an, dass das oberste Feld des AA-Frames das erste Beispiel ist.</span><span class="sxs-lookup"><span data-stu-id="2138d-170">Specifies that the top field of the AA frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="2138d-171">WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ BB \_ Top</span><span class="sxs-lookup"><span data-stu-id="2138d-171">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BB\_TOP</span></span>    | <span data-ttu-id="2138d-172">Gibt an, dass das oberste Feld des BB-Frames das erste Beispiel ist.</span><span class="sxs-lookup"><span data-stu-id="2138d-172">Specifies that the top field of the BB frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="2138d-173">WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ BC \_ Top</span><span class="sxs-lookup"><span data-stu-id="2138d-173">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BC\_TOP</span></span>    | <span data-ttu-id="2138d-174">Gibt an, dass das oberste Feld des BC-Frames das erste Beispiel ist.</span><span class="sxs-lookup"><span data-stu-id="2138d-174">Specifies that the top field of the BC frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="2138d-175">WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ CD \_ Top</span><span class="sxs-lookup"><span data-stu-id="2138d-175">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_CD\_TOP</span></span>    | <span data-ttu-id="2138d-176">Gibt an, dass das oberste Feld des CD-Frames das erste Beispiel ist.</span><span class="sxs-lookup"><span data-stu-id="2138d-176">Specifies that the top field of the CD frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="2138d-177">WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ DD \_ Top</span><span class="sxs-lookup"><span data-stu-id="2138d-177">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_DD\_TOP</span></span>    | <span data-ttu-id="2138d-178">Gibt an, dass das oberste Feld des DD-Frames das erste Beispiel ist.</span><span class="sxs-lookup"><span data-stu-id="2138d-178">Specifies that the top field of the DD frame is the first sample.</span></span>                                                                                                                                                                                                                                             |
| <span data-ttu-id="2138d-179">WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ AA \_ unten</span><span class="sxs-lookup"><span data-stu-id="2138d-179">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_AA\_BOTTOM</span></span> | <span data-ttu-id="2138d-180">Gibt an, dass das untere Feld des AA-Frames das erste Beispiel ist.</span><span class="sxs-lookup"><span data-stu-id="2138d-180">Specifies that the bottom field of the AA frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="2138d-181">WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ BB \_ unten</span><span class="sxs-lookup"><span data-stu-id="2138d-181">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BB\_BOTTOM</span></span> | <span data-ttu-id="2138d-182">Gibt an, dass das untere Feld des BB-Frames das erste Beispiel ist.</span><span class="sxs-lookup"><span data-stu-id="2138d-182">Specifies that the bottom field of the BB frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="2138d-183">WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ BC \_ Bottom</span><span class="sxs-lookup"><span data-stu-id="2138d-183">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_BC\_BOTTOM</span></span> | <span data-ttu-id="2138d-184">Gibt an, dass das untere Feld des BC-Frames das erste Beispiel ist.</span><span class="sxs-lookup"><span data-stu-id="2138d-184">Specifies that the bottom field of the BC frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="2138d-185">WM \_ DM \_ \_ der erste \_ Frame \_ in \_ Clip \_ ist \_ CD \_ unten</span><span class="sxs-lookup"><span data-stu-id="2138d-185">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_CD\_BOTTOM</span></span> | <span data-ttu-id="2138d-186">Gibt an, dass das untere Feld des CD-Frames das erste Beispiel ist.</span><span class="sxs-lookup"><span data-stu-id="2138d-186">Specifies that the bottom field of the CD frame is the first sample.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="2138d-187">WM \_ DM \_ \_ der erste \_ Frame \_ im \_ Clip \_ ist \_ TT \_ unten</span><span class="sxs-lookup"><span data-stu-id="2138d-187">WM\_DM\_IT\_FIRST\_FRAME\_IN\_CLIP\_IS\_DD\_BOTTOM</span></span> | <span data-ttu-id="2138d-188">Gibt an, dass das untere Feld des DD-Frames das erste Beispiel ist.</span><span class="sxs-lookup"><span data-stu-id="2138d-188">Specifies that the bottom field of the DD frame is the first sample.</span></span>                                                                                                                                                                                                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="2138d-189">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2138d-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2138d-190">**Erweiterte Themen**</span><span class="sxs-lookup"><span data-stu-id="2138d-190">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> </dl>

 

 





