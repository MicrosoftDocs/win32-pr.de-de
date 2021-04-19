---
description: Video-Interlacing
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: Video-Interlacing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec10f49ef21f3701f85467a3f4a1c4b08d69df72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348850"
---
# <a name="video-interlacing"></a><span data-ttu-id="88ced-103">Video-Interlacing</span><span class="sxs-lookup"><span data-stu-id="88ced-103">Video Interlacing</span></span>

<span data-ttu-id="88ced-104">In diesem Thema wird beschrieben, wie Medienquellen und Decoder Zeilen Sprung Videoinhalte verarbeiten sollten.</span><span class="sxs-lookup"><span data-stu-id="88ced-104">This topic describes how media sources and decoders should handle interlaced video content.</span></span>

<span data-ttu-id="88ced-105">Zum Decodieren und Rendering von verschachtelten Videos sind folgende Informationen erforderlich:</span><span class="sxs-lookup"><span data-stu-id="88ced-105">To decode and render interlaced video correctly, the following information is needed:</span></span>

-   <span data-ttu-id="88ced-106">Progressiv oder Zeilen Sprung.</span><span class="sxs-lookup"><span data-stu-id="88ced-106">Progressive or interlaced.</span></span> <span data-ttu-id="88ced-107">Ein Videostream kann progressive Frames, Zeilen Sprung Rahmen oder eine Kombination aus beidem enthalten.</span><span class="sxs-lookup"><span data-stu-id="88ced-107">A video stream can contain progressive frames, interlaced frames, or a mix of both.</span></span>

-   <span data-ttu-id="88ced-108">Feld Dominanz.</span><span class="sxs-lookup"><span data-stu-id="88ced-108">Field dominance.</span></span> <span data-ttu-id="88ced-109">Die Feld Dominanz beschreibt, welches Feld zuerst, das obere Feld oder das untere Feld angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="88ced-109">Field dominance describes which field appears first, the upper field or the lower field.</span></span>

-   <span data-ttu-id="88ced-110">Wiederholen Sie das erste Feld.</span><span class="sxs-lookup"><span data-stu-id="88ced-110">Repeat first field.</span></span> <span data-ttu-id="88ced-111">Dieses Flag wird in 3:2 Pulldown verwendet, wenn der Frame progressiv ist, der Stream jedoch mit Zeilen Sprung versehen ist.</span><span class="sxs-lookup"><span data-stu-id="88ced-111">This flag is used in 3:2 pulldown, when the frame is progressive but the stream is interlaced.</span></span> <span data-ttu-id="88ced-112">In diesem Kontext kann das erste Feld das obere oder untere Feld sein.</span><span class="sxs-lookup"><span data-stu-id="88ced-112">In this context, the first field can be the upper or lower field.</span></span>

-   <span data-ttu-id="88ced-113">Verschachtelte Felder oder ein einzelnes Feld.</span><span class="sxs-lookup"><span data-stu-id="88ced-113">Interleaved fields or single field.</span></span> <span data-ttu-id="88ced-114">Ein Beispiel kann entweder ein einzelnes Feld oder zwei verschachtelte Felder enthalten.</span><span class="sxs-lookup"><span data-stu-id="88ced-114">A sample can hold either a single field, or two interleaved fields.</span></span> <span data-ttu-id="88ced-115">Wenn ein Beispiel ein einzelnes Feld enthält, ist die Stichproben Höhe die Hälfte der Rahmenhöhe, da das Beispiel nur die Hälfte der Überprüfungs Linien für einen Frame enthält.</span><span class="sxs-lookup"><span data-stu-id="88ced-115">If a sample contains a single field, the sample height is half the frame height, because the sample contains only half of the scan lines for a frame.</span></span> <span data-ttu-id="88ced-116">Verschachtelte Felder werden empfohlen, es sei denn, die Eigenschaften des Quell Inhalts werden anderweitig empfohlen.</span><span class="sxs-lookup"><span data-stu-id="88ced-116">Interleaved fields are recommended unless the characteristics of the source content dictate otherwise.</span></span>

<span data-ttu-id="88ced-117">Alle diese Merkmale können von einem Beispiel in das nächste geändert werden.</span><span class="sxs-lookup"><span data-stu-id="88ced-117">Any of these characteristics can change from one sample to the next.</span></span> <span data-ttu-id="88ced-118">Videokomponenten müssen jedoch etwas über den gesamten Inhalt wissen, bevor das Streaming beginnt.</span><span class="sxs-lookup"><span data-stu-id="88ced-118">However, video components need to know something about the overall content before streaming begins.</span></span> <span data-ttu-id="88ced-119">Wenn das Video z. b. Zeilen Sprung ist, muss der erweiterte Videorenderer (EVR) Videospeicher für das Deinterlacing reservieren.</span><span class="sxs-lookup"><span data-stu-id="88ced-119">For example, if the video is interlaced, the enhanced video renderer (EVR) needs to reserve video memory for the deinterlacing.</span></span> <span data-ttu-id="88ced-120">Wenn das Video vollständig progressive Frames ist, kann der EVR die Renderingpipeline optimieren.</span><span class="sxs-lookup"><span data-stu-id="88ced-120">If the video is entirely progressive frames, on the other hand, the EVR can optimize the rendering pipeline.</span></span> <span data-ttu-id="88ced-121">Das Hinzufügen eines Deinterlacing-Schritts zur Pipeline erhöht die Renderingleistung.</span><span class="sxs-lookup"><span data-stu-id="88ced-121">Adding a deinterlacing step to the pipeline increases the rendering latency.</span></span>

<span data-ttu-id="88ced-122">Informationen über das Zeilen Sprung werden an zwei Stellen gespeichert:</span><span class="sxs-lookup"><span data-stu-id="88ced-122">Information about interlacing is stored in two places:</span></span>

-   <span data-ttu-id="88ced-123">Allgemeine Informationen über die Überlappung in einem Stream werden in den Medientyp eingefügt.</span><span class="sxs-lookup"><span data-stu-id="88ced-123">General information about the interlacing in a stream is placed in the media type.</span></span> <span data-ttu-id="88ced-124">Weitere Informationen zu Medientypen finden Sie unter [Medientypen](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="88ced-124">For more information about media types, see [Media Types](media-types.md).</span></span>

-   <span data-ttu-id="88ced-125">Informationen, die sich bei jeder Stichprobe ändern können, werden im Beispiel als Attribut abgelegt.</span><span class="sxs-lookup"><span data-stu-id="88ced-125">Information that can change with each sample is placed on the sample as an attribute.</span></span> <span data-ttu-id="88ced-126">Weitere Informationen zu Beispielen finden Sie unter [Medien Beispiele](media-samples.md).</span><span class="sxs-lookup"><span data-stu-id="88ced-126">For more information about samples, see [Media Samples](media-samples.md).</span></span>

## <a name="interlace-information-in-the-media-type"></a><span data-ttu-id="88ced-127">Interlace-Informationen im Medientyp</span><span class="sxs-lookup"><span data-stu-id="88ced-127">Interlace Information in the Media Type</span></span>

<span data-ttu-id="88ced-128">Das [**MF \_ MT \_ Interlace \_ Mode**](mf-mt-interlace-mode-attribute.md) -Attribut für den Medientyp beschreibt, wie der Datenstrom als Ganzes mit Zeilen Sprung versehen wird.</span><span class="sxs-lookup"><span data-stu-id="88ced-128">The [**MF\_MT\_INTERLACE\_MODE**](mf-mt-interlace-mode-attribute.md) attribute on the media type describes how the stream as a whole is interlaced.</span></span> <span data-ttu-id="88ced-129">Der Wert dieses Attributs ist ein Member der [**mfvideointerlacemode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="88ced-129">The value of this attribute is a member of the [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) enumeration.</span></span> <span data-ttu-id="88ced-130">Ein Video Medientyp sollte immer über dieses Attribut verfügen.</span><span class="sxs-lookup"><span data-stu-id="88ced-130">A video media type should always have this attribute.</span></span>

-   <span data-ttu-id="88ced-131">Wenn der Stream nur progressive Frames ohne Zeilen Sprung enthält, verwenden Sie MF videointerlace \_ progressiv.</span><span class="sxs-lookup"><span data-stu-id="88ced-131">If the stream contains only progressive frames, with no interlaced frames, use MFVideoInterlace\_Progressive.</span></span>
-   <span data-ttu-id="88ced-132">Wenn der Stream nur Zeilen Sprung Rahmen enthält und jedes Beispiel zwei verschachtelte Felder enthält, verwenden Sie MF videointerlace \_ fieldinterleavedupperfirst oder MF videointerlace \_ fieldinterleavedlowerfirst.</span><span class="sxs-lookup"><span data-stu-id="88ced-132">If the stream contains only interlaced frames, and every sample contains two interleaved fields, use MFVideoInterlace\_FieldInterleavedUpperFirst or MFVideoInterlace\_FieldInterleavedLowerFirst.</span></span>
-   <span data-ttu-id="88ced-133">Wenn der Stream nur verschachtelte Rahmen enthält und jedes Beispiel ein einzelnes Feld enthält, verwenden Sie MF videointerlace \_ fieldsingleupperoder MF videointerlace \_ fieldsinglelower.</span><span class="sxs-lookup"><span data-stu-id="88ced-133">If the stream contains only interlaced frames, and every sample contains a single field, use MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower.</span></span> <span data-ttu-id="88ced-134">Wenn die Felder zwischen Groß und unten wechseln, spielt es keine Rolle, welche dieser beiden Werte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="88ced-134">If the fields alternate between upper and lower, then it does not matter which of these two values is used.</span></span> <span data-ttu-id="88ced-135">Wenn das Format nur obere Felder oder nur untere Felder enthält, legen Sie den Wert fest, der dem Inhalt entspricht.</span><span class="sxs-lookup"><span data-stu-id="88ced-135">If the format contains just upper fields, or just lower fields, then set the value that corresponds to the content.</span></span>
-   <span data-ttu-id="88ced-136">Wenn der Stream eine Mischung aus Zeilen Sprung-und progressivem Rahmen enthält oder die Feld Dominanz wechselt, legen Sie den Medientyp auf mfvideointerlace \_ mixedinterlaceorprogressive fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-136">If the stream contains a mix of interlaced and progressive frames, or if the field dominance switches, set the media type to MFVideoInterlace\_MixedInterlaceOrProgressive.</span></span> <span data-ttu-id="88ced-137">Verwenden Sie Beispiel Attribute, um die einzelnen Frames zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="88ced-137">Use sample attributes to describe each frame.</span></span>

<span data-ttu-id="88ced-138">In der folgenden Tabelle wird dieses Attribut zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="88ced-138">The following table summarizes this attribute.</span></span>



| <span data-ttu-id="88ced-139">MF- \_ MT- \_ Interlace- \_ Modus</span><span class="sxs-lookup"><span data-stu-id="88ced-139">MF\_MT\_INTERLACE\_MODE</span></span>                       | <span data-ttu-id="88ced-140">Zeilen Sprung?</span><span class="sxs-lookup"><span data-stu-id="88ced-140">Interlaced?</span></span> | <span data-ttu-id="88ced-141">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88ced-141">Samples</span></span>                                  | <span data-ttu-id="88ced-142">Erstes Feld</span><span class="sxs-lookup"><span data-stu-id="88ced-142">First field</span></span>    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| <span data-ttu-id="88ced-143">MF videointerlace \_ progressiv</span><span class="sxs-lookup"><span data-stu-id="88ced-143">MFVideoInterlace\_Progressive</span></span>                 | <span data-ttu-id="88ced-144">Nein</span><span class="sxs-lookup"><span data-stu-id="88ced-144">No</span></span>          | <span data-ttu-id="88ced-145">Progressiver Frame</span><span class="sxs-lookup"><span data-stu-id="88ced-145">Progressive frame</span></span>                        | <span data-ttu-id="88ced-146">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="88ced-146">Not applicable</span></span> |
| <span data-ttu-id="88ced-147">MF-Interlace \_ fieldinterleavedupperfirst</span><span class="sxs-lookup"><span data-stu-id="88ced-147">MFVideoInterlace\_FieldInterleavedUpperFirst</span></span>  | <span data-ttu-id="88ced-148">Ja</span><span class="sxs-lookup"><span data-stu-id="88ced-148">Yes</span></span>         | <span data-ttu-id="88ced-149">Verschachtelte Felder</span><span class="sxs-lookup"><span data-stu-id="88ced-149">Interleaved fields</span></span>                       | <span data-ttu-id="88ced-150">Obere erste</span><span class="sxs-lookup"><span data-stu-id="88ced-150">Upper first</span></span>    |
| <span data-ttu-id="88ced-151">MF-Interlace \_ fieldinterleavedlowerfirst</span><span class="sxs-lookup"><span data-stu-id="88ced-151">MFVideoInterlace\_FieldInterleavedLowerFirst</span></span>  | <span data-ttu-id="88ced-152">Ja</span><span class="sxs-lookup"><span data-stu-id="88ced-152">Yes</span></span>         | <span data-ttu-id="88ced-153">Verschachtelte Felder</span><span class="sxs-lookup"><span data-stu-id="88ced-153">Interleaved fields</span></span>                       | <span data-ttu-id="88ced-154">Zuerst unten</span><span class="sxs-lookup"><span data-stu-id="88ced-154">Lower first</span></span>    |
| <span data-ttu-id="88ced-155">MF-Interlace \_ fieldsingleupper</span><span class="sxs-lookup"><span data-stu-id="88ced-155">MFVideoInterlace\_FieldSingleUpper</span></span>            | <span data-ttu-id="88ced-156">Ja</span><span class="sxs-lookup"><span data-stu-id="88ced-156">Yes</span></span>         | <span data-ttu-id="88ced-157">Einzelfeld</span><span class="sxs-lookup"><span data-stu-id="88ced-157">Single field</span></span>                             | <span data-ttu-id="88ced-158">Obere erste</span><span class="sxs-lookup"><span data-stu-id="88ced-158">Upper first</span></span>    |
| <span data-ttu-id="88ced-159">MF-Interlace \_ fieldsinglelower</span><span class="sxs-lookup"><span data-stu-id="88ced-159">MFVideoInterlace\_FieldSingleLower</span></span>            | <span data-ttu-id="88ced-160">Ja</span><span class="sxs-lookup"><span data-stu-id="88ced-160">Yes</span></span>         | <span data-ttu-id="88ced-161">Einzelfeld</span><span class="sxs-lookup"><span data-stu-id="88ced-161">Single field</span></span>                             | <span data-ttu-id="88ced-162">Zuerst unten</span><span class="sxs-lookup"><span data-stu-id="88ced-162">Lower first</span></span>    |
| <span data-ttu-id="88ced-163">MF videointerlace \_ mixedinterlaceorprogressiv</span><span class="sxs-lookup"><span data-stu-id="88ced-163">MFVideoInterlace\_MixedInterlaceOrProgressive</span></span> | <span data-ttu-id="88ced-164">Kann variieren</span><span class="sxs-lookup"><span data-stu-id="88ced-164">Can vary</span></span>    | <span data-ttu-id="88ced-165">Verschachtelte Felder oder progressive Frames</span><span class="sxs-lookup"><span data-stu-id="88ced-165">Interleaved fields or progressive frames</span></span> | <span data-ttu-id="88ced-166">Kann variieren</span><span class="sxs-lookup"><span data-stu-id="88ced-166">Can vary</span></span>       |



 

<span data-ttu-id="88ced-167">Verschachtelte Felder und einzelne Felder können nicht gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="88ced-167">Interleaved fields and single fields cannot be mixed.</span></span> <span data-ttu-id="88ced-168">Der Wechsel von einem zu einem anderen erfordert eine Änderung des Medientyps.</span><span class="sxs-lookup"><span data-stu-id="88ced-168">Switching from one to another requires a media type change.</span></span>

## <a name="interlace-flags-on-samples"></a><span data-ttu-id="88ced-169">Interlace-Flags für Beispiele</span><span class="sxs-lookup"><span data-stu-id="88ced-169">Interlace Flags on Samples</span></span>

<span data-ttu-id="88ced-170">Informationen, die sich von einem Beispiel in das nächste ändern können, werden mithilfe von Beispiel Attributen angegeben.</span><span class="sxs-lookup"><span data-stu-id="88ced-170">Information that can change from one sample to the next is indicated using sample attributes.</span></span> <span data-ttu-id="88ced-171">Verwenden Sie die [**imfsample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) -Schnittstelle, um diese Attribute zu erhalten oder festzulegen.</span><span class="sxs-lookup"><span data-stu-id="88ced-171">Use the [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) interface to get or set these attributes.</span></span>

<span data-ttu-id="88ced-172">Alle in diesem Abschnitt aufgeführten Zeilen Sprung-Attribute verfügen über boolesche Werte.</span><span class="sxs-lookup"><span data-stu-id="88ced-172">All of the interlacing attributes listed in this section have Boolean values.</span></span> <span data-ttu-id="88ced-173">Tatsächlich kann jedes dieser Attribute über drei Werte verfügen: **true**, **false** oder nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="88ced-173">Effectively, each of these attributes can have three values: either **TRUE**, **FALSE**, or not set.</span></span> <span data-ttu-id="88ced-174">Wenn ein Attribut nicht festgelegt ist, wird der Wert aus dem Medientyp entnommen.</span><span class="sxs-lookup"><span data-stu-id="88ced-174">If an attribute is not set, the value is taken from the media type.</span></span> <span data-ttu-id="88ced-175">Wenn ein Attribut festgelegt ist, überschreibt der Wert den Medientyp.</span><span class="sxs-lookup"><span data-stu-id="88ced-175">If an attribute is set, the value overrides the media type.</span></span> <span data-ttu-id="88ced-176">Einige Kombinationen von Flags und Medientypen sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="88ced-176">Some combinations of flags and media types are not valid.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88ced-177">Attribut</span><span class="sxs-lookup"><span data-stu-id="88ced-177">Attribute</span></span></th>
<th><span data-ttu-id="88ced-178">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="88ced-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="88ced-179"><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></span><span class="sxs-lookup"><span data-stu-id="88ced-179"><a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a></span></span></td>
<td><span data-ttu-id="88ced-180"><strong>True</strong>gibt an, dass der Frame mit Zeilen Sprung verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="88ced-180">If <strong>TRUE</strong>, the frame is interlaced.</span></span> <span data-ttu-id="88ced-181"><strong>False</strong>gibt an, dass der Frame progressiv ist.</span><span class="sxs-lookup"><span data-stu-id="88ced-181">If <strong>FALSE</strong>, the frame is progressive.</span></span><br/> <span data-ttu-id="88ced-182">Legen Sie dieses Attribut für jedes Beispiel fest, wenn der Medientyp MFVideoInterlace_MixedInterlaceOrProgressive ist.</span><span class="sxs-lookup"><span data-stu-id="88ced-182">Set this attribute on every sample if the media type is MFVideoInterlace_MixedInterlaceOrProgressive.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88ced-183"><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></span><span class="sxs-lookup"><span data-stu-id="88ced-183"><a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a></span></span></td>
<td><span data-ttu-id="88ced-184">Die Bedeutung dieses Flags hängt davon ab, ob die Beispiele verschachtelte Felder oder einzelne Felder enthalten.</span><span class="sxs-lookup"><span data-stu-id="88ced-184">The meaning of this flag depends on whether the samples contain interleaved fields or single fields.</span></span><br/>
<ul>
<li><span data-ttu-id="88ced-185">Verschachtelte Felder: <strong>true</strong>gibt an, dass das untere Feld zuerst ist.</span><span class="sxs-lookup"><span data-stu-id="88ced-185">Interleaved fields: If <strong>TRUE</strong>, the lower field is first.</span></span> <span data-ttu-id="88ced-186">Wenn <strong>false</strong>, wird das obere Feld zuerst angezeigt.</span><span class="sxs-lookup"><span data-stu-id="88ced-186">If <strong>FALSE</strong>, the upper field is first.</span></span><br/></li>
<li><span data-ttu-id="88ced-187">Einzelne Felder: Wenn <strong>true</strong>, enthält das Beispiel ein niedrigeres Feld.</span><span class="sxs-lookup"><span data-stu-id="88ced-187">Single fields: If <strong>TRUE</strong>, the sample contains a lower field.</span></span> <span data-ttu-id="88ced-188"><strong>False</strong>gibt an, dass das Beispiel ein oberes Feld enthält.</span><span class="sxs-lookup"><span data-stu-id="88ced-188">If <strong>FALSE</strong>, the sample contains an upper field.</span></span><br/></li>
</ul>
<span data-ttu-id="88ced-189">Legen Sie dieses Attribut für jedes damit-Beispiel fest, wenn der Medientyp MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower oder MFVideoInterlace_MixedInterlaceOrProgressive ist.</span><span class="sxs-lookup"><span data-stu-id="88ced-189">Set this attribute on every interlace sample if the media type is MFVideoInterlace_FieldSingleUpper, MFVideoInterlace_FieldSingleLower, or MFVideoInterlace_MixedInterlaceOrProgressive.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="88ced-190"><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></span><span class="sxs-lookup"><span data-stu-id="88ced-190"><a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a></span></span></td>
<td><span data-ttu-id="88ced-191"><strong>True</strong>gibt an, dass das erste Feld wiederholt wird.</span><span class="sxs-lookup"><span data-stu-id="88ced-191">If <strong>TRUE</strong>, the first field is repeated.</span></span> <span data-ttu-id="88ced-192">Wenn <strong>false</strong> oder nicht festgelegt ist, wird das erste Feld nicht wiederholt.</span><span class="sxs-lookup"><span data-stu-id="88ced-192">If <strong>FALSE</strong> or not set, the first field is not repeated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="88ced-193"><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></span><span class="sxs-lookup"><span data-stu-id="88ced-193"><a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a></span></span></td>
<td><span data-ttu-id="88ced-194"><strong>True</strong>gibt an, dass das Beispiel ein einzelnes Feld enthält.</span><span class="sxs-lookup"><span data-stu-id="88ced-194">If <strong>TRUE</strong>, the sample contains a single field.</span></span> <span data-ttu-id="88ced-195">Wenn der Wert <strong>false</strong>ist, enthält das Beispiel verschachtelte Felder.</span><span class="sxs-lookup"><span data-stu-id="88ced-195">If <strong>FALSE</strong>, the sample contains interleaved fields.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="88ced-196">In der folgenden Tabelle wird basierend auf dem Medientyp angezeigt, welche Flags erforderlich, optional oder nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="88ced-196">The following table shows which flags are required, optional, or prohibited, based on the media type.</span></span>



| <span data-ttu-id="88ced-197">Medientyp</span><span class="sxs-lookup"><span data-stu-id="88ced-197">Media Type</span></span>         | <span data-ttu-id="88ced-198">Zeilen Sprung-Flag</span><span class="sxs-lookup"><span data-stu-id="88ced-198">Interlaced Flag</span></span>                      | <span data-ttu-id="88ced-199">Bottomfieldfirst-Flag</span><span class="sxs-lookup"><span data-stu-id="88ced-199">BottomFieldFirst Flag</span></span>                    | <span data-ttu-id="88ced-200">Repeatfirstfield-Flag</span><span class="sxs-lookup"><span data-stu-id="88ced-200">RepeatFirstField Flag</span></span> | <span data-ttu-id="88ced-201">Singlefield-Flag</span><span class="sxs-lookup"><span data-stu-id="88ced-201">SingleField Flag</span></span>                     |
|--------------------|--------------------------------------|------------------------------------------|-----------------------|--------------------------------------|
| <span data-ttu-id="88ced-202">progressiv</span><span class="sxs-lookup"><span data-stu-id="88ced-202">Progressive</span></span>        | <span data-ttu-id="88ced-203">Optionale Wenn festgelegt, muss den Wert **false** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="88ced-203">Optional; if set, must be **FALSE**.</span></span> | <span data-ttu-id="88ced-204">Legen Sie keinen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-204">Do not set.</span></span>                              | <span data-ttu-id="88ced-205">Legen Sie keinen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-205">Do not set.</span></span>           | <span data-ttu-id="88ced-206">Legen Sie keinen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-206">Do not set.</span></span>                          |
| <span data-ttu-id="88ced-207">Verschachtelte Felder</span><span class="sxs-lookup"><span data-stu-id="88ced-207">Interleaved fields</span></span> | <span data-ttu-id="88ced-208">Optionale Wenn festgelegt, muss **true** sein.</span><span class="sxs-lookup"><span data-stu-id="88ced-208">Optional; if set, must be **TRUE**.</span></span>  | <span data-ttu-id="88ced-209">Optionale Wenn festgelegt, muss dem Medientyp entsprechen.</span><span class="sxs-lookup"><span data-stu-id="88ced-209">Optional; if set, must match media type.</span></span> | <span data-ttu-id="88ced-210">Legen Sie keinen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-210">Do not set.</span></span>           | <span data-ttu-id="88ced-211">Optionale Wenn festgelegt, muss den Wert **false** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="88ced-211">Optional; if set, must be **FALSE**.</span></span> |
| <span data-ttu-id="88ced-212">Einzelne Felder</span><span class="sxs-lookup"><span data-stu-id="88ced-212">Single fields</span></span>      | <span data-ttu-id="88ced-213">Optionale Wenn festgelegt, muss **true** sein.</span><span class="sxs-lookup"><span data-stu-id="88ced-213">Optional; if set, must be **TRUE**.</span></span>  | <span data-ttu-id="88ced-214">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="88ced-214">Required.</span></span>                                | <span data-ttu-id="88ced-215">Legen Sie keinen Wert fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-215">Do not set.</span></span>           | <span data-ttu-id="88ced-216">Auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="88ced-216">Set to **TRUE**.</span></span>                     |
| <span data-ttu-id="88ced-217">Mixed</span><span class="sxs-lookup"><span data-stu-id="88ced-217">Mixed</span></span>              | <span data-ttu-id="88ced-218">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="88ced-218">Required.</span></span>                            | <span data-ttu-id="88ced-219">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="88ced-219">Required.</span></span>                                | <span data-ttu-id="88ced-220">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="88ced-220">Required.</span></span>             | <span data-ttu-id="88ced-221">Optionale Wenn festgelegt, muss den Wert **false** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="88ced-221">Optional; if set, must be **FALSE**.</span></span> |



 

<span data-ttu-id="88ced-222">In Fällen, in denen das Attribut optional ist, definiert der Medientyp bereits die Informationen.</span><span class="sxs-lookup"><span data-stu-id="88ced-222">In the cases where the attribute is optional, the media type already defines the information.</span></span> <span data-ttu-id="88ced-223">Es ist zulässig, das-Attribut auf eine Entsprechung festzulegen, jedoch nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="88ced-223">It is valid to set the attribute to match, but not required.</span></span>

<span data-ttu-id="88ced-224">Wenn der Medientyp z. b. "MF videointerlace \_ progressiv" ist, bedeutet dies, dass alle Frames im Stream progressiv sind.</span><span class="sxs-lookup"><span data-stu-id="88ced-224">For example, if the media type is MFVideoInterlace\_Progressive, it implies that all frames in the stream are progressive.</span></span> <span data-ttu-id="88ced-225">Daher können Sie entweder das **\_ Interlacing-Attribut "mfsampleextension** " auf " **false**" festlegen oder das Attribut nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="88ced-225">Therefore, you can either set the **MFSampleExtension\_Interlaced** attribute to **FALSE**, or leave the attribute unset.</span></span>

## <a name="recommendations"></a><span data-ttu-id="88ced-226">Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="88ced-226">Recommendations</span></span>

<span data-ttu-id="88ced-227">Dieser Abschnitt enthält Empfehlungen für verschiedene Inhaltstypen.</span><span class="sxs-lookup"><span data-stu-id="88ced-227">This section contains recommendations for various types of content.</span></span>

1. <span data-ttu-id="88ced-228">Das Video ist alle progressiven Frames.</span><span class="sxs-lookup"><span data-stu-id="88ced-228">The video is all progressive frames.</span></span>

-   <span data-ttu-id="88ced-229">Legen Sie den Medientyp auf mfvideointerlace \_ progressiv fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-229">Set the media type to MFVideoInterlace\_Progressive.</span></span>

-   <span data-ttu-id="88ced-230">Legen Sie das **\_ Interlacing-Attribut "mfsampleextension** " nicht fest, oder legen Sie es für jeden Frame auf " **false** " fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-230">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="88ced-231">Legen Sie die ' **MF SampleExtension '-Attribute ' \_ bottomfieldfirst**', ' **MF SampleExtension ' \_ repeatfirstfield**' oder ' **MF Sample Extension \_** ' nicht fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-231">Do not set the **MFSampleExtension\_BottomFieldFirst**, **MFSampleExtension\_RepeatFirstField**, or **MFSampleExtension\_SingleField** attributes.</span></span>

2. <span data-ttu-id="88ced-232">Das Video stellt alle Zeilen Sprung Felder mit der gleichen Feld Dominanz dar.</span><span class="sxs-lookup"><span data-stu-id="88ced-232">The video is all interlaced fields with the same field dominance.</span></span> <span data-ttu-id="88ced-233">Beispiele enthalten verschachtelte Felder.</span><span class="sxs-lookup"><span data-stu-id="88ced-233">Samples contain interleaved fields.</span></span>

-   <span data-ttu-id="88ced-234">Legen Sie den Medientyp auf mfvideointerlace \_ fieldinterleavedupperfirst oder mfvideointerlace \_ fieldinterleavedlowerfirst fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-234">Set the media type to MFVideoInterlace\_FieldInterleavedUpperFirst or MFVideoInterlace\_FieldInterleavedLowerFirst.</span></span>

-   <span data-ttu-id="88ced-235">Legen Sie das **\_ Interlacing-Attribut "mfsampleextension** " nicht fest, oder legen Sie es für jeden Frame auf " **true** " fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-235">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **TRUE** on every frame.</span></span>

-   <span data-ttu-id="88ced-236">Legen Sie das Attribut " **mfsampleextension \_ bottomfieldfirst** " nicht fest, oder legen Sie den Wert für jeden Frame entsprechend dem Medientyp fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-236">Do not set the **MFSampleExtension\_BottomFieldFirst** attribute, or set the value on every frame to match the media type.</span></span>

-   <span data-ttu-id="88ced-237">Legen Sie das Attribut " **\_ repeatfirstfield" der mfsampleextension** nicht fest, oder legen Sie es für jeden Frame auf " **false** " fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-237">Do not set the **MFSampleExtension\_RepeatFirstField** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="88ced-238">Legen Sie das **\_ Singlefield-Attribut "mfsampleextension** " nicht fest, oder legen Sie es für jeden Frame auf " **false** " fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-238">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **FALSE** on every frame.</span></span>

3. <span data-ttu-id="88ced-239">Das Video enthält eine Mischung aus Zeilen Sprung-und progressivem Rahmen mit wiederholten Feldern und abweichender Feld Dominanz (z. b. DVD-Video).</span><span class="sxs-lookup"><span data-stu-id="88ced-239">The video contains a mix of interlaced and progressive frames, with repeated fields and varying field dominance (for example, DVD video).</span></span>

-   <span data-ttu-id="88ced-240">Legen Sie den Medientyp auf mfvideointerlace \_ mixedinterlaceorprogressive fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-240">Set the media type to MFVideoInterlace\_MixedInterlaceOrProgressive.</span></span>

-   <span data-ttu-id="88ced-241">Legen Sie in jedem Frame die Attribute **mfsampleextension \_ Interlacing**, **mfsampleextension \_ bottomfieldfirst** und **mfsampleextension \_ repeatfirstfield** fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-241">On every frame, set the **MFSampleExtension\_Interlaced**, **MFSampleExtension\_BottomFieldFirst**, and **MFSampleExtension\_RepeatFirstField** attributes.</span></span>

-   <span data-ttu-id="88ced-242">Legen Sie das **\_ Singlefield-Attribut "mfsampleextension** " nicht fest, oder legen Sie es für jeden Frame auf " **false** " fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-242">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **FALSE** on every frame.</span></span>

4. <span data-ttu-id="88ced-243">Das Video ist Zeilen Sprung, und die Beispiele enthalten einzelne Felder.</span><span class="sxs-lookup"><span data-stu-id="88ced-243">The video is interlaced and samples contain single fields.</span></span>

-   <span data-ttu-id="88ced-244">Legen Sie den Medientyp auf mfvideointerlace \_ fieldsingleupperoder mfvideointerlace \_ fieldsinglelower fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-244">Set the media type to MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower.</span></span>

-   <span data-ttu-id="88ced-245">Legen Sie in jedem Frame das Attribut " **mfsampleextension \_ bottomfieldfirst** " fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-245">On every frame, set the **MFSampleExtension\_BottomFieldFirst** attribute.</span></span>

-   <span data-ttu-id="88ced-246">Legen Sie das **\_ Interlacing-Attribut "mfsampleextension** " nicht fest, oder legen Sie es für jeden Frame auf " **true** " fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-246">Do not set the **MFSampleExtension\_Interlaced** attribute, or set it to **TRUE** on every frame.</span></span>

-   <span data-ttu-id="88ced-247">Legen Sie das Attribut " **\_ repeatfirstfield" der mfsampleextension** nicht fest, oder legen Sie es für jeden Frame auf " **false** " fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-247">Do not set the **MFSampleExtension\_RepeatFirstField** attribute, or set it to **FALSE** on every frame.</span></span>

-   <span data-ttu-id="88ced-248">Legen Sie das **\_ Singlefield-Attribut "mfsampleextension** " nicht fest, oder legen Sie es für jeden Frame auf " **true** " fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-248">Do not set the **MFSampleExtension\_SingleField** attribute, or set it to **TRUE** on every frame.</span></span>

<span data-ttu-id="88ced-249">Die meisten Videoinhalte fallen in eine dieser Kategorien.</span><span class="sxs-lookup"><span data-stu-id="88ced-249">Most video content falls into one of these categories.</span></span>

## <a name="mpeg-2-mappings"></a><span data-ttu-id="88ced-250">MPEG-2-Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="88ced-250">MPEG-2 Mappings</span></span>

<span data-ttu-id="88ced-251">Verwenden Sie für MPEG-2-Inhalte die folgenden Zuordnungen, um die MPEG-2-Flags in Media Foundation Beispiel Attribute zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="88ced-251">For MPEG-2 content, use the following mappings to convert the MPEG-2 flags to Media Foundation sample attributes.</span></span>

<span data-ttu-id="88ced-252">**Bild \_ Struktur**</span><span class="sxs-lookup"><span data-stu-id="88ced-252">**picture\_structure**</span></span>



| <span data-ttu-id="88ced-253">Wert</span><span class="sxs-lookup"><span data-stu-id="88ced-253">Value</span></span>         | <span data-ttu-id="88ced-254">Sample-Attribut</span><span class="sxs-lookup"><span data-stu-id="88ced-254">Sample Attribute</span></span>                                                                                                        |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88ced-255">frame</span><span class="sxs-lookup"><span data-stu-id="88ced-255">frame</span></span>         | <span data-ttu-id="88ced-256">**MF Sample Extension \_ Singlefield**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="88ced-256">**MFSampleExtension\_SingleField** = **FALSE**</span></span>                                                                          |
| <span data-ttu-id="88ced-257">Oberstes \_ Feld</span><span class="sxs-lookup"><span data-stu-id="88ced-257">top\_field</span></span>    | <span data-ttu-id="88ced-258">**MF Sample Extension \_ Singlefield**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="88ced-258">**MFSampleExtension\_SingleField** = **TRUE**</span></span><br/> <span data-ttu-id="88ced-259">**MF Sample Extension \_ Bottomfieldfirst**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="88ced-259">**MFSampleExtension\_BottomFieldFirst** = **FALSE**</span></span><br/> |
| <span data-ttu-id="88ced-260">Unteres \_ Feld</span><span class="sxs-lookup"><span data-stu-id="88ced-260">bottom\_field</span></span> | <span data-ttu-id="88ced-261">**MF Sample Extension \_ Singlefield**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="88ced-261">**MFSampleExtension\_SingleField** = **TRUE**</span></span><br/> <span data-ttu-id="88ced-262">**MF Sample Extension \_ Bottomfieldfirst**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="88ced-262">**MFSampleExtension\_BottomFieldFirst** = **TRUE**</span></span><br/>  |



 

<span data-ttu-id="88ced-263">**progressiver \_ Frame**</span><span class="sxs-lookup"><span data-stu-id="88ced-263">**progressive\_frame**</span></span>



| <span data-ttu-id="88ced-264">Wert</span><span class="sxs-lookup"><span data-stu-id="88ced-264">Value</span></span> | <span data-ttu-id="88ced-265">Sample-Attribut</span><span class="sxs-lookup"><span data-stu-id="88ced-265">Sample Attribute</span></span>                              |
|-------|-----------------------------------------------|
| <span data-ttu-id="88ced-266">0</span><span class="sxs-lookup"><span data-stu-id="88ced-266">0</span></span>     | <span data-ttu-id="88ced-267">**MF Sample Extension \_** Zeilen Sprung  =  **true**</span><span class="sxs-lookup"><span data-stu-id="88ced-267">**MFSampleExtension\_Interlaced** = **TRUE**</span></span>  |
| <span data-ttu-id="88ced-268">1</span><span class="sxs-lookup"><span data-stu-id="88ced-268">1</span></span>     | <span data-ttu-id="88ced-269">**MF Sample Extension \_** Zeilen Sprung  =  **false**</span><span class="sxs-lookup"><span data-stu-id="88ced-269">**MFSampleExtension\_Interlaced** = **FALSE**</span></span> |



 

<span data-ttu-id="88ced-270">**Oberstes \_ Feld \_ zuerst**</span><span class="sxs-lookup"><span data-stu-id="88ced-270">**top\_field\_first**</span></span>



| <span data-ttu-id="88ced-271">Wert</span><span class="sxs-lookup"><span data-stu-id="88ced-271">Value</span></span> | <span data-ttu-id="88ced-272">Sample-Attribut</span><span class="sxs-lookup"><span data-stu-id="88ced-272">Sample Attribute</span></span>                                    |
|-------|-----------------------------------------------------|
| <span data-ttu-id="88ced-273">0</span><span class="sxs-lookup"><span data-stu-id="88ced-273">0</span></span>     | <span data-ttu-id="88ced-274">**MF Sample Extension \_ Bottomfieldfirst**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="88ced-274">**MFSampleExtension\_BottomFieldFirst** = **TRUE**</span></span>  |
| <span data-ttu-id="88ced-275">1</span><span class="sxs-lookup"><span data-stu-id="88ced-275">1</span></span>     | <span data-ttu-id="88ced-276">**MF Sample Extension \_ Bottomfieldfirst**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="88ced-276">**MFSampleExtension\_BottomFieldFirst** = **FALSE**</span></span> |



 

<span data-ttu-id="88ced-277">**\_erstes \_ Feld wiederholen**</span><span class="sxs-lookup"><span data-stu-id="88ced-277">**repeat\_first\_field**</span></span>



| <span data-ttu-id="88ced-278">Wert</span><span class="sxs-lookup"><span data-stu-id="88ced-278">Value</span></span> | <span data-ttu-id="88ced-279">Sample-Attribut</span><span class="sxs-lookup"><span data-stu-id="88ced-279">Sample Attribute</span></span>                                    |
|-------|-----------------------------------------------------|
| <span data-ttu-id="88ced-280">0</span><span class="sxs-lookup"><span data-stu-id="88ced-280">0</span></span>     | <span data-ttu-id="88ced-281">**MF Sample Extension \_ Repeatfirstfield**  =  **false**</span><span class="sxs-lookup"><span data-stu-id="88ced-281">**MFSampleExtension\_RepeatFirstField** = **FALSE**</span></span> |
| <span data-ttu-id="88ced-282">1</span><span class="sxs-lookup"><span data-stu-id="88ced-282">1</span></span>     | <span data-ttu-id="88ced-283">**MF Sample Extension \_ Repeatfirstfield**  =  **true**</span><span class="sxs-lookup"><span data-stu-id="88ced-283">**MFSampleExtension\_RepeatFirstField** = **TRUE**</span></span>  |



 

## <a name="single-field-samples"></a><span data-ttu-id="88ced-284">Single-Field Beispiele</span><span class="sxs-lookup"><span data-stu-id="88ced-284">Single-Field Samples</span></span>

<span data-ttu-id="88ced-285">Wenn der Medientyp MF videointerlace \_ fieldsingleupperor MF videointerlace \_ fieldsinglelower ist, bedeutet dies, dass jedes Beispiel ein einzelnes Feld enthält.</span><span class="sxs-lookup"><span data-stu-id="88ced-285">If the media type is MFVideoInterlace\_FieldSingleUpper or MFVideoInterlace\_FieldSingleLower, it means that each sample contains a single field.</span></span> <span data-ttu-id="88ced-286">Der Medientyp beschreibt jedoch den gesamten Frame.</span><span class="sxs-lookup"><span data-stu-id="88ced-286">However, the media type describes the entire frame.</span></span> <span data-ttu-id="88ced-287">Daher enthält jeder Puffer nur die Hälfte der Anzahl der Feld Zeilen, die im Medientyp angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="88ced-287">Therefore, each buffer contains only half the number of field lines given in the media type.</span></span> <span data-ttu-id="88ced-288">Wenn der Medientyp z. b. das Video als 720 × 480 beschreibt, enthält jedes Feld 240 Scan Zeilen, und jeder Puffer enthält daher nur 240 Zeilen von Pixeln.</span><span class="sxs-lookup"><span data-stu-id="88ced-288">For example, if the media type describes the video as 720 × 480, each field contains 240 scan lines, and therefore each buffer contains only 240 rows of pixels.</span></span> <span data-ttu-id="88ced-289">Wenn Sie eine Komponente schreiben, die Medientypen mit Einzel Feld Beispielen annimmt, müssen Sie diese Tatsache berücksichtigen, wenn Sie auf die Daten im Puffer zugreifen.</span><span class="sxs-lookup"><span data-stu-id="88ced-289">If you write a component that accepts media types with single-field samples, you must take this fact into account when you access the data in the buffer.</span></span>

<span data-ttu-id="88ced-290">Die gleiche Regel gilt für den geometrischen Aperture ("[MF \_ MT \_ geometrischen \_ Aperture](mf-mt-geometric-aperture-attribute.md) "-Attribut) und die minimale Anzeige Öffnung ("MF MT"-Attribut der[ \_ \_ minimalen \_ Anzeige \_ Öffnung](mf-mt-minimum-display-aperture-attribute.md) ).</span><span class="sxs-lookup"><span data-stu-id="88ced-290">The same rule applies to the geometric aperture ([MF\_MT\_GEOMETRIC\_APERTURE](mf-mt-geometric-aperture-attribute.md) attribute) and minimum display aperture ([MF\_MT\_MINIMUM\_DISPLAY\_APERTURE](mf-mt-minimum-display-aperture-attribute.md) attribute).</span></span> <span data-ttu-id="88ced-291">Diese Regionen werden in Bezug auf den gesamten Frame und nicht auf die einzelnen Felder angegeben.</span><span class="sxs-lookup"><span data-stu-id="88ced-291">These regions are specified in terms of the entire frame, not the individual fields.</span></span>

## <a name="directshow-mappings"></a><span data-ttu-id="88ced-292">DirectShow-Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="88ced-292">DirectShow Mappings</span></span>

<span data-ttu-id="88ced-293">In DirectShow ist das Sample-Zeilen Sprung-Element im **dwtypespecificflags** -Member der **am \_ SAMPLE2 \_ Properties** -Struktur enthalten.</span><span class="sxs-lookup"><span data-stu-id="88ced-293">In DirectShow, per-sample interlacing information is contained in the **dwTypeSpecificFlags** member of the **AM\_SAMPLE2\_PROPERTIES** structure.</span></span> <span data-ttu-id="88ced-294">In der folgenden Tabelle werden die entsprechenden Attribute für Media Foundation angezeigt.</span><span class="sxs-lookup"><span data-stu-id="88ced-294">The following table shows the equivalent attributes for Media Foundation.</span></span>



| <span data-ttu-id="88ced-295">DirectShow-beispielflag</span><span class="sxs-lookup"><span data-stu-id="88ced-295">DirectShow sample flag</span></span>              | <span data-ttu-id="88ced-296">Media Foundation Sample-Attribut</span><span class="sxs-lookup"><span data-stu-id="88ced-296">Media Foundation sample attribute</span></span>                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="88ced-297">überlappenden Frame mit dem \_ \_ videolflag \_ \_</span><span class="sxs-lookup"><span data-stu-id="88ced-297">AM\_VIDEO\_FLAG\_INTERLEAVED\_FRAME</span></span> | <span data-ttu-id="88ced-298">**MF Sample Extension \_ Singlefield**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="88ced-298">**MFSampleExtension\_SingleField** = **FALSE**.</span></span>                                                                                                                                    |
| <span data-ttu-id="88ced-299">AM \_ - \_ videoflag \_ FIELD1</span><span class="sxs-lookup"><span data-stu-id="88ced-299">AM\_VIDEO\_FLAG\_FIELD1</span></span>             | <span data-ttu-id="88ced-300">**MF Sample Extension \_** Zeilen Sprung "  =  **true**".</span><span class="sxs-lookup"><span data-stu-id="88ced-300">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span><br/> <span data-ttu-id="88ced-301">**MF Sample Extension \_ Singlefield**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="88ced-301">**MFSampleExtension\_SingleField** = **TRUE**.</span></span><br/> <span data-ttu-id="88ced-302">**MF Sample Extension \_ Bottomfieldfirst**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="88ced-302">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span><br/> |
| <span data-ttu-id="88ced-303">AM \_ - \_ videoflag \_ FIELD2</span><span class="sxs-lookup"><span data-stu-id="88ced-303">AM\_VIDEO\_FLAG\_FIELD2</span></span>             | <span data-ttu-id="88ced-304">**MF Sample Extension \_** Zeilen Sprung "  =  **true**".</span><span class="sxs-lookup"><span data-stu-id="88ced-304">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span><br/> <span data-ttu-id="88ced-305">**MF Sample Extension \_ Singlefield**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="88ced-305">**MFSampleExtension\_SingleField** = **TRUE**.</span></span><br/> <span data-ttu-id="88ced-306">**MF Sample Extension \_ Bottomfieldfirst**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="88ced-306">**MFSampleExtension\_BottomFieldFirst** = **TRUE**.</span></span><br/>  |
| <span data-ttu-id="88ced-307">AM \_ - \_ videoflag \_</span><span class="sxs-lookup"><span data-stu-id="88ced-307">AM\_VIDEO\_FLAG\_WEAVE</span></span>              | <span data-ttu-id="88ced-308">**MF Sample Extension \_** Zeilen Sprung  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="88ced-308">**MFSampleExtension\_Interlaced** = **FALSE**.</span></span> <span data-ttu-id="88ced-309">(Dieses Flag gibt an, dass der Treiber die beiden Felder nicht deinstalversien sollte.)</span><span class="sxs-lookup"><span data-stu-id="88ced-309">(This flag indicates that the driver should not deinterlace the two fields.)</span></span>                                                        |
| <span data-ttu-id="88ced-310">AM \_ - \_ videoflag \_ FIELD1FIRST</span><span class="sxs-lookup"><span data-stu-id="88ced-310">AM\_VIDEO\_FLAG\_FIELD1FIRST</span></span>        | <span data-ttu-id="88ced-311">**MF Sample Extension \_ Bottomfieldfirst**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="88ced-311">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span> <span data-ttu-id="88ced-312">Wenn der Inhalt mit Zeilen Sprung versehen ist und das Flag "am \_ Video \_ Flag \_ FIELD1FIRST" nicht vorhanden ist, legen Sie dieses Attribut auf " **true**" fest.</span><span class="sxs-lookup"><span data-stu-id="88ced-312">If the content is interlaced and the AM\_VIDEO\_FLAG\_FIELD1FIRST flag is not present, set this attribute to **TRUE**.</span></span>        |
| <span data-ttu-id="88ced-313">\_ \_ \_ Textfeld zum Wiederholen von \_ textflags</span><span class="sxs-lookup"><span data-stu-id="88ced-313">AM\_VIDEO\_FLAG\_REPEAT\_FIELD</span></span>      | <span data-ttu-id="88ced-314">**MF Sample Extension \_ Repeatfirstfield**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="88ced-314">**MFSampleExtension\_RepeatFirstField** = **TRUE**.</span></span> <span data-ttu-id="88ced-315">\_ \_ \_ \_ Legen Sie dieses Attribut auf " **false**" fest, wenn das Feld Flag zum Wiederholen des Felds mit der Markierung nicht vorhanden ist</span><span class="sxs-lookup"><span data-stu-id="88ced-315">If the AM\_VIDEO\_FLAG\_REPEAT\_FIELD flag is not present, set this attribute to **FALSE**.</span></span>                                    |



 

<span data-ttu-id="88ced-316">Wenn das DirectShow-Beispiel keine beispielflags enthält, verwenden Sie den Wert von **dwinterlaceflags** aus der **VIDEOINFOHEADER2** -Struktur:</span><span class="sxs-lookup"><span data-stu-id="88ced-316">If the DirectShow sample does not contain sample flags, use the value of **dwInterlaceFlags** from the **VIDEOINFOHEADER2** structure:</span></span>



| <span data-ttu-id="88ced-317">DirectShow-damit-Flag</span><span class="sxs-lookup"><span data-stu-id="88ced-317">DirectShow interlace flag</span></span>    | <span data-ttu-id="88ced-318">Media Foundation Sample-Attribut</span><span class="sxs-lookup"><span data-stu-id="88ced-318">Media Foundation sample attribute</span></span>                    |
|------------------------------|------------------------------------------------------|
| <span data-ttu-id="88ced-319">Aminterlace \_ isinterschnür</span><span class="sxs-lookup"><span data-stu-id="88ced-319">AMINTERLACE\_IsInterlaced</span></span>    | <span data-ttu-id="88ced-320">**MF Sample Extension \_** Zeilen Sprung "  =  **true**".</span><span class="sxs-lookup"><span data-stu-id="88ced-320">**MFSampleExtension\_Interlaced** = **TRUE**.</span></span>        |
| <span data-ttu-id="88ced-321">Aminterlace \_ 1fieldpersample</span><span class="sxs-lookup"><span data-stu-id="88ced-321">AMINTERLACE\_1FieldPerSample</span></span> | <span data-ttu-id="88ced-322">**MF Sample Extension \_ Singlefield**  =  **true**.</span><span class="sxs-lookup"><span data-stu-id="88ced-322">**MFSampleExtension\_SingleField** = **TRUE**.</span></span>       |
| <span data-ttu-id="88ced-323">Aminterlace \_ Field1First</span><span class="sxs-lookup"><span data-stu-id="88ced-323">AMINTERLACE\_Field1First</span></span>     | <span data-ttu-id="88ced-324">**MF Sample Extension \_ Bottomfieldfirst**  =  **false**.</span><span class="sxs-lookup"><span data-stu-id="88ced-324">**MFSampleExtension\_BottomFieldFirst** = **FALSE**.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="88ced-325">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="88ced-325">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88ced-326">Video Medientypen</span><span class="sxs-lookup"><span data-stu-id="88ced-326">Video Media Types</span></span>](video-media-types.md)
</dt> <dt>

[<span data-ttu-id="88ced-327">Medientypen</span><span class="sxs-lookup"><span data-stu-id="88ced-327">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




