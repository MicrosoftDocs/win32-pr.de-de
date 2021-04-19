---
title: Stichprobenerweiterungstypen
description: Stichprobenerweiterungstypen
ms.assetid: 8de2e003-cb21-4be9-bcde-7f5909b6260a
keywords:
- Windows Media-Format-SDK, Beispiel Erweiterungen
- Advanced Systems Format (ASF), Beispiel Erweiterungen
- ASF (Advanced Systems Format), Beispiel Erweiterungen
- Windows Media-Format-SDK, Dateneinheiten Erweiterungen
- Advanced Systems Format (ASF), Dateneinheiten Erweiterungen
- ASF (Advanced Systems Format), Dateneinheiten Erweiterungen
- Windows Media-Format-SDK, Puffer Eigenschaften
- Advanced Systems Format (ASF), Puffer Eigenschaften
- ASF (Advanced Systems Format), Puffer Eigenschaften
- Beispiel Erweiterungen, Typen
- Dateneinheiten Erweiterungen, Typen
- Puffer Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 972e3da1ecaad277158bb270cc358436f53db9e2
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2020
ms.locfileid: "106342121"
---
# <a name="sample-extension-types"></a><span data-ttu-id="28651-115">Stichprobenerweiterungstypen</span><span class="sxs-lookup"><span data-stu-id="28651-115">Sample Extension Types</span></span>

<span data-ttu-id="28651-116">Beispiel Erweiterungen, die auch als Dateneinheiten Erweiterungen (Gebühren) oder Puffer Eigenschaften bezeichnet werden, sind Elemente von Daten, die an die Medien Beispiele im Data-Abschnitt der ASF-Datei angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="28651-116">Sample extensions, also called data unit extensions (DUEs) or buffer properties, are items of data that are attached to the media samples in the data section of the ASF file.</span></span> <span data-ttu-id="28651-117">Verschiedene Typen von Beispiel Erweiterungen werden im Windows Media-Format-SDK definiert.</span><span class="sxs-lookup"><span data-stu-id="28651-117">Several types of sample extensions are defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="28651-118">Sie können auch eigene Erweiterungs Typen erstellen.</span><span class="sxs-lookup"><span data-stu-id="28651-118">You can also create your own extension types.</span></span>

<span data-ttu-id="28651-119">Um Beispiel Erweiterungen zu verwenden, müssen Sie den Erweiterungstyp in den Datenstrom-Konfigurationsdaten des Profils angeben.</span><span class="sxs-lookup"><span data-stu-id="28651-119">To use sample extensions, you must identify the extension type in the stream configuration data of the profile.</span></span> <span data-ttu-id="28651-120">Aufrufen der [**IWMStreamConfig2:: adddataunitextension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) -Methode zum Konfigurieren eines Datenstroms, um Beispiele mit erweiterten Daten zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="28651-120">Call the [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) method to configure a stream to accept samples with extended data.</span></span>

<span data-ttu-id="28651-121">Einzelne Beispiel Erweiterungen müssen den Eingabe Beispielen hinzugefügt werden, indem die [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="28651-121">Individual sample extensions must be added to the input samples by calling the [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) method.</span></span> <span data-ttu-id="28651-122">Beim Lesen von Beispielen können Sie die [**INSSBuffer3:: GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) -Methode aufrufen, um die Erweiterungs Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="28651-122">When reading samples, you can call the [**INSSBuffer3::GetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-getproperty) method to retrieve the extension data.</span></span> <span data-ttu-id="28651-123">Sie können auch die Methoden der [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) -Schnittstelle verwenden, um die an eine Stichprobe angefügten dateneinheits-Erweiterungen aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="28651-123">You can also use the methods of the [**INSSBuffer4**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer4) interface to enumerate the data unit extensions attached to a sample.</span></span>

<span data-ttu-id="28651-124">In der folgenden Tabelle werden die vordefinierten dateneinheits-Erweiterungs Bezeichner aufgelistet, und es werden die Daten beschrieben, die jeweils an Samples angefügt werden.</span><span class="sxs-lookup"><span data-stu-id="28651-124">The following table lists the predefined data unit extension identifiers, and describes the data that is attached to samples for each.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="28651-125">GUID der Beispiel Erweiterung</span><span class="sxs-lookup"><span data-stu-id="28651-125">Sample extension GUID</span></span></th>
<th><span data-ttu-id="28651-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28651-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="28651-127">WM_SampleExtensionGUID_OutputCleanPoint</span><span class="sxs-lookup"><span data-stu-id="28651-127">WM_SampleExtensionGUID_OutputCleanPoint</span></span></td>
<td><span data-ttu-id="28651-128">Die Daten zeigen an, ob das Beispiel ein <a href="wmformat-glossary.md"><em>Cleanpoint</em></a>ist.</span><span class="sxs-lookup"><span data-stu-id="28651-128">The data indicates whether the sample is a <a href="wmformat-glossary.md"><em>cleanpoint</em></a>.</span></span> <span data-ttu-id="28651-129">Der Wert 0 (null) gibt an, dass das Beispiel kein Cleanpoint ist.</span><span class="sxs-lookup"><span data-stu-id="28651-129">A value of zero indicates that the sample is not a cleanpoint.</span></span> <span data-ttu-id="28651-130">Ein Wert ungleich 0 (null) gibt an, dass es sich um einen Cleanpoint handelt.</span><span class="sxs-lookup"><span data-stu-id="28651-130">A non-zero value indicates that it is a cleanpoint.</span></span> <span data-ttu-id="28651-131">Diese Beispiel Daten-Einheits Erweiterung (Due) wird verwendet, um die Bereinigung von cleanpoints beim Schreiben von vorkomprimierten Mediendaten strömen zu verfolgen, die mit Codecs von Drittanbietern codiert wurden.</span><span class="sxs-lookup"><span data-stu-id="28651-131">This sample data unit extension (DUE) type is used to keep track of cleanpoints when writing precompressed media streams that were encoded with third-party codecs.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28651-132">WM_SampleExtensionGUID_Timecode</span><span class="sxs-lookup"><span data-stu-id="28651-132">WM_SampleExtensionGUID_Timecode</span></span></td>
<td><span data-ttu-id="28651-133">Bei den Daten handelt es sich um eine <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> Struktur, die dem Beispiel zugeordnete SMPTE-Zeit Code Daten enthält. Die Größe für diese Fälligkeit ist immer WM_SampleExtension_Timecode_Size, also 14 Bytes.</span><span class="sxs-lookup"><span data-stu-id="28651-133">The data is a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_timecode_extension_data"><strong>WMT_TIMECODE_EXTENSION_DATA</strong></a> structure containing SMPTE time code data associated with the sample.The size for this DUE is always WM_SampleExtension_Timecode_Size, which is 14 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28651-134">WM_SampleExtensionGUID_FileName</span><span class="sxs-lookup"><span data-stu-id="28651-134">WM_SampleExtensionGUID_FileName</span></span></td>
<td><span data-ttu-id="28651-135">Diese Art von Beispiel Erweiterung wird für Dateistreams verwendet.</span><span class="sxs-lookup"><span data-stu-id="28651-135">This type of sample extension is used for file streams.</span></span> <span data-ttu-id="28651-136">Die Daten in einem File Stream-Beispiel sind ein Teil einer Datendatei.</span><span class="sxs-lookup"><span data-stu-id="28651-136">The data in a file stream sample is a piece of a data file.</span></span> <span data-ttu-id="28651-137">Die Daten in der Beispiel Erweiterung geben den Namen der Datei an, aus der der Inhalt in der Stichprobe entnommen wurde. Der Dateiname ist eine Zeichenfolge mit breit Zeichen, die den Dateinamen im Name. Extension-Format ohne Pfadinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="28651-137">The data in the sample extension specifies the name of the file from which the content in the sample was taken.The file name is a wide-character string containing the file name in name.extension format without any path information.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28651-138">WM_SampleExtensionGUID_ContentType</span><span class="sxs-lookup"><span data-stu-id="28651-138">WM_SampleExtensionGUID_ContentType</span></span></td>
<td><span data-ttu-id="28651-139">Die Daten identifizieren den Inhaltstyp, den das Beispiel enthält.</span><span class="sxs-lookup"><span data-stu-id="28651-139">The data identifies the type of content that the sample contains.</span></span> <span data-ttu-id="28651-140">Diese Art von Beispiel Erweiterung wird mit Zeilen Sprung-Videostreams verwendet. Bei allen Zeilen Sprung Inhalten wird das WM_CT_INTERLACED-Flag zusammen mit einem bitweisen <strong>or</strong> mit WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST oder WM_CT_REPEAT_FIRST_FIELD verwendet.</span><span class="sxs-lookup"><span data-stu-id="28651-140">This type of sample extension is used with interlaced video streams.All interlaced content uses the WM_CT_INTERLACED flag combined by a bitwise <strong>OR</strong> with either WM_CT_BOTTOM_FIELD_FIRST, WM_CT_TOP_FIELD_FIRST, or WM_CT_REPEAT_FIRST_FIELD.</span></span><br/> <span data-ttu-id="28651-141">Die Feld Reihenfolge wird nicht im Codierungsprozess verwendet, sondern mit den komprimierten Beispielen verwaltet, sodass Sie an die renderinghardware übermittelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="28651-141">The field order is not used in the encoding process, but is maintained with the compressed samples so that it can be passed to the rendering hardware.</span></span> <span data-ttu-id="28651-142">Durch die Wiedergabe von Zeilen Sprung Inhalt mit der falschen Feld Reihenfolge werden Artefakte wie Motion Jitter im Video eingeführt.</span><span class="sxs-lookup"><span data-stu-id="28651-142">Playing interlaced content with the incorrect field order introduces artifacts such as motion jitter in the video.</span></span><br/> <span data-ttu-id="28651-143">Die Größe für diese Fälligkeit ist immer WM_SampleExtension_ContentType_Size.</span><span class="sxs-lookup"><span data-stu-id="28651-143">The size for this DUE is always WM_SampleExtension_ContentType_Size.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28651-144">WM_SampleExtensionGUID_PixelAspectRatio</span><span class="sxs-lookup"><span data-stu-id="28651-144">WM_SampleExtensionGUID_PixelAspectRatio</span></span></td>
<td><span data-ttu-id="28651-145">Die Daten zeigen das Pixel Seitenverhältnis des Inhalts in der Stichprobe an.</span><span class="sxs-lookup"><span data-stu-id="28651-145">The data indicates the pixel aspect ratio of the content in the sample.</span></span> <span data-ttu-id="28651-146">Dies gilt nur für Videos. Dieser Erweiterungstyp wird verwendet, um das Seitenverhältnis von nicht quadratischen Pixeln zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="28651-146">This applies only to video.This extension type is used to identify the aspect ratio of non-square pixels.</span></span> <span data-ttu-id="28651-147">Weitere Informationen finden <a href="to-read-and-write-video-streams-with-non-square-pixels.md">Sie unter so lesen und schreiben Sie Videostreams mit nicht quadratischen Pixeln</a>.</span><span class="sxs-lookup"><span data-stu-id="28651-147">For more information, see <a href="to-read-and-write-video-streams-with-non-square-pixels.md">To Read and Write Video Streams with Non-Square Pixels</a>.</span></span><br/> <span data-ttu-id="28651-148">Seitenverhältnis Werte werden als Wort gespeichert, dessen niedriges Byte der X-Aspekt und dessen hohes Byte der Y-Aspekt ist.</span><span class="sxs-lookup"><span data-stu-id="28651-148">Aspect ratio values are stored as a word whose low byte is the X aspect and whose high byte is the Y aspect.</span></span> <span data-ttu-id="28651-149">Beispielsweise wird 16:9 als 0x0910 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="28651-149">For example, 16:9 is stored as 0x0910.</span></span><br/> <span data-ttu-id="28651-150">Die Größe für diese Fälligkeit ist immer WM_SampleExtension_PixelAspectRatio_Size, d. h. 2 Bytes.</span><span class="sxs-lookup"><span data-stu-id="28651-150">The size for this DUE is always WM_SampleExtension_PixelAspectRatio_Size, which is 2 bytes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28651-151">WM_SampleExtensionGUID_SampleDuration</span><span class="sxs-lookup"><span data-stu-id="28651-151">WM_SampleExtensionGUID_SampleDuration</span></span></td>
<td><span data-ttu-id="28651-152">Die Daten zeigen die Dauer (in Millisekunden) des im Buffer-Objekt enthaltenen Beispiels an.</span><span class="sxs-lookup"><span data-stu-id="28651-152">The data indicates the duration, in milliseconds, of the sample contained in the buffer object.</span></span> <span data-ttu-id="28651-153">Wenn bei der Wiedergabe diese Einstellung festgelegt ist, wird Sie vom Reader-Objekt zum Überschreiben des vorhandenen Sample Duration-Werts verwendet. Dieser Wert wird automatisch durch die SDK-Laufzeitkomponenten in Videostreams mit Bitraten von 100 kbit/s oder höher festgelegt, wobei der Aufwand der fälligen Informationen nicht signifikant ist.</span><span class="sxs-lookup"><span data-stu-id="28651-153">On playback, if this DUE is set the reader object will use it to overwrite the existing sample duration value.This DUE is set automatically by the SDK run-time components on video streams with bit rates of 100 kbps or greater, where the overhead of the DUE information is not significant.</span></span> <span data-ttu-id="28651-154">Sie ist nicht für Streams mit Bitraten unter 100 kbit/s festgelegt.</span><span class="sxs-lookup"><span data-stu-id="28651-154">It is not set for streams with bit rates under 100 kbps.</span></span> <span data-ttu-id="28651-155">Anwendungen sollten diesen Wert nicht manuell festlegen, da der Writer (bei hochbitrate-Streams) den Wert mit seinen eigenen Daten überschreibt.</span><span class="sxs-lookup"><span data-stu-id="28651-155">Applications should not set this DUE manually because the writer (on high-bit-rate streams) will overwrite the value with its own data.</span></span><br/> <span data-ttu-id="28651-156">Die Größe für diese Fälligkeit ist immer WM_SampleExtension_SampleDuration_Size, d. h. 2 Bytes.</span><span class="sxs-lookup"><span data-stu-id="28651-156">The size for this DUE is always WM_SampleExtension_SampleDuration_Size, which is 2 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28651-157">WM_SampleExtensionGUID_ChromaLocation</span><span class="sxs-lookup"><span data-stu-id="28651-157">WM_SampleExtensionGUID_ChromaLocation</span></span></td>
<td><span data-ttu-id="28651-158">Die Daten geben den Typ der Chroma-Unterstichprobe an, die im I420-Videoformat verwendet wird. Der Wert dieser Erweiterung wird auf einen der folgenden Werte festgelegt:</span><span class="sxs-lookup"><span data-stu-id="28651-158">The data indicates the type of chroma subsampling used in the I420 video format.The value of this extension is set to one of the follow values:</span></span><br/>
<ul>
<li><span data-ttu-id="28651-159">WM_CL_INTERLACED420</span><span class="sxs-lookup"><span data-stu-id="28651-159">WM_CL_INTERLACED420</span></span></li>
<li><span data-ttu-id="28651-160">WM_CL_PROGRESSIVE420</span><span class="sxs-lookup"><span data-stu-id="28651-160">WM_CL_PROGRESSIVE420</span></span></li>
</ul>
<span data-ttu-id="28651-161">Diese Dateneinheiten Erweiterung ist im Profil nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="28651-161">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="28651-162">Es ist in der Beispielausgabe des Decoders enthalten.</span><span class="sxs-lookup"><span data-stu-id="28651-162">It is included in samples output from the decoder.</span></span><br/> <span data-ttu-id="28651-163">Die Größe dieses fälligen ist immer WM_SampleExtension_ChromaLocation_Size, 1 Byte.</span><span class="sxs-lookup"><span data-stu-id="28651-163">The size of this DUE is always WM_SampleExtension_ChromaLocation_Size, which is 1 byte.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28651-164">WM_SampleExtensionGUID_ColorSpaceInfo</span><span class="sxs-lookup"><span data-stu-id="28651-164">WM_SampleExtensionGUID_ColorSpaceInfo</span></span></td>
<td><span data-ttu-id="28651-165">Die Daten enthalten Informationen über den für den aktuellen Videoframe verwendeten Farbraum. Der Wert dieser Erweiterung ist eine <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> Struktur.</span><span class="sxs-lookup"><span data-stu-id="28651-165">The data provides information about the color space used for the current video frame.The value of this extension is a <a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_colorspaceinfo_extension_data"><strong>WMT_COLORSPACEINFO_EXTENSION_DATA</strong></a> structure.</span></span><br/> <span data-ttu-id="28651-166">Diese Dateneinheiten Erweiterung ist im Profil nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="28651-166">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="28651-167">Es ist in der Beispielausgabe des Decoders enthalten.</span><span class="sxs-lookup"><span data-stu-id="28651-167">It is included in samples output from the decoder.</span></span><br/> <span data-ttu-id="28651-168">Die Größe dieses fälligen ist immer WM_SampleExtension_ColorSpaceInfo_Size, also 3 Bytes.</span><span class="sxs-lookup"><span data-stu-id="28651-168">The size of this DUE is always WM_SampleExtension_ColorSpaceInfo_Size, which is 3 bytes.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="28651-169">WM_SampleExtensionGUID_UserDataInfo</span><span class="sxs-lookup"><span data-stu-id="28651-169">WM_SampleExtensionGUID_UserDataInfo</span></span></td>
<td><span data-ttu-id="28651-170">Bei den Daten handelt es sich um benutzerdefinierte Benutzerdaten. Die ersten vier Bytes der Daten enthalten die Größe der benutzerdefinierten Daten.</span><span class="sxs-lookup"><span data-stu-id="28651-170">The data is custom user data.The first four bytes of the data contain the size of the custom data.</span></span><br/> <span data-ttu-id="28651-171">Das nächste Byte enthält den Typ der Benutzerdaten, die in der Beispiel Erweiterung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="28651-171">The next byte contains the type of user data provided in the sample extension.</span></span> <span data-ttu-id="28651-172">Die folgenden Typen werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="28651-172">The following types are supported:</span></span><br/>
<ul>
<li><span data-ttu-id="28651-173">0x1F-Sequenz Ebene-Benutzerdaten</span><span class="sxs-lookup"><span data-stu-id="28651-173">0x1F - Sequence level user data</span></span></li>
<li><span data-ttu-id="28651-174">0x1E-Benutzerdaten auf Einstiegspunkt Ebene</span><span class="sxs-lookup"><span data-stu-id="28651-174">0x1E - Entry-point level user data</span></span></li>
<li><span data-ttu-id="28651-175">0x1D-Benutzerdaten auf Frame-Ebene</span><span class="sxs-lookup"><span data-stu-id="28651-175">0x1D - Frame level user data</span></span></li>
<li><span data-ttu-id="28651-176">0x1C-Benutzerdaten auf Feldebene</span><span class="sxs-lookup"><span data-stu-id="28651-176">0x1C - Field level user data</span></span></li>
<li><span data-ttu-id="28651-177">0x1B-Benutzerdaten auf Slice-Ebene</span><span class="sxs-lookup"><span data-stu-id="28651-177">0x1B - Slice level user data</span></span></li>
</ul>
<span data-ttu-id="28651-178">Die sechsten und nachfolgenden Bytes enthalten die Benutzerdaten.</span><span class="sxs-lookup"><span data-stu-id="28651-178">The sixth and subsequent bytes contain the user data.</span></span> <span data-ttu-id="28651-179">Es gibt so viele Bytes von Benutzerdaten, wie durch die Zahl in den ersten vier Bytes angegeben.</span><span class="sxs-lookup"><span data-stu-id="28651-179">There are as many bytes of user data as specified by the number in the first four bytes.</span></span><br/> <span data-ttu-id="28651-180">Diese Dateneinheiten Erweiterung ist im Profil nicht konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="28651-180">This data unit extension is not configured in the profile.</span></span> <span data-ttu-id="28651-181">Es ist in den Beispielen enthalten, die vom Decoder ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="28651-181">It is included in samples that are output from the decoder.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="28651-182">WM_SampleExtensionGUID_SampleProtectionSalt</span><span class="sxs-lookup"><span data-stu-id="28651-182">WM_SampleExtensionGUID_SampleProtectionSalt</span></span></td>
<td><span data-ttu-id="28651-183">Die Daten werden anhand von Stichproben verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="28651-183">The data is encrypted by sample.</span></span> <span data-ttu-id="28651-184">Dieser Beispiel Erweiterungstyp wird für Inhalte verwendet, die aus einem nicht-ASF-Dateiformat und einem anderen Rechte Schutzschema als Windows Media DRM importiert werden. Beim Importieren geschützter Inhalte muss jede Stichprobe einen eindeutigen Salt-Inhalt enthalten.</span><span class="sxs-lookup"><span data-stu-id="28651-184">This sample extension type is used for content that is imported from a non-ASF file format and a rights protection scheme other than Windows Media DRM.When importing protected content, each sample must include a unique salt.</span></span> <span data-ttu-id="28651-185">In der Regel handelt es sich bei diesem Wert um einen monoton steigenden Leistungswert.</span><span class="sxs-lookup"><span data-stu-id="28651-185">Typically, this value is a monotonically increasing counter.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="28651-186">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28651-186">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28651-187">**Programmierverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="28651-187">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 





