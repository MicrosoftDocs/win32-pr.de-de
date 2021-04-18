---
title: Unterstützung von Wasserzeichen
description: Unterstützung von Wasserzeichen
ms.assetid: 1fafb15e-57b8-4dd0-8f0c-ccf460f05157
keywords:
- Windows Media-Format-SDK, Unterstützung von Wasserzeichen
- Windows Media-Format-SDK, digitales Wasserzeichen
- Advanced Systems Format (ASF), Unterstützung von Wasserzeichen
- ASF (Advanced Systems Format), Unterstützung von Wasserzeichen
- Advanced Systems Format (ASF), digitales Wasserzeichen
- ASF (Advanced Systems Format), digitales Wasserzeichen
- Windows Media-Format-SDK, DMO
- Advanced Systems Format (ASF), DMO
- ASF (Advanced Systems Format), DMO
- Windows Media-Format-SDK, iwmwatermarkinfo-Schnittstelle
- Advanced Systems Format (ASF), iwmwatermarkinfo-Schnittstelle
- ASF (Advanced Systems Format), iwmwatermarkinfo-Schnittstelle
- Wasserzeichen, Info
- digitales Wasserzeichen
- DirectX-Medienobjekt (DMO), Informationen zu
- DMO (DirectX-Medienobjekt), Informationen zu
- Iwmwatermarkinfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 417012cb165c0028e71af6f8b50052fdd2fab208
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341705"
---
# <a name="watermarking-support"></a><span data-ttu-id="71a8a-120">Unterstützung von Wasserzeichen</span><span class="sxs-lookup"><span data-stu-id="71a8a-120">Watermarking Support</span></span>

<span data-ttu-id="71a8a-121">Das digitale Wasserzeichen ist eine Möglichkeit, Copyright-oder sonstige Informationen in die Daten eines Medien Stroms einzubetten.</span><span class="sxs-lookup"><span data-stu-id="71a8a-121">Digital watermarking is a way to embed copyright or other information in the data of a media stream.</span></span> <span data-ttu-id="71a8a-122">Die Verfahren für die wassermarkierung variieren stark von einer Lösung zum nächsten.</span><span class="sxs-lookup"><span data-stu-id="71a8a-122">Techniques for watermarking vary widely from one solution to the next.</span></span> <span data-ttu-id="71a8a-123">Die einfachste Art von Wasserzeichen ist das einfache Hinzufügen eines identifizierenden Bilds zu jedem Frame eines Videodaten Stroms.</span><span class="sxs-lookup"><span data-stu-id="71a8a-123">The simplest form of watermarking is simply adding an identifying image to each frame of a video stream.</span></span> <span data-ttu-id="71a8a-124">Diese Technik wird häufig von Fernsehstationen verwendet, um ein semitransparentes Logo in der unteren Ecke der Übertragung einzufügen.</span><span class="sxs-lookup"><span data-stu-id="71a8a-124">Television stations frequently use this technique to insert a semi-transparent logo in a bottom corner of their broadcast.</span></span> <span data-ttu-id="71a8a-125">Anspruchsvollere Formen digitaler Wasserzeichen sind nicht wahrnehmbar für den Benutzer, der den Inhalt überwacht oder überwacht.</span><span class="sxs-lookup"><span data-stu-id="71a8a-125">More sophisticated forms of digital watermarking are imperceptible to the user watching or listening to the content.</span></span>

<span data-ttu-id="71a8a-126">Das Windows Media-Format-SDK unterstützt die Verwendung digitaler Wasserzeichen- [*DMOS*](wmformat-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="71a8a-126">The Windows Media Format SDK supports the use of digital watermarking [*DMOs*](wmformat-glossary.md).</span></span> <span data-ttu-id="71a8a-127">In der Praxis ist ein Wasserzeichen System sehr ähnlich wie ein Codec: es nimmt Medien Beispiele an, führt Algorithmen für die Daten aus und gibt die geänderten Beispiele aus.</span><span class="sxs-lookup"><span data-stu-id="71a8a-127">In practice, a watermarking system is very similar to a codec: it takes media samples, runs algorithms on the data, and outputs the altered samples.</span></span> <span data-ttu-id="71a8a-128">Wenn ein Wasserzeichen System für einen Stream angegeben wird, schließt das Writer-Objekt den DMO in seine Verarbeitung von Eingabe Beispielen ein.</span><span class="sxs-lookup"><span data-stu-id="71a8a-128">When a watermarking system is specified for a stream, the writer object includes the DMO in its processing of input samples.</span></span>

<span data-ttu-id="71a8a-129">Sie müssen Informationen zur Wasserzeichen Konfiguration angeben, wenn Sie einen Datenstrom für das Wasserzeichen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="71a8a-129">You must specify watermark configuration information when you configure a stream for watermarking.</span></span> <span data-ttu-id="71a8a-130">Die Konfigurationswerte unterscheiden sich je nach dem Wasserzeichen DMO.</span><span class="sxs-lookup"><span data-stu-id="71a8a-130">The configuration values will be different depending upon the watermarking DMO.</span></span> <span data-ttu-id="71a8a-131">Der verwendete DMO sollte Anweisungen enthalten, in denen die von ihm unterstützten Konfigurationswerte beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="71a8a-131">The DMO you use should come with instructions describing the configuration values it supports.</span></span>

<span data-ttu-id="71a8a-132">Informationen zu den Einstellungen, die zum Angeben eines Wasserzeichen Systems verwendet werden, finden Sie unter [ **IWMWriterAdvanced2:: setinputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)</span><span class="sxs-lookup"><span data-stu-id="71a8a-132">For information about the settings used to specify a watermarking system, see [**IWMWriterAdvanced2::SetInputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced2-setinputsetting)</span></span>

<span data-ttu-id="71a8a-133">Sie können Ihre Anwendung so programmieren, dass Sie die auf dem Client Computer installierten Wasserzeichen DMOS aufzählt.</span><span class="sxs-lookup"><span data-stu-id="71a8a-133">You can program your application to enumerate the watermarking DMOs installed on the client computer.</span></span> <span data-ttu-id="71a8a-134">Weitere Informationen finden Sie unter der [**iwmwatermarkinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="71a8a-134">For more information, see the [**IWMWatermarkInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwatermarkinfo) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="71a8a-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="71a8a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71a8a-136">**Funktionen zum Schreiben von Dateien**</span><span class="sxs-lookup"><span data-stu-id="71a8a-136">**File Writing Features**</span></span>](file-writing-features.md)
</dt> </dl>

 

 




