---
title: Konformitäts Vorlagen für Audiogeräte
description: Konformitäts Vorlagen für Audiogeräte
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- Windows Media-Format-SDK, Geräte Konformitäts Vorlagen
- Advanced Systems Format (ASF), Geräte Konformitäts Vorlagen
- ASF (Advanced Systems Format), Geräte Konformitäts Vorlagen
- Windows Media-Format-SDK, Vorlagen für die Konformität von Audiogeräten
- Advanced Systems Format (ASF), Audiogeräte-Konformitäts Vorlagen
- ASF (Advanced Systems Format), Formatvorlagen für Audiogeräte
- Windows Media Audio 9-Codec, Vorlagen für Audiogeräte Konformität
- Codecs, Windows Media Audio 9-Codec
- Geräte Konformitäts Vorlagen, Video
- Konformitäts Vorlagen für Audiogeräte
- Vorlagen, Konformitäts Vorlagen für Audiogeräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e1065395e64fdd2d8e60585900307a4dd3f39b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309988"
---
# <a name="audio-device-conformance-templates"></a><span data-ttu-id="776b6-114">Konformitäts Vorlagen für Audiogeräte</span><span class="sxs-lookup"><span data-stu-id="776b6-114">Audio Device Conformance Templates</span></span>

<span data-ttu-id="776b6-115">In der folgenden Tabelle werden die Geräte Konformitäts Vorlagen und die zugehörigen Parameter für den Windows Media Audio 9-Codec oder höher aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="776b6-115">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 codec, or later.</span></span>



| <span data-ttu-id="776b6-116">Vorlagen Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="776b6-116">Template string</span></span> | <span data-ttu-id="776b6-117">Bereich für Bitrate</span><span class="sxs-lookup"><span data-stu-id="776b6-117">Bit rate range</span></span>     | <span data-ttu-id="776b6-118">Notizen</span><span class="sxs-lookup"><span data-stu-id="776b6-118">Notes</span></span>                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="776b6-119">L1</span><span class="sxs-lookup"><span data-stu-id="776b6-119">"L1"</span></span>            | <span data-ttu-id="776b6-120">64 160 KBit/s</span><span class="sxs-lookup"><span data-stu-id="776b6-120">64 Kbps   160 Kbps</span></span> | <span data-ttu-id="776b6-121">Diese Vorlage ist für eingeschränkte reine Audiogeräte gedacht.</span><span class="sxs-lookup"><span data-stu-id="776b6-121">This template is intended for constrained audio-only devices.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="776b6-122">L2</span><span class="sxs-lookup"><span data-stu-id="776b6-122">"L2"</span></span>            | <span data-ttu-id="776b6-123"><= 160 KBit/s</span><span class="sxs-lookup"><span data-stu-id="776b6-123"><= 160 Kbps</span></span>     | <span data-ttu-id="776b6-124">Diese Vorlage entspricht der Klasse 4 im Windows Media Audio portieren Kit, das die gesamte Windows Media Audio Decoder-Implementierung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="776b6-124">This template corresponds to Class 4 in the Windows Media Audio porting kit, which supports the entire Windows Media Audio decoder implementation.</span></span>                                                                                   |
| <span data-ttu-id="776b6-125">L3</span><span class="sxs-lookup"><span data-stu-id="776b6-125">"L3"</span></span>            | <span data-ttu-id="776b6-126"><= 384 Kbit/s</span><span class="sxs-lookup"><span data-stu-id="776b6-126"><= 384 Kbps</span></span>     | <span data-ttu-id="776b6-127">Diese Vorlage entspricht der Klasse 4 im Windows Media Audio portieren Kit, das die gesamte Windows Media Audio Decoder-Implementierung unterstützt. Der Bitrate Bereich ist der einzige Unterschied zwischen dieser Vorlage und L2.</span><span class="sxs-lookup"><span data-stu-id="776b6-127">This template corresponds to Class 4 in the Windows Media Audio porting kit, which supports the entire Windows Media Audio decoder implementation.The bit rate range is the only difference between this template and L2.</span></span><br/> |
| <span data-ttu-id="776b6-128">Int</span><span class="sxs-lookup"><span data-stu-id="776b6-128">"L"</span></span>             | <span data-ttu-id="776b6-129">Alle Bitraten</span><span class="sxs-lookup"><span data-stu-id="776b6-129">All bit rates</span></span>      | <span data-ttu-id="776b6-130">Diese Vorlage ist nur für die Verwendung mit persönlichen Computern vorgesehen und wird normalerweise verwendet, um die vollständigen Funktionen des Codecs vorzustellen.</span><span class="sxs-lookup"><span data-stu-id="776b6-130">This template is for use with personal computers only, and is usually used to showcase the full capabilities of the codec.</span></span>                                                                                                           |



 

<span data-ttu-id="776b6-131">In der folgenden Tabelle sind die Geräte Übereinstimmungs Vorlagen und die zugehörigen Parameter für den Windows Media Audio 9-Sprachcodec aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="776b6-131">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 Voice codec.</span></span>



| <span data-ttu-id="776b6-132">Vorlagen Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="776b6-132">Template string</span></span> | <span data-ttu-id="776b6-133">Bereich für Bitrate</span><span class="sxs-lookup"><span data-stu-id="776b6-133">Bit rate range</span></span> | <span data-ttu-id="776b6-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="776b6-134">Notes</span></span>                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="776b6-135">S1</span><span class="sxs-lookup"><span data-stu-id="776b6-135">"S1"</span></span>            | <span data-ttu-id="776b6-136"><= 20 kbit/s</span><span class="sxs-lookup"><span data-stu-id="776b6-136"><= 20 Kbps</span></span>  | <span data-ttu-id="776b6-137">Diese Vorlage ist nur für Geräte mit sehr geringer Komplexität vorgesehen. Diese Vorlage ist nur sprachbasiert.</span><span class="sxs-lookup"><span data-stu-id="776b6-137">This template is intended for very low-complexity devices only.This template is speech only.</span></span><br/>                    |
| <span data-ttu-id="776b6-138">S2</span><span class="sxs-lookup"><span data-stu-id="776b6-138">"S2"</span></span>            | <span data-ttu-id="776b6-139"><= 20 kbit/s</span><span class="sxs-lookup"><span data-stu-id="776b6-139"><= 20 Kbps</span></span>  | <span data-ttu-id="776b6-140">Dies ist die empfohlene Vorlage für die meisten Anwendungen. Diese Vorlage unterstützt Kombinationen von Sprache und Musik.</span><span class="sxs-lookup"><span data-stu-id="776b6-140">This is the recommended template for most applications.This template supports combinations of speech and music.</span></span><br/> |



 

<span data-ttu-id="776b6-141">In der folgenden Tabelle werden die Geräte Konformitäts Vorlagen und die zugehörigen Parameter für den Windows Media Audio 9 Professional-Codec oder höher aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="776b6-141">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 Professional codec, or later.</span></span>



| <span data-ttu-id="776b6-142">Vorlagen Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="776b6-142">Template string</span></span> | <span data-ttu-id="776b6-143">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="776b6-143">Properties</span></span>                                                                                   | <span data-ttu-id="776b6-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="776b6-144">Notes</span></span>                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="776b6-145">M1</span><span class="sxs-lookup"><span data-stu-id="776b6-145">"M1"</span></span>            | <span data-ttu-id="776b6-146">Bitrate <= 384 kbpssampling Rate <= 48 kHz</span><span class="sxs-lookup"><span data-stu-id="776b6-146">Bit rate <= 384 KbpsSampling rate <= 48 kHz</span></span><br/> <span data-ttu-id="776b6-147">Kanäle <= 5,1</span><span class="sxs-lookup"><span data-stu-id="776b6-147">Channels <= 5.1</span></span><br/>   | <span data-ttu-id="776b6-148">Diese Vorlage wird für Standardfilme mit umschließenden Sound empfohlen.</span><span class="sxs-lookup"><span data-stu-id="776b6-148">This template is recommended for standard movies with surround sound.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="776b6-149">Groß</span><span class="sxs-lookup"><span data-stu-id="776b6-149">"M2"</span></span>            | <span data-ttu-id="776b6-150">Bitrate <= 768 kbpssampling Rate <= 96 kHz</span><span class="sxs-lookup"><span data-stu-id="776b6-150">Bit rate <= 768 KbpsSampling rate <= 96 kHz</span></span><br/> <span data-ttu-id="776b6-151">Kanäle <= 5,1</span><span class="sxs-lookup"><span data-stu-id="776b6-151">Channels <= 5.1</span></span><br/>   | <span data-ttu-id="776b6-152">Diese Vorlage wird für hoch Definitions Filme mit umschließenden Sound empfohlen.</span><span class="sxs-lookup"><span data-stu-id="776b6-152">This template is recommended for high-definition movies with surround sound.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="776b6-153">Kubikmeter</span><span class="sxs-lookup"><span data-stu-id="776b6-153">"M3"</span></span>            | <span data-ttu-id="776b6-154">Bitrate <= 1.500 kbpssampling Rate <= 96 kHz</span><span class="sxs-lookup"><span data-stu-id="776b6-154">Bit rate <= 1,500 KbpsSampling rate <= 96 kHz</span></span><br/> <span data-ttu-id="776b6-155">Kanäle <= 7,1</span><span class="sxs-lookup"><span data-stu-id="776b6-155">Channels <= 7.1</span></span><br/> | <span data-ttu-id="776b6-156">Diese Vorlage wird für hoch Definitions Filme mit 8-Kanal-Umschließungs Sound empfohlen, wie z. b. Inhalte, die für die Präsentation in Theatern codiert sind.</span><span class="sxs-lookup"><span data-stu-id="776b6-156">This template is recommended for high-definition movies with 8-channel surround sound, such as content encoded for presentation in theaters.</span></span>                                                                                                    |
| <span data-ttu-id="776b6-157">"M"</span><span class="sxs-lookup"><span data-stu-id="776b6-157">"M"</span></span>             | <span data-ttu-id="776b6-158">Alle Bitraten alle Samplings an</span><span class="sxs-lookup"><span data-stu-id="776b6-158">All bit ratesAll sampling rates</span></span><br/> <span data-ttu-id="776b6-159">Alle Kanäle</span><span class="sxs-lookup"><span data-stu-id="776b6-159">All channels</span></span><br/>                           | <span data-ttu-id="776b6-160">Diese Vorlage ist nur für die Verwendung mit persönlichen Computern vorgesehen und wird normalerweise verwendet, um die vollständigen Funktionen des Codecs vorzustellen. Dies ist auch die Vorlagen Bezeichnung für alle Audiodaten, die mit dem Windows Media Audio 9 verlustfreien Codec codiert sind.</span><span class="sxs-lookup"><span data-stu-id="776b6-160">This template is for use with personal computers only, and is usually used to showcase the full capabilities of the codec.This is also the template designation for all audio encoded with the Windows Media Audio 9 Lossless codec.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="776b6-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="776b6-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="776b6-162">**Parameter für die Geräte Konformitäts Vorlage**</span><span class="sxs-lookup"><span data-stu-id="776b6-162">**Device Conformance Template Parameters**</span></span>](device-conformance-template-parameters.md)
</dt> <dt>

[<span data-ttu-id="776b6-163">**Empfohlene Kombinationen von Geräte Konformitäts Vorlagen**</span><span class="sxs-lookup"><span data-stu-id="776b6-163">**Recommended Device Conformance Template Combinations**</span></span>](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[<span data-ttu-id="776b6-164">**Vorlagen für die Konformitäts Konformität von Video Geräten**</span><span class="sxs-lookup"><span data-stu-id="776b6-164">**Video Device Conformance Templates**</span></span>](video-device-conformance-templates.md)
</dt> </dl>

 

 





