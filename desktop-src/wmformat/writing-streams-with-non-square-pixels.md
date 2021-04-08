---
title: Schreiben von Streams mit nicht quadratischen Pixeln
description: Schreiben von Streams mit nicht quadratischen Pixeln
ms.assetid: 4af7dedc-e2b8-4dc2-add4-84424e93c297
keywords:
- Windows Media-Format-SDK, Schreiben von Videostreams
- Windows Media-Format-SDK, Videostreams
- Windows Media-Format-SDK, nicht eckige Pixel
- Windows Media-Format-SDK, Pixel (ohne Quadrat)
- Advanced Systems Format (ASF), Schreiben von Videostreams
- ASF (Advanced Systems Format), Schreiben von Videostreams
- Advanced Systems Format (ASF), Videostreams
- ASF (Advanced Systems Format), Videostreams
- Advanced Systems Format (ASF), nicht quadratische Pixel
- ASF (Advanced Systems Format), nicht eckige Pixel
- Advanced Systems Format (ASF), Pixel (ohne Quadrat)
- ASF (Advanced Systems Format), Pixel (ohne Quadrat)
- Schreiben von Videostreams
- Videostreams, schreiben
- Videostreams, nicht quadratische Pixel
- nicht quadratische Pixel
- Pixel (nicht quadratisch)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1349840f151ab787ba0e0512cfab8fea08aacf1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038549"
---
# <a name="writing-streams-with-non-square-pixels"></a><span data-ttu-id="38772-120">Schreiben von Streams mit nicht quadratischen Pixeln</span><span class="sxs-lookup"><span data-stu-id="38772-120">Writing Streams with Non-Square Pixels</span></span>

<span data-ttu-id="38772-121">Es gibt zwei Möglichkeiten, Videostreams mit nicht quadratischen Pixeln zu erstellen, die in Windows-Media Player ordnungsgemäß angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="38772-121">There are two ways to create video streams with non-square pixels that will be displayed correctly in Windows Media Player.</span></span> <span data-ttu-id="38772-122">Das erste Verfahren umfasst das Festlegen von Attributen auf Streamebene im Dateiheader.</span><span class="sxs-lookup"><span data-stu-id="38772-122">The first technique involves setting stream-level attributes in the file header.</span></span> <span data-ttu-id="38772-123">Das zweite Verfahren umfasst das Hinzufügen einer Dateneinheiten Erweiterung zu einem Stream im Profil und das anschließende Festlegen eines Werts für die Erweiterung in jedem geschriebenen Beispiel.</span><span class="sxs-lookup"><span data-stu-id="38772-123">The second technique involves adding a data unit extension to a stream in the profile, and then setting a value for it in every sample that is written.</span></span>

## <a name="to-use-stream-level-header-attributes-to-set-pixel-aspect-ratio"></a><span data-ttu-id="38772-124">So verwenden Sie Header Attribute auf Streamebene zum Festlegen des Pixel Seitenverhältnisses</span><span class="sxs-lookup"><span data-stu-id="38772-124">To Use Stream-level Header Attributes to Set Pixel Aspect Ratio</span></span>

1.  <span data-ttu-id="38772-125">Richten Sie das Writer-Objekt ein.</span><span class="sxs-lookup"><span data-stu-id="38772-125">Set up the writer object.</span></span> <span data-ttu-id="38772-126">Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="38772-126">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="38772-127">Erstellen oder laden Sie ein Profil mit einem oder mehreren Videostreams.</span><span class="sxs-lookup"><span data-stu-id="38772-127">Create or load a profile with one or more video streams.</span></span> <span data-ttu-id="38772-128">Weitere Informationen finden [Sie unter So verwenden Sie Profile mit dem Writer](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="38772-128">For more information, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
3.  <span data-ttu-id="38772-129">Nennen Sie [**iwmwriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span><span class="sxs-lookup"><span data-stu-id="38772-129">Call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span> <span data-ttu-id="38772-130">(Diese Methode wird immer aufgerufen, bevor Header Attribute festgelegt werden.)</span><span class="sxs-lookup"><span data-stu-id="38772-130">(Always call this method before setting any header attributes.)</span></span>
4.  <span data-ttu-id="38772-131">Rufen Sie **QueryInterface** auf, um die [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) -Schnittstelle zu erhalten, und rufen Sie [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) zweimal auf, um [**aspectratiox**](aspectratiox.md) und [**aspectratioy**](aspectratioy.md) als Attribute auf Streamebene des Videodaten Stroms hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="38772-131">Call **QueryInterface** to obtain the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface and call [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) twice to add [**AspectRatioX**](aspectratiox.md) and [**AspectRatioY**](aspectratioy.md) as stream-level attributes of the video stream.</span></span> <span data-ttu-id="38772-132">Diese Attribute sind **DWORD** -Werte.</span><span class="sxs-lookup"><span data-stu-id="38772-132">These attributes are **DWORD** values.</span></span>
5.  <span data-ttu-id="38772-133">Schreiben Sie die Datei.</span><span class="sxs-lookup"><span data-stu-id="38772-133">Write the file.</span></span>

## <a name="to-use-data-unit-extensions-to-set-pixel-aspect-ratio"></a><span data-ttu-id="38772-134">So verwenden Sie Dateneinheiten Erweiterungen zum Festlegen des Pixel Seitenverhältnisses</span><span class="sxs-lookup"><span data-stu-id="38772-134">To Use Data Unit Extensions to Set Pixel Aspect Ratio</span></span>

<span data-ttu-id="38772-135">**Vor dem Schreiben:**</span><span class="sxs-lookup"><span data-stu-id="38772-135">**Before writing:**</span></span>

1.  <span data-ttu-id="38772-136">Richten Sie das Writer-Objekt ein.</span><span class="sxs-lookup"><span data-stu-id="38772-136">Set up the writer object.</span></span> <span data-ttu-id="38772-137">Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="38772-137">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
2.  <span data-ttu-id="38772-138">Erstellen oder laden Sie ein Profil mit einem oder mehreren Videostreams.</span><span class="sxs-lookup"><span data-stu-id="38772-138">Create or load a profile with one or more video streams.</span></span> <span data-ttu-id="38772-139">Weitere Informationen finden [Sie unter So verwenden Sie Profile mit dem Writer](to-use-profiles-with-the-writer.md).</span><span class="sxs-lookup"><span data-stu-id="38772-139">For more information, see [To Use Profiles with the Writer](to-use-profiles-with-the-writer.md).</span></span>
3.  <span data-ttu-id="38772-140">Nennen Sie für jeden Stream (eines beliebigen Medientyps) im Profil [**iwmstreamconfig:: setstreamname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) , um einen eindeutigen Namen Ihrer Wahl anzugeben.</span><span class="sxs-lookup"><span data-stu-id="38772-140">For each stream (of any media type) in the profile, call [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) to specify a unique name of your choice.</span></span> <span data-ttu-id="38772-141">Weisen Sie zwei Streams nicht denselben Namen zu.</span><span class="sxs-lookup"><span data-stu-id="38772-141">Do not give two streams the same name.</span></span>
4.  <span data-ttu-id="38772-142">Verwenden Sie [**IWMStreamConfig2:: adddataunitextension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) im Videostream, um eine dateneinheits Erweiterung für das Pixel Seitenverhältnis hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="38772-142">Use [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) on the video stream to add a data unit extension for pixel aspect ratio.</span></span>
5.  <span data-ttu-id="38772-143">Nennen Sie [**iwmwriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span><span class="sxs-lookup"><span data-stu-id="38772-143">Call [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).</span></span>
6.  <span data-ttu-id="38772-144">Schreiben Sie die Datei.</span><span class="sxs-lookup"><span data-stu-id="38772-144">Write the file.</span></span>

<span data-ttu-id="38772-145">**Beim Schreiben:**</span><span class="sxs-lookup"><span data-stu-id="38772-145">**While writing:**</span></span>

-   <span data-ttu-id="38772-146">Geben Sie für jedes Beispiel [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) an, und geben Sie die WM \_ sampleextensionguid \_ pixelaspectratio-Eigenschaft zusammen mit dem korrekten Wert an.</span><span class="sxs-lookup"><span data-stu-id="38772-146">For each sample, call [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) and specify the WM\_SampleExtensionGUID\_PixelAspectRatio property along with the correct value.</span></span> <span data-ttu-id="38772-147">Seitenverhältnis Werte werden als zwei verketteten zweistelligen Wert geschrieben.</span><span class="sxs-lookup"><span data-stu-id="38772-147">Aspect ratio values are written as two concatenated two-digit values.</span></span> <span data-ttu-id="38772-148">Beispielsweise wird 16:9 als 1609 oder 0x0649 geschrieben.</span><span class="sxs-lookup"><span data-stu-id="38772-148">For example, 16:9 is written as 1609 or 0x0649.</span></span> <span data-ttu-id="38772-149">Dabei handelt es sich immer um einen 2-Byte-Wert.</span><span class="sxs-lookup"><span data-stu-id="38772-149">This is always a 2-byte value.</span></span>

## <a name="related-topics"></a><span data-ttu-id="38772-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="38772-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="38772-151">**So lesen und schreiben Sie Videostreams mit nicht quadratischen Pixeln**</span><span class="sxs-lookup"><span data-stu-id="38772-151">**To Read and Write Video Streams with Non-Square Pixels**</span></span>](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




