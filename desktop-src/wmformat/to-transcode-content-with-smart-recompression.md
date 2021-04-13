---
title: So transcodieren Sie Inhalte mit intelligenter Neukomprimierung
description: So transcodieren Sie Inhalte mit intelligenter Neukomprimierung
ms.assetid: 02398462-b0a4-4a17-84e3-4c6f9f26639f
keywords:
- Windows Media-Format-SDK, Transcodierung von Inhalten
- Windows Media-Format-SDK, intelligente Neukomprimierung
- SDK für Windows Media-Format, Neukomprimierung
- Windows Media-Format-SDK, Windows Media Audio Codecs
- Advanced Systems Format (ASF), Transcodierung von Inhalten
- ASF (Advanced Systems Format), Transcodierung von Inhalten
- Advanced Systems Format (ASF), intelligente Neukomprimierung
- ASF (Advanced Systems Format), intelligente Neukomprimierung
- Advanced Systems Format (ASF), Neukomprimierung
- ASF (Advanced Systems Format), erneute Komprimierung
- Advanced Systems Format (ASF), Windows Media Audio Codecs
- ASF (Advanced Systems Format), Windows Media Audio Codecs
- Transcodieren von Inhalten
- intelligente Neukomprimierung
- Neukomprimierung
- Windows Media Audio Codecs, Transcodierung von Inhalten
- Codecs, Windows Media Audio Codecs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a1317989ea9384d4a9747d712af1ce5c61d484c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104314291"
---
# <a name="to-transcode-content-with-smart-recompression"></a><span data-ttu-id="a78a7-120">So transcodieren Sie Inhalte mit intelligenter Neukomprimierung</span><span class="sxs-lookup"><span data-stu-id="a78a7-120">To Transcode Content with Smart Recompression</span></span>

<span data-ttu-id="a78a7-121">Mithilfe des SDK für den Windows Media-Format können Sie Inhalte von einer Bitrate in eine andere transcodieren.</span><span class="sxs-lookup"><span data-stu-id="a78a7-121">You can transcode content from one bit rate to another using the Windows Media Format SDK.</span></span> <span data-ttu-id="a78a7-122">Normalerweise besteht dies darin, den Inhalt einfach zu decodieren und erneut in die gewünschte Bitrate zu codieren.</span><span class="sxs-lookup"><span data-stu-id="a78a7-122">Normally, this involves simply decoding the content and encoding it again to the desired bit rate.</span></span> <span data-ttu-id="a78a7-123">Der Windows Media Audio 9-Codec unterstützt die intelligente Neukomprimierung, die eine bessere Qualität als normale ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="a78a7-123">The Windows Media Audio 9 codec supports smart recompression, which enables transcoding that achieves better quality than normal.</span></span>

<span data-ttu-id="a78a7-124">Bei der intelligenten Neukomprimierung muss der ursprüngliche Audiostream mit dem Windows Media Audio Codec codiert werden.</span><span class="sxs-lookup"><span data-stu-id="a78a7-124">For smart recompression, the original audio stream must be encoded with the Windows Media Audio codec.</span></span> <span data-ttu-id="a78a7-125">Alle Codec-Versionen werden unterstützt, aber die spezialisierten audiovercodecs (Windows Media Audio 9 Professional und Windows Media Audio 9 Voice) nicht.</span><span class="sxs-lookup"><span data-stu-id="a78a7-125">All versions of the codec are supported, but the specialized audio codecs (Windows Media Audio 9 Professional and Windows Media Audio 9 Voice) are not.</span></span> <span data-ttu-id="a78a7-126">Wenn die ursprüngliche Audiodatei mit dem Windows Media Audio 9-Codec ohne Verlust verwendet wurde, ist die Verwendung intelligenter Neukomprimierung nicht erforderlich, da keine Informationen in der ursprünglichen Codierung verloren gegangen sind.</span><span class="sxs-lookup"><span data-stu-id="a78a7-126">If the original audio was encoded with the Windows Media Audio 9 Lossless codec, there is no need to use smart recompression, because no information was lost in the original encoding.</span></span>

<span data-ttu-id="a78a7-127">Führen Sie die folgenden Schritte aus, um die intelligente Neukomprimierung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a78a7-127">To use smart recompression, perform the following steps.</span></span>

1.  <span data-ttu-id="a78a7-128">Richten Sie ein Reader-Objekt mit der Quelldatei zum Lesen ein.</span><span class="sxs-lookup"><span data-stu-id="a78a7-128">Set up a reader object with the source file for reading.</span></span> <span data-ttu-id="a78a7-129">Weitere Informationen finden Sie unter [Lesen von ASF-Dateien](reading-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="a78a7-129">For more information, see [Reading ASF Files](reading-asf-files.md).</span></span>
2.  <span data-ttu-id="a78a7-130">Richten Sie ein Writer-Objekt ein, das zum transcodieren der Datei verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a78a7-130">Set up a writer object to use for transcoding the file.</span></span> <span data-ttu-id="a78a7-131">Legen Sie den Dateinamen für die neue Datei fest.</span><span class="sxs-lookup"><span data-stu-id="a78a7-131">Set the file name for the new file.</span></span> <span data-ttu-id="a78a7-132">Wählen Sie ein Profil aus, das für die neue Datei verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a78a7-132">Select a profile to use for the new file.</span></span> <span data-ttu-id="a78a7-133">Legen Sie das ausgewählte Profil im Writer-Objekt fest.</span><span class="sxs-lookup"><span data-stu-id="a78a7-133">Set the selected profile in the writer object.</span></span> <span data-ttu-id="a78a7-134">Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien](writing-asf-files.md).</span><span class="sxs-lookup"><span data-stu-id="a78a7-134">For more information, see [Writing ASF Files](writing-asf-files.md).</span></span>
3.  <span data-ttu-id="a78a7-135">Abrufen eines Zeigers auf die [**iwmprofile**](iwmprofile.md) -Schnittstelle des Reader-Objekts durch Aufrufen von **iwmreader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="a78a7-135">Get a pointer to the [**IWMProfile**](iwmprofile.md) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
4.  <span data-ttu-id="a78a7-136">Rufen Sie die [**iwmstreamconfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) -Schnittstelle für den Audiostream ab, der durch Aufrufen von [**iwmprofile:: GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream)transcodiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a78a7-136">Retrieve the [**IWMStreamConfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig) interface for the audio stream to be transcoded by calling [**IWMProfile::GetStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmprofile-getstream).</span></span>
5.  <span data-ttu-id="a78a7-137">Rufen Sie die [**iwmmediarequicenschnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) für das Datenstrom-Konfigurationsobjekt ab, indem Sie **iwmstreamconfig:: QueryInterface** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a78a7-137">Get the [**IWMMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops) interface for the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
6.  <span data-ttu-id="a78a7-138">Rufen Sie die [**WM- \_ \_ Medientyp**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) Struktur für den Stream ab, indem Sie zwei Aufrufe an [**iwmmedia-Eigenschaften:: getmediatype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype)durchführen.</span><span class="sxs-lookup"><span data-stu-id="a78a7-138">Retrieve the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure for the stream by making two calls to [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype).</span></span> <span data-ttu-id="a78a7-139">Abrufen der Größe der Struktur beim ersten-Befehl und Zuweisen von Arbeitsspeicher für einen Puffer, der beim zweiten-Befehl übergeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="a78a7-139">Get the size of the structure on the first call, and allocate memory for a buffer to pass on the second call.</span></span>
7.  <span data-ttu-id="a78a7-140">Rufen Sie einen Zeiger auf die [**iwminputmedia-**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) Oberfläche für die Eingabe im Writer auf, indem Sie [**iwmwriter:: GetInput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)Eigenschaften aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a78a7-140">Get a pointer to the [**IWMInputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) interface for the input in the writer by calling [**IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops).</span></span>
8.  <span data-ttu-id="a78a7-141">Rufen Sie die [**iwmpropertyvault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) -Schnittstelle für das Eingabemedien Eigenschaften-Objekt durch Aufrufen von **iwminputmediaproperties:: QueryInterface** ab.</span><span class="sxs-lookup"><span data-stu-id="a78a7-141">Get the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface for the input media properties object by calling **IWMInputMediaProps::QueryInterface**.</span></span>
9.  <span data-ttu-id="a78a7-142">Verwenden Sie die [**iwmpropertyvault:: SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) -Methode, um die \_ Eigenschaft g wszoriginalwaveformat festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a78a7-142">Use the [**IWMPropertyVault::SetProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmpropertyvault-setproperty) method to set the g\_wszOriginalWaveFormat property.</span></span> <span data-ttu-id="a78a7-143">Verwenden Sie die in Schritt 6 erhaltene **WaveFormatEx** -Struktur als Wert der-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="a78a7-143">Use the **WAVEFORMATEX** structure obtained in step 6 as the value of the property.</span></span>
10. <span data-ttu-id="a78a7-144">Schließen Sie die an den Eingabemedien Eigenschaften vorgenommenen Änderungen ein, indem Sie [**iwmwriter:: mentinputtial**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) aufrufen und einen Zeiger auf die **iwminputmediaproperties** -Schnittstelle übergeben.</span><span class="sxs-lookup"><span data-stu-id="a78a7-144">Include changes made to the input media properties by calling [**IWMWriter::SetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setinputprops) and passing it a pointer to the **IWMInputMediaProps** interface.</span></span>
11. <span data-ttu-id="a78a7-145">Beginnen Sie mit dem Lesen von Beispielen aus der ursprünglichen Datei, und übergeben Sie Sie mit Aufrufen von [**iwmwriter:: Write-ample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample)an den Writer.</span><span class="sxs-lookup"><span data-stu-id="a78a7-145">Begin reading samples from the original file and passing them to the writer with calls to [**IWMWriter::WriteSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-writesample).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a78a7-146">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a78a7-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a78a7-147">**Erweiterte Themen**</span><span class="sxs-lookup"><span data-stu-id="a78a7-147">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="a78a7-148">**Iwminputmediarequiterschnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a78a7-148">**IWMInputMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops)
</dt> <dt>

[<span data-ttu-id="a78a7-149">**Iwmmedia-Eigenschaften Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a78a7-149">**IWMMediaProps Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmediaprops)
</dt> <dt>

[<span data-ttu-id="a78a7-150">**Iwmprofile-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a78a7-150">**IWMProfile Interface**</span></span>](iwmprofile.md)
</dt> <dt>

[<span data-ttu-id="a78a7-151">**Iwmpropertyvault-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a78a7-151">**IWMPropertyVault Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault)
</dt> <dt>

[<span data-ttu-id="a78a7-152">**Iwmstreamconfig-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a78a7-152">**IWMStreamConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig)
</dt> </dl>

 

 




