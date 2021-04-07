---
title: Lesen von Multichannel-Audiodateien
description: Lesen von Multichannel-Audiodateien
ms.assetid: 9d577c5c-7275-493e-8a77-318c264b59b3
keywords:
- Windows Media Format SDK, Lesen von Multichannel-Audiodaten
- Advanced Systems Format (ASF), Lesen von Multichannel-Audiodaten
- ASF (Advanced Systems Format), Lesen von Multichannel-Audiodaten
- Advanced Systems Format (ASF), Multichannel-Audiodatei
- ASF (Advanced Systems Format), Multichannel-Audiodatei
- Codecs, Lesen von Multichannel-Audiodaten
- Multichannel-Audiodaten, lesen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59da950eb4218ad87995ed80e22de4de302f8e42
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729456"
---
# <a name="reading-multichannel-audio"></a><span data-ttu-id="4ba2c-110">Lesen von Multichannel-Audiodateien</span><span class="sxs-lookup"><span data-stu-id="4ba2c-110">Reading Multichannel Audio</span></span>

<span data-ttu-id="4ba2c-111">Der Windows Media Audio 9 Professional-Codec kann Multichannel-Audiocodierung (mehr als zwei Kanäle) codieren.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-111">The Windows Media Audio 9 Professional codec can encode multichannel audio (more than two channels).</span></span> <span data-ttu-id="4ba2c-112">Wenn Sie eine Datei mit Multichannel-Audiodaten lesen, müssen Sie die Ausgabe ordnungsgemäß konfigurieren, oder die Audiodaten werden in einer niedrigeren Qualität und in Stereo bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-112">When reading a file with multichannel audio, you must configure the output properly or the audio will be delivered at a lower quality and in stereo.</span></span> <span data-ttu-id="4ba2c-113">Zum Festlegen einer Ausgabe für die Multichannel-audioübermittlung müssen Sie zwei Ausgabeeinstellungen festlegen: g \_ wszene ablediskreteoutput und g \_ wszspeakerconfig.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-113">To set an output for multichannel audio delivery, you must set two output settings: g\_wszEnableDiscreteOutput and g\_wszSpeakerConfig.</span></span>

<span data-ttu-id="4ba2c-114">Durch Festlegen \_ von g wszene ablediskreteoutput auf **true** wird der Codec so festgelegt, dass eine hochauflösende Audioausgabe bereitstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-114">Setting g\_wszEnableDiscreteOutput to **TRUE** sets the codec to deliver high-definition audio output.</span></span> <span data-ttu-id="4ba2c-115">High-Definition-Audiodaten werden vom Windows Media Audio 9-Codec mit 24-Bit-Beispielen in Stereo-oder mehreren Kanälen codiert.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-115">High-definition audio is encoded by the Windows Media Audio 9 codec with 24-bit samples in stereo or multiple channels.</span></span> <span data-ttu-id="4ba2c-116">Wenn diese Einstellung auf " **false**" festgelegt ist, wird nur eine 16-Bit-Stereoausgabe übermittelt.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-116">If this setting is **FALSE**, only 16-bit stereo output will be delivered.</span></span>

<span data-ttu-id="4ba2c-117">Die Anzahl der Redner auf dem Spielcomputer wird mit g \_ wszspeakerconfig festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-117">The number of speakers on the playing computer is set with g\_wszSpeakerConfig.</span></span> <span data-ttu-id="4ba2c-118">Diese Einstellung ist ein **DWORD** -Wert, der auf eine der in der folgenden Tabelle aufgeführten DirectSound-Sprecher Konstanten festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-118">This setting is a **DWORD** value set to one of the DirectSound speaker constants listed in the following table.</span></span> <span data-ttu-id="4ba2c-119">Um diese Konstanten Namen für den Compiler aufzulösen, müssen Sie DSound. h einschließen.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-119">To resolve these constant names for your compiler, you must include dsound.h.</span></span>



| <span data-ttu-id="4ba2c-120">Konstante</span><span class="sxs-lookup"><span data-stu-id="4ba2c-120">Constant</span></span>             | <span data-ttu-id="4ba2c-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4ba2c-121">Value</span></span>      | <span data-ttu-id="4ba2c-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ba2c-122">Description</span></span>                                                                  |
|----------------------|------------|------------------------------------------------------------------------------|
| <span data-ttu-id="4ba2c-123">dsspeaker- \_ directout</span><span class="sxs-lookup"><span data-stu-id="4ba2c-123">DSSPEAKER\_DIRECTOUT</span></span> | <span data-ttu-id="4ba2c-124">0x00000000</span><span class="sxs-lookup"><span data-stu-id="4ba2c-124">0x00000000</span></span> | <span data-ttu-id="4ba2c-125">Die Audiodaten werden direkt durchlaufen, ohne für Referenten konfiguriert zu werden.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-125">The audio is passed through directly, without being configured for speakers.</span></span> |
| <span data-ttu-id="4ba2c-126">dsspeaker- \_ Telefon</span><span class="sxs-lookup"><span data-stu-id="4ba2c-126">DSSPEAKER\_HEADPHONE</span></span> | <span data-ttu-id="4ba2c-127">0x00000001</span><span class="sxs-lookup"><span data-stu-id="4ba2c-127">0x00000001</span></span> | <span data-ttu-id="4ba2c-128">Der Client Computer ist mit einem Kopfhörer ausgestattet.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-128">The client computer is equipped with headphones.</span></span>                             |
| <span data-ttu-id="4ba2c-129">dsspeaker \_ Mono</span><span class="sxs-lookup"><span data-stu-id="4ba2c-129">DSSPEAKER\_MONO</span></span>      | <span data-ttu-id="4ba2c-130">0x00000002</span><span class="sxs-lookup"><span data-stu-id="4ba2c-130">0x00000002</span></span> | <span data-ttu-id="4ba2c-131">Der Client Computer ist mit einem monalen Redner ausgestattet.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-131">The client computer is equipped with a monaural speaker.</span></span>                     |
| <span data-ttu-id="4ba2c-132">dsspeaker \_ Quad</span><span class="sxs-lookup"><span data-stu-id="4ba2c-132">DSSPEAKER\_QUAD</span></span>      | <span data-ttu-id="4ba2c-133">0x00000003</span><span class="sxs-lookup"><span data-stu-id="4ba2c-133">0x00000003</span></span> | <span data-ttu-id="4ba2c-134">Der Client Computer ist mit quadratischen sprechenden Referenten ausgestattet.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-134">The client computer is equipped with quadraphonic speakers.</span></span>                  |
| <span data-ttu-id="4ba2c-135">dsspeaker- \_ Stereo</span><span class="sxs-lookup"><span data-stu-id="4ba2c-135">DSSPEAKER\_STEREO</span></span>    | <span data-ttu-id="4ba2c-136">0x00000004</span><span class="sxs-lookup"><span data-stu-id="4ba2c-136">0x00000004</span></span> | <span data-ttu-id="4ba2c-137">Der Client Computer ist mit Stereo Referenten ausgestattet.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-137">The client computer is equipped with stereo speakers.</span></span>                        |
| <span data-ttu-id="4ba2c-138">Umschließen von dsspeaker \_</span><span class="sxs-lookup"><span data-stu-id="4ba2c-138">DSSPEAKER\_SURROUND</span></span>  | <span data-ttu-id="4ba2c-139">0x00000005</span><span class="sxs-lookup"><span data-stu-id="4ba2c-139">0x00000005</span></span> | <span data-ttu-id="4ba2c-140">Der Client Computer ist mit vier-Kanal-umschließenden sprechenden ausgestattet.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-140">The client computer is equipped with four-channel surround-sound speakers.</span></span>   |
| <span data-ttu-id="4ba2c-141">Dsspeaker \_ 5point1</span><span class="sxs-lookup"><span data-stu-id="4ba2c-141">DSSPEAKER\_5POINT1</span></span>   | <span data-ttu-id="4ba2c-142">0x00000006</span><span class="sxs-lookup"><span data-stu-id="4ba2c-142">0x00000006</span></span> | <span data-ttu-id="4ba2c-143">Der Client Computer ist mit fünf Referenten und einem Subwoofer ausgestattet.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-143">The client computer is equipped with five speakers and a subwoofer.</span></span>          |
| <span data-ttu-id="4ba2c-144">Dsspeaker \_ 7point1</span><span class="sxs-lookup"><span data-stu-id="4ba2c-144">DSSPEAKER\_7POINT1</span></span>   | <span data-ttu-id="4ba2c-145">0x00000007</span><span class="sxs-lookup"><span data-stu-id="4ba2c-145">0x00000007</span></span> | <span data-ttu-id="4ba2c-146">Der Client Computer ist mit sieben Referenten und einem Subwoofer ausgestattet.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-146">The client computer is equipped with seven speakers and a subwoofer.</span></span>         |



 

<span data-ttu-id="4ba2c-147">Verwenden Sie [**IWMReaderAdvanced2:: setoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting), um diese Einstellungen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-147">To set these settings, use [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span></span>

<span data-ttu-id="4ba2c-148">Schließlich müssen Sie den richtigen Medientyp für die Ausgabe festlegen, damit die Kanäle diskret ausgegeben werden, und Sie müssen den richtigen Medientyp für die Ausgabe festlegen, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="4ba2c-148">Finally, for the channels to be output discretely, with no fold-down to stereo, you must set the correct media type on the output by following these steps:</span></span>

1.  <span data-ttu-id="4ba2c-149">Rufen Sie [**iwmreader:: getoutputformatcount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) auf, um die Anzahl der unterstützten Formate für die relevante Audioausgabe abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-149">Call [**IWMReader::GetOutputFormatCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformatcount) to get the number of supported formats for the relevant audio output.</span></span> <span data-ttu-id="4ba2c-150">Ausgabeformat Indizes sind NULL basiert.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-150">Output format indexes are zero-based.</span></span>
2.  <span data-ttu-id="4ba2c-151">Rufen Sie für jedes unterstützte Format [**iwmreader:: getoutputformat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) auf, um die [**iwmoutputmediaproperties**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) -Schnittstelle für das Eigenschaften Objekt der Ausgabemedien abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-151">For each supported format, call [**IWMReader::GetOutputFormat**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-getoutputformat) to retrieve the [**IWMOutputMediaProps**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmoutputmediaprops) interface on the output media properties object.</span></span>
3.  <span data-ttu-id="4ba2c-152">Rufen Sie [**iwmmedia-Eigenschaften:: getmediatype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) auf, um den Medientyp abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-152">Call [**IWMMediaProps::GetMediaType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype) to retrieve the media type.</span></span>
4.  <span data-ttu-id="4ba2c-153">Wenn der Typ des abgerufenen Mediums der gewünschte Multichannel-Typ ist, legen Sie ihn durch Aufrufen von [**iwmreader:: SetOutput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops)Eigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-153">If the retrieved media type is the desired multichannel type, then set it by calling [**IWMReader::SetOutputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-setoutputprops).</span></span>

<span data-ttu-id="4ba2c-154">Nachdem Sie die diskrete Ausgabe und die Sprecher Konfiguration festgelegt haben, sollten die vom Reader aufgelisteten Ausgabeformate Multichannel-Formate enthalten, die die [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) -Struktur verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-154">After you have set discrete output and the speaker configuration, the output formats enumerated by the reader should include multichannel formats that use the [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd757721(v=vs.85)) structure.</span></span> <span data-ttu-id="4ba2c-155">Wenn Sie die Ausgabeformate vor dem Festlegen der Eigenschaften aufzählen, werden nur Formate mit einem oder zwei Kanälen und maximal 16 Bits pro Kanal eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-155">If you enumerate the output formats before setting the properties, only formats with 1 or 2 channels and a maximum of 16 bits per channel will be included.</span></span> <span data-ttu-id="4ba2c-156">Wie bei anderen Audioformaten sollten Sie nur die Formate verwenden, die vom Reader aufgelistet werden. Konfigurieren Sie keine eigenen.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-156">As with other audio formats, you should use only the formats enumerated by the reader; do not configure your own.</span></span>

> [!Note]  
> <span data-ttu-id="4ba2c-157">Sie können Multichannel-Audiodaten nur ausgeben, wenn Ihre Anwendung unter Microsoft Windows XP oder einer neueren Version von Microsoft Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ba2c-157">You can output multichannel audio only if your application is running on Microsoft Windows XP or a later version of Microsoft Windows.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="4ba2c-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4ba2c-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4ba2c-159">**Eingaben, Streams und Ausgaben**</span><span class="sxs-lookup"><span data-stu-id="4ba2c-159">**Inputs, Streams and Outputs**</span></span>](inputs-streams-and-outputs.md)
</dt> <dt>

[<span data-ttu-id="4ba2c-160">**Lesen von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="4ba2c-160">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="4ba2c-161">**Ausgabeeinstellungen**</span><span class="sxs-lookup"><span data-stu-id="4ba2c-161">**Output Settings**</span></span>](output-settings.md)
</dt> <dt>

[<span data-ttu-id="4ba2c-162">**Arbeiten mit High-Resolution PCM-Audiodatei**</span><span class="sxs-lookup"><span data-stu-id="4ba2c-162">**Working with High-Resolution PCM Audio**</span></span>](working-with-high-resolution-pcm-audio.md)
</dt> </dl>

 

 