---
title: So verwenden Sie ein Zeilen Sprung Video
description: So verwenden Sie ein Zeilen Sprung Video
ms.assetid: cb77bac7-bea8-4f1b-8302-fee9a43d4815
keywords:
- Windows Media-Format-SDK, Zeilen Sprung Video
- Windows Media-Format-SDK, Videocodierung mit Zeilen Sprung
- Windows Media-Format-SDK, Codieren von verschachtelten Videos
- Windows Media-Format-SDK, Decodieren von Text mit Interlacing
- Windows Media-Format-SDK, Feld Reihenfolge
- Advanced Systems Format (ASF), Zeilen Sprung Video
- ASF (Advanced Systems Format), Zeilen Sprung Video
- Advanced Systems Format (ASF), Videocodierung mit Zeilen Sprung
- ASF (Advanced Systems Format), Video Encoding Interlacing
- Advanced Systems Format (ASF), Codieren von Zeilen Sprung Videos
- ASF (Advanced Systems Format), Codieren von Zeilen Sprung Videos
- Advanced Systems Format (ASF), Decodieren von interschnür Videos
- ASF (Advanced Systems Format), Decodieren von Zeilen Sprung Videos
- Advanced Systems Format (ASF), Feld Reihenfolge
- ASF (Advanced Systems Format), Feld Reihenfolge
- Zeilen Sprung Video, Info
- Zeilen Sprung Video, Codierung
- Zeilen Sprung Video, Decodierung
- Zeilen Sprung Video, Feld Reihenfolge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a093ddd6d9d9487ffcd4b73e1f5c75b849cdcdc1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858015"
---
# <a name="to-use-interlaced-video"></a><span data-ttu-id="6567b-122">So verwenden Sie ein Zeilen Sprung Video</span><span class="sxs-lookup"><span data-stu-id="6567b-122">To Use Interlaced Video</span></span>

<span data-ttu-id="6567b-123">Es gibt zwei grundlegende Arten der Videocodierung: progressiv und Zeilen Sprung.</span><span class="sxs-lookup"><span data-stu-id="6567b-123">There are two basic types of video encoding: progressive and interlaced.</span></span> <span data-ttu-id="6567b-124">Bei progressiver Codierung ist jeder Frame eine codierte Darstellung eines Frame Videos.</span><span class="sxs-lookup"><span data-stu-id="6567b-124">In progressive encoding, each frame is an encoded representation of one frame of video.</span></span> <span data-ttu-id="6567b-125">Bei der Zeilen Sprung Codierung ist jeder Frame eine codierte Darstellung von entweder allen geraden Zeilen des Videos oder allen ungeraden Zeilen.</span><span class="sxs-lookup"><span data-stu-id="6567b-125">In interlaced encoding, each frame is an encoded representation of either all of the even rows of pixels in the video, or all of the odd rows.</span></span> <span data-ttu-id="6567b-126">Jeder Zeilen Sprung Rahmen wird als *Feld* bezeichnet, sodass es ungerade Felder und sogar Felder gibt.</span><span class="sxs-lookup"><span data-stu-id="6567b-126">Each interlaced frame is called a *field*, so there are odd fields and even fields.</span></span> <span data-ttu-id="6567b-127">Eine Zeilen Sprung Anzeige (z. b. ein Fernsehgerät) rendert die Felder einzeln und abwechselnd Felder.</span><span class="sxs-lookup"><span data-stu-id="6567b-127">An interlaced display (like a television) renders the fields one at a time, alternating fields.</span></span> <span data-ttu-id="6567b-128">Eine progressive Anzeige rendert Frames alle gleichzeitig.</span><span class="sxs-lookup"><span data-stu-id="6567b-128">A progressive display renders frames all at once.</span></span>

<span data-ttu-id="6567b-129">Das Windows Media Video 9 Advanced Profile Codec bietet Unterstützung für die Beibehaltung von interlacings in komprimierten Datenströmen.</span><span class="sxs-lookup"><span data-stu-id="6567b-129">The Windows Media Video 9 Advanced Profile codec provides support for maintaining interlacing in compressed streams.</span></span>

## <a name="when-to-use-interlaced-video"></a><span data-ttu-id="6567b-130">Verwendung von Zeilen Sprung Videos</span><span class="sxs-lookup"><span data-stu-id="6567b-130">When to Use Interlaced Video</span></span>

<span data-ttu-id="6567b-131">Das Codieren von Zeilen Sprung Videos ist nur hilfreich, wenn der Inhalt auf einem Zeilen Sprung Gerät angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6567b-131">Encoding interlaced video is useful only when the content is displayed on an interlaced device.</span></span> <span data-ttu-id="6567b-132">Inhalte, die in einem Fernsehgerät (über eine Top-Box oder ein anderes Gerät) angezeigt werden sollen, müssen möglicherweise mit Zeilen Sprung verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="6567b-132">Content that is intended to be viewed on a television (through a set-top box or other device) may need to be interlaced.</span></span> <span data-ttu-id="6567b-133">Inhalte, die ausschließlich auf einer Computer Anzeige angezeigt werden sollen, sollten nicht als Zeilen Sprung codiert werden.</span><span class="sxs-lookup"><span data-stu-id="6567b-133">Content that is intended to be viewed exclusively on a computer display should not be encoded as interlaced.</span></span>

<span data-ttu-id="6567b-134">Zum Codieren von überlappenden Videos als progressives Video müssen Sie die Eingabeeinstellungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="6567b-134">To encode interlaced video as progressive video, you must configure input settings.</span></span> <span data-ttu-id="6567b-135">Weitere Informationen finden [Sie unter dem deinterlace-Video](to-deinterlace-video.md).</span><span class="sxs-lookup"><span data-stu-id="6567b-135">For more information, see [To Deinterlace Video](to-deinterlace-video.md).</span></span>

## <a name="field-order"></a><span data-ttu-id="6567b-136">Feldreihenfolge</span><span class="sxs-lookup"><span data-stu-id="6567b-136">Field Order</span></span>

<span data-ttu-id="6567b-137">Bei den meisten Quellen mit Zeilen Sprung Video, z. b. Video Erfassungs Karten, werden Videobeispiele bereitstellt, die beide Felder miteinander verschachtelt sind.</span><span class="sxs-lookup"><span data-stu-id="6567b-137">Most sources of interlaced video, such as video capture cards, deliver video samples that include both fields interleaved with each other.</span></span> <span data-ttu-id="6567b-138">Das Ergebnis ähnelt einem kompletten Videorahmen, mit dem Unterschied, dass die ungeraden und geraden Zeilen etwas zeitgleich verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="6567b-138">The result is like a complete frame of video, except that the odd and even lines are shifted slightly in time.</span></span> <span data-ttu-id="6567b-139">Es gibt keinen universellen Standard, zu dem das Feld im überlappenden Video Beispiel erstmalig vorkommt.</span><span class="sxs-lookup"><span data-stu-id="6567b-139">There is no universal standard as to which field in the interleaved video sample occurs first in time.</span></span>

<span data-ttu-id="6567b-140">Sie sollten es Benutzern ermöglichen, die Feld Reihenfolge anzugeben, wenn Sie überlappende Beispiele an die Anwendung übergeben.</span><span class="sxs-lookup"><span data-stu-id="6567b-140">You should enable users to specify field order when passing interlaced samples to your application.</span></span>

## <a name="encoding-interlaced-video"></a><span data-ttu-id="6567b-141">Codieren von interschnür Videos</span><span class="sxs-lookup"><span data-stu-id="6567b-141">Encoding Interlaced Video</span></span>

<span data-ttu-id="6567b-142">Führen Sie die folgenden Schritte aus, um die Zeilen Sprung Codierung zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="6567b-142">To use interlaced encoding, perform the following steps:</span></span>

1.  <span data-ttu-id="6567b-143">Konfigurieren Sie den Videostream im Profil so, dass die Inhaltstyp-Dateneinheiten Erweiterung verwendet wird, indem Sie die [**IWMStreamConfig2:: adddataunitextension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6567b-143">Configure the video stream in the profile to use the content type data unit extension by calling the [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) method.</span></span> <span data-ttu-id="6567b-144">Die Beispiel Erweiterungs-GUID für die Inhaltstyp Erweiterung ist WM \_ sampleextensionsguid \_ ContentType.</span><span class="sxs-lookup"><span data-stu-id="6567b-144">The sample extension GUID for the content type extension is WM\_SampleExtensionsGUID\_ContentType.</span></span>
2.  <span data-ttu-id="6567b-145">Legen Sie den Stream im Profil fest, und konfigurieren Sie den Writer wie gewohnt mit dem Profil.</span><span class="sxs-lookup"><span data-stu-id="6567b-145">Set the stream in the profile and configure the writer with the profile as normal.</span></span>
3.  <span data-ttu-id="6567b-146">Bevor Sie Zeilen Sprung Beispiele an den Writer übergeben, müssen Sie die [**IWMWriterAdvanced2:: setinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) -Methode aufzurufen, um die \_ Eingabe Einstellung g wszinterlacedcoding auf **true** festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6567b-146">Before passing interlaced samples to the writer, call the [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting) method to set the g\_wszInterlacedCoding input setting to **TRUE**.</span></span>
4.  <span data-ttu-id="6567b-147">Aufrufen Sie für jedes mit dem Writer übergebene Zeilen Sprung Beispiel die [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) -Methode, um den Inhaltstyp festzulegen.</span><span class="sxs-lookup"><span data-stu-id="6567b-147">For every interlaced sample that you pass to the writer, call the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method to set the content type.</span></span> <span data-ttu-id="6567b-148">Inhaltstyp Werte sind Kombinationen der Flags in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6567b-148">Content type values are combinations of the flags in the following table.</span></span>



| <span data-ttu-id="6567b-149">Flag</span><span class="sxs-lookup"><span data-stu-id="6567b-149">Flag</span></span>                         | <span data-ttu-id="6567b-150">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6567b-150">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6567b-151">Zeilen Sprung mit \_ der WM-Geschwindigkeit \_</span><span class="sxs-lookup"><span data-stu-id="6567b-151">WM\_CT\_INTERLACED</span></span>           | <span data-ttu-id="6567b-152">Legen Sie dieses Flag immer fest, wenn Sie Zeilen Sprung Inhalt codieren.</span><span class="sxs-lookup"><span data-stu-id="6567b-152">Always set this flag when encoding interlaced content.</span></span> <span data-ttu-id="6567b-153">Wenn Sie dieses Flag verwenden, ohne ein Flag für die Feld Reihenfolge festzulegen ("WM \_ CT \_ Bottom \_ Field \_ First" oder "WM \_ CT \_ Top \_ Field First" \_ ), nimmt der Codec an, dass das oberste Feld zuerst ist.</span><span class="sxs-lookup"><span data-stu-id="6567b-153">If you use this flag without setting a field-order flag (WM\_CT\_BOTTOM\_FIELD\_FIRST or WM\_CT\_TOP\_FIELD\_FIRST) the codec will assume that the top field is first.</span></span> <span data-ttu-id="6567b-154">Wenn der Codec die falsche Feld Reihenfolge verwendet, sollte die Bildqualität nicht beeinträchtigt werden, aber die Codierungseffizienz wird beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="6567b-154">If the codec uses the wrong field order, there should be no impact on image quality, but the encoding efficiency will be affected.</span></span> |
| <span data-ttu-id="6567b-155">letzte Zeile, \_ \_ \_ \_ erstes Feld</span><span class="sxs-lookup"><span data-stu-id="6567b-155">WM\_CT\_BOTTOM\_FIELD\_FIRST</span></span> | <span data-ttu-id="6567b-156">In Kombination mit dem "WM CT"- \_ \_ Zeilen Sprung Flag gibt dieses Flag an, dass das untere Feld (das Feld, das mit der zweiten Zeile im Beispiel beginnt) zum ersten Mal auftritt.</span><span class="sxs-lookup"><span data-stu-id="6567b-156">When combined with the WM\_CT\_INTERLACED flag, this flag indicates that the bottom field (the field starting with the second line in the sample) occurs first in time.</span></span>                                                                                                                                                                                          |
| <span data-ttu-id="6567b-157">\_ \_ \_ erstes erstes Feld, \_ erstes Feld</span><span class="sxs-lookup"><span data-stu-id="6567b-157">WM\_CT\_TOP\_FIELD\_FIRST</span></span>    | <span data-ttu-id="6567b-158">In Kombination mit dem "WM CT"- \_ \_ Zeilen Sprung Flag gibt dieses Flag an, dass das oberste Feld (das Feld, das mit der ersten Zeile im Beispiel beginnt) zum ersten Mal auftritt.</span><span class="sxs-lookup"><span data-stu-id="6567b-158">When combined with the WM\_CT\_INTERLACED flag, this flag indicates that the top field (the field starting with the first line in the sample) occurs first in time.</span></span>                                                                                                                                                                                              |
| <span data-ttu-id="6567b-159">WM \_ CT \_ , \_ erstes \_ Feld wiederholen</span><span class="sxs-lookup"><span data-stu-id="6567b-159">WM\_CT\_REPEAT\_FIRST\_FIELD</span></span> | <span data-ttu-id="6567b-160">Gibt an, dass das erste Feld im Beispiel bei der Wiedergabe wiederholt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6567b-160">Indicates that the first field in the sample should be repeated on playback.</span></span> <span data-ttu-id="6567b-161">Dieses Flag wird für Video verwendet, das vom telecine-Prozess aus dem Film erstellt wurde. Wenn kein Flag für die Feld Reihenfolge in Verbindung mit diesem Flag festgelegt wird, wird davon ausgegangen, dass das oberste Feld zum ersten Mal auftritt.</span><span class="sxs-lookup"><span data-stu-id="6567b-161">This flag is used for video that has created from film by the telecine process.If no field-order flag is set in conjunction with this flag, the top field is assumed to occur first in time.</span></span><br/>                                                                             |



 

> [!Note]  
> <span data-ttu-id="6567b-162">Wenn das "WM CT"-Zeilen Sprung \_ \_ Flag nicht festgelegt ist, wird angenommen, dass das Beispiel einen progressiven Videorahmen enthält.</span><span class="sxs-lookup"><span data-stu-id="6567b-162">If the WM\_CT\_INTERLACED flag is not set, the sample is assumed to contain a progressive video frame.</span></span>

 

## <a name="decoding-interlaced-video"></a><span data-ttu-id="6567b-163">Decodieren von interschnür Videos</span><span class="sxs-lookup"><span data-stu-id="6567b-163">Decoding Interlaced Video</span></span>

<span data-ttu-id="6567b-164">Beim Decodieren von Videos mit Zeilen Sprung müssen Sie die \_ Einstellung "g wszzuweisung winterlacedoutput" mithilfe der [**IWMReaderAdvanced2:: setoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) -Methode auf " **true** " festlegen.</span><span class="sxs-lookup"><span data-stu-id="6567b-164">When decoding interlaced video, you must set the g\_wszAllowInterlacedOutput setting to **TRUE** using the [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting) method.</span></span> <span data-ttu-id="6567b-165">Andernfalls liefert der Codec progressive Frames.</span><span class="sxs-lookup"><span data-stu-id="6567b-165">Otherwise the codec will deliver progressive frames.</span></span>

<span data-ttu-id="6567b-166">Die-Inhaltstyp-Dateneinheiten Erweiterung wird in den Ausgabe Beispielen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="6567b-166">The content type data unit extension is maintained on the output samples.</span></span> <span data-ttu-id="6567b-167">Sie sollten die Feld Ausrichtung an das renderinggerät übergeben, um eine ordnungsgemäße Wiedergabe sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="6567b-167">You should pass the field orientation to the rendering device to ensure proper playback.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6567b-168">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6567b-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6567b-169">**Erweiterte Themen**</span><span class="sxs-lookup"><span data-stu-id="6567b-169">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> </dl>

 

 





