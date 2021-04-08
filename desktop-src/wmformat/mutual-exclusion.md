---
title: Gegenseitiger Ausschluss
description: Gegenseitiger Ausschluss
ms.assetid: 3a3f6763-a241-4bbd-a6e8-62041b05622d
keywords:
- Windows Media-Format-SDK, gegenseitiger Ausschluss
- Advanced Systems Format (ASF), gegenseitiger Ausschluss
- ASF (Advanced Systems Format), gegenseitiger Ausschluss
- Windows Media-Format-SDK, gegenseitiger MBR-Ausschluss
- Advanced Systems Format (ASF), gegenseitiger MBR-Ausschluss
- ASF (Advanced Systems-Format), gegenseitiger MBR-Ausschluss
- Windows Media-Format-SDK, mehrfache Bitrate (MBR)
- Advanced Systems Format (ASF), mehrfache Bitrate (MBR)
- ASF (Advanced Systems Format), Multiple Bitrate (MBR)
- gegenseitiger Ausschluss, Informationen
- mehrfache Bitrate (MBR), gegenseitiger Ausschluss
- MBR (mehrfache Bitrate), gegenseitiger Ausschluss
- gegenseitiger Ausschluss, Bitrate
- gegenseitiger Ausschluss, Sprache
- gegenseitiger Ausschluss, Präsentation
- gegenseitiger Ausschluss, unbekannt
- gegenseitiger Ausschluss, Features
- gegenseitiger Ausschluss, erweiterte Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd00bf5bcb544d2541a6bc5465171fe9bacc1b9c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856888"
---
# <a name="mutual-exclusion"></a><span data-ttu-id="efaac-121">Gegenseitiger Ausschluss</span><span class="sxs-lookup"><span data-stu-id="efaac-121">Mutual Exclusion</span></span>

<span data-ttu-id="efaac-122">Jede ASF-Datei enthält einen oder mehrere Streams, die jeweils digitale Mediendaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="efaac-122">Every ASF file contains one or more streams, each containing digital media data.</span></span> <span data-ttu-id="efaac-123">Unter normalen Umständen ist jeder Stream einer einzelnen Ausgabe zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="efaac-123">Under normal circumstances, each stream is associated with a single output.</span></span> <span data-ttu-id="efaac-124">Bei der Wiedergabe stellt das Reader-Objekt für jede Ausgabe Beispiele bereit.</span><span class="sxs-lookup"><span data-stu-id="efaac-124">On playback, the reader object delivers samples for each output.</span></span> <span data-ttu-id="efaac-125">Standardmäßig wird jeder Stream in einer ASF-Datei vom Reader bei der Wiedergabe zugestellt.</span><span class="sxs-lookup"><span data-stu-id="efaac-125">So, as a default, every stream in an ASF file is delivered by the reader on playback.</span></span>

<span data-ttu-id="efaac-126">Es gibt Situationen, in denen Sie nicht möchten, dass jeder Stream an den Client übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="efaac-126">There are situations where you do not want every stream delivered to the client.</span></span> <span data-ttu-id="efaac-127">Wenn Sie z. b. eine Videodatei mit fünf Audiostreams erstellen, eine für jede von fünf Sprachen, soll jeweils nur eine bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="efaac-127">For example, if you create a video file with five audio streams, one for each of five languages, you want only one of them to be delivered at a time.</span></span> <span data-ttu-id="efaac-128">Der gegenseitige Ausschluss ist eine Funktion des Windows Media SDK-SDKs, mit der Sie eine Reihe von sich gegenseitig ausschließenden Streams angeben können, die alle derselben Ausgabe entsprechen.</span><span class="sxs-lookup"><span data-stu-id="efaac-128">Mutual exclusion is a feature of the Windows Media Format SDK that enables you to specify a number of mutually exclusive streams that all equate to the same output.</span></span>

<span data-ttu-id="efaac-129">Der gegenseitige Ausschluss wird im Profil definiert, das zum Erstellen einer Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="efaac-129">Mutual exclusion is defined in the profile used to create a file.</span></span> <span data-ttu-id="efaac-130">Sie konfigurieren den gegenseitigen Ausschluss in einem Profil mithilfe von gegenseitigen Ausschluss Objekten.</span><span class="sxs-lookup"><span data-stu-id="efaac-130">You configure mutual exclusion in a profile by using mutual exclusion objects.</span></span> <span data-ttu-id="efaac-131">Sie fügen Streams nacheinander zum gegenseitigen Ausschluss Objekt hinzu, legen den Typ fest und fügen das Objekt in das Profil ein.</span><span class="sxs-lookup"><span data-stu-id="efaac-131">You add streams one at a time to the mutual exclusion object, set the type, and include the object in the profile.</span></span>

<span data-ttu-id="efaac-132">Das SDK für den Windows Media-Format erkennt vier Typen von gegenseitigem Ausschluss:</span><span class="sxs-lookup"><span data-stu-id="efaac-132">The Windows Media Format SDK recognizes four types of mutual exclusion:</span></span>

-   <span data-ttu-id="efaac-133">Bitrate</span><span class="sxs-lookup"><span data-stu-id="efaac-133">Bit rate</span></span>
-   <span data-ttu-id="efaac-134">Sprache</span><span class="sxs-lookup"><span data-stu-id="efaac-134">Language</span></span>
-   <span data-ttu-id="efaac-135">Präsentation</span><span class="sxs-lookup"><span data-stu-id="efaac-135">Presentation</span></span>
-   <span data-ttu-id="efaac-136">Unbekannt</span><span class="sxs-lookup"><span data-stu-id="efaac-136">Unknown</span></span>

## <a name="mutual-exclusion-by-bit-rate"></a><span data-ttu-id="efaac-137">Gegenseitiger Ausschluss durch Bitrate</span><span class="sxs-lookup"><span data-stu-id="efaac-137">Mutual Exclusion by Bit Rate</span></span>

<span data-ttu-id="efaac-138">Der gegenseitige Ausschluss der Bitrate ist eine besondere Art von gegenseitigem Ausschluss und wird häufiger als MBR-gegenseitiger Ausschluss (Multiple Bitrate) bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="efaac-138">Bit rate mutual exclusion is a special type of mutual exclusion and is more commonly referred to as multiple bit rate (MBR) mutual exclusion.</span></span> <span data-ttu-id="efaac-139">Ein MBR-gegenseitiger Ausschluss enthält eine Reihe von Streams, die alle aus derselben Eingabe stammen, aber mit unterschiedlichen Bitraten codiert sind.</span><span class="sxs-lookup"><span data-stu-id="efaac-139">An MBR mutual exclusion contains a number of streams that all originate from the same input, but are encoded at different bit rates.</span></span> <span data-ttu-id="efaac-140">Wenn eine Datei mit MBR abgespielt wird, bestimmt der Reader basierend auf der verfügbaren Bandbreite den besten Stream, der verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="efaac-140">When playing a file with MBR, the reader determines the best stream to use based on the available bandwidth.</span></span>

<span data-ttu-id="efaac-141">Das Windows Media-Format-SDK unterstützt MBR für Audiodaten und Videodaten Ströme.</span><span class="sxs-lookup"><span data-stu-id="efaac-141">The Windows Media Format SDK supports MBR for audio and video streams.</span></span> <span data-ttu-id="efaac-142">Das SDK unterstützt auch eine besondere Art von MBR-Video mit dem Namen "Multiple Video size MBR".</span><span class="sxs-lookup"><span data-stu-id="efaac-142">The SDK also supports a special type of MBR video called multiple video size MBR.</span></span> <span data-ttu-id="efaac-143">Dies ähnelt dem normalen MBR-Video, mit dem Unterschied, dass die einzelnen Streams verschiedene Frame Größen aufweisen können.</span><span class="sxs-lookup"><span data-stu-id="efaac-143">This is like normal MBR video except that the individual streams can have different frame sizes.</span></span> <span data-ttu-id="efaac-144">Beispielsweise verfügen Sie möglicherweise über einige Streams mit der Standardgröße von 320 x 240 und einige andere mit höheren Bitraten und 640 x 480 Video Größen.</span><span class="sxs-lookup"><span data-stu-id="efaac-144">For example, you might have some streams at the default 320 x 240 video size and some others with higher bit rates and 640 x 480 video size.</span></span>

## <a name="mutual-exclusion-by-language"></a><span data-ttu-id="efaac-145">Gegenseitiger Ausschluss nach Sprache</span><span class="sxs-lookup"><span data-stu-id="efaac-145">Mutual Exclusion by Language</span></span>

<span data-ttu-id="efaac-146">Der sprachbasierte gegenseitige Ausschluss ist für die Verwendung mit Inhalten (normalerweise Audiodaten) konzipiert, die in mehreren Sprachen aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="efaac-146">Language-based mutual exclusion is designed for use with content (usually audio) recorded in several languages.</span></span> <span data-ttu-id="efaac-147">Ein sprach basierter gegenseitiger Ausschluss umfasst mehrere Streams, die aus eindeutigen Eingaben stammen.</span><span class="sxs-lookup"><span data-stu-id="efaac-147">A language-based mutual exclusion includes several streams that originate from unique inputs.</span></span> <span data-ttu-id="efaac-148">Jede Eingabe ist derselbe Inhalt, jedoch in einer anderen Sprache.</span><span class="sxs-lookup"><span data-stu-id="efaac-148">Each input is the same content, but in a different language.</span></span>

<span data-ttu-id="efaac-149">Damit der gegenseitige Ausschluss nach Sprache funktioniert, muss die Leseanwendung Logik enthalten, um die entsprechende Sprache auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="efaac-149">For mutual exclusion by language to work, the reading application must include logic to select the appropriate language.</span></span> <span data-ttu-id="efaac-150">Wenn Sie eine Anwendung für die Wiedergabe von ASF-Dateien schreiben und Dateien mit sprach basiertem gegenseitigem Ausschluss unterstützen möchten, sollten Sie den entsprechenden Stream vor Beginn der Wiedergabe auswählen.</span><span class="sxs-lookup"><span data-stu-id="efaac-150">If you write an application to play ASF files, and you want to support files with language-based mutual exclusion, you should select the appropriate stream before beginning playback.</span></span>

## <a name="mutual-exclusion-by-presentation"></a><span data-ttu-id="efaac-151">Gegenseitiger Ausschluss durch Präsentation</span><span class="sxs-lookup"><span data-stu-id="efaac-151">Mutual Exclusion by Presentation</span></span>

<span data-ttu-id="efaac-152">Präsentations basierter gegenseitiger Ausschluss wird bereitgestellt, um Videostreams zu unterstützen, die denselben Inhalt enthalten, der mit unterschiedlichen Seitenverhältnissen codiert ist</span><span class="sxs-lookup"><span data-stu-id="efaac-152">Presentation-based mutual exclusion is provided to support video streams that contain the same content encoded with different aspect ratios.</span></span> <span data-ttu-id="efaac-153">Dies wird in der Regel verwendet, wenn Videos in einer Briefkasten Version (Seitenverhältnis 16:9) bereitgestellt werden und für Fernsehbildschirme (Seitenverhältnis 4:3) formatiert wird.</span><span class="sxs-lookup"><span data-stu-id="efaac-153">Typically, this is used when providing video in a letterbox version (aspect ratio 16:9) as well as formatted for television screens (aspect ratio 4:3).</span></span>

<span data-ttu-id="efaac-154">Die Auswahl einer Präsentation für die Wiedergabe wird am häufigsten vom Benutzer festgelegt.</span><span class="sxs-lookup"><span data-stu-id="efaac-154">The selection of a presentation for playback is most often determined by the user.</span></span> <span data-ttu-id="efaac-155">Wenn Sie eine Anwendung für die Wiedergabe von ASF-Dateien schreiben und Dateien mit dem Präsentations basierten gegenseitigen Ausschluss unterstützen möchten, sollten Sie dem Benutzer die Möglichkeit geben, einen Präsentationstypen für die Anzeige auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="efaac-155">If you write an application to play ASF files and want to support files with presentation based mutual exclusion, you should present the user with the option of selecting a presentation type for viewing.</span></span>

## <a name="unknown-mutual-exclusion"></a><span data-ttu-id="efaac-156">Unbekannter gegenseitiger Ausschluss</span><span class="sxs-lookup"><span data-stu-id="efaac-156">Unknown Mutual Exclusion</span></span>

<span data-ttu-id="efaac-157">Sie können den gegenseitigen Ausschluss basierend auf beliebigen Kriterien erstellen.</span><span class="sxs-lookup"><span data-stu-id="efaac-157">You can create mutual exclusion based on any criteria you like.</span></span> <span data-ttu-id="efaac-158">Alle benutzerdefinierten Typen für den gegenseitigen Ausschluss sollten mit dem unbekannten Typ erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="efaac-158">All custom mutual exclusion types should be created using the unknown type.</span></span>

## <a name="advanced-mutual-exclusion-features"></a><span data-ttu-id="efaac-159">Erweiterte Funktionen für den gegenseitigen Ausschluss</span><span class="sxs-lookup"><span data-stu-id="efaac-159">Advanced Mutual Exclusion Features</span></span>

<span data-ttu-id="efaac-160">Sie können auch den gegenseitigen Ausschluss verwenden, um Datenströme anderen Gruppen zuzuweisen, die sich gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="efaac-160">You can also use mutual exclusion to assign streams to groups that are mutually exclusive of one another.</span></span> <span data-ttu-id="efaac-161">Beispielsweise können Sie Audiodatenströme in mehreren Sprachen haben und jedem einen anderen Videostream zuweisen.</span><span class="sxs-lookup"><span data-stu-id="efaac-161">For example, you might want to have audio streams in multiple languages and assign a different video stream to each.</span></span> <span data-ttu-id="efaac-162">Sie verwenden den gegenseitigen Ausschluss, um jeden Audiostream mit dem entsprechenden Videostream zu gruppieren und alle Gruppen gegenseitig zu schließen.</span><span class="sxs-lookup"><span data-stu-id="efaac-162">You use mutual exclusion to group each audio stream with its corresponding video stream and make all groups mutually exclusive.</span></span>

<span data-ttu-id="efaac-163">Der Reader wählt automatisch Streams für alle gegenseitigen Ausschlüsse aus.</span><span class="sxs-lookup"><span data-stu-id="efaac-163">The reader automatically selects streams for all mutual exclusions.</span></span> <span data-ttu-id="efaac-164">Für alle Typen von gegenseitigem Ausschluss mit Ausnahme von MBR und einem sprachbasierten gegenseitigen Ausschluss wählt der Reader stets den Standardstream aus. Dies ist der erste Datenstrom, der dem gegenseitigen Ausschluss Objekt im Profil hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="efaac-164">For all types of mutual exclusion except MBR and language-based mutual exclusion, the reader always selects the default stream, which is the first stream added to the mutual exclusion object in the profile.</span></span> <span data-ttu-id="efaac-165">Für MBR wählt der Reader den Stream aus, der zum Zeitpunkt der Wiedergabe am besten der verfügbaren Bandbreite entspricht.</span><span class="sxs-lookup"><span data-stu-id="efaac-165">For MBR, the reader selects the stream that best suits the available bandwidth at the time of playback.</span></span> <span data-ttu-id="efaac-166">Wenn Sie den Standardstream nicht verwenden möchten, können Sie die Streamauswahl auf "manuell" festlegen, bevor Sie mit dem Lesen einer Datei beginnen.</span><span class="sxs-lookup"><span data-stu-id="efaac-166">If you do not want to use the default stream, you can set stream selection to manual before starting to read a file.</span></span>

<span data-ttu-id="efaac-167">Die manuelle Datenstrom Auswahl gilt für die gesamte Datei.</span><span class="sxs-lookup"><span data-stu-id="efaac-167">Manual stream selection applies to the entire file.</span></span> <span data-ttu-id="efaac-168">Es können Schwierigkeiten auftreten, wenn Sie gegenseitige Ausschlüsse verschiedener Typen in derselben Datei haben.</span><span class="sxs-lookup"><span data-stu-id="efaac-168">Difficulties can arise when you have mutual exclusions of different types in the same file.</span></span> <span data-ttu-id="efaac-169">Beispielsweise kann eine Datei sowohl Bitrate-basierten gegenseitigen Ausschluss als auch benutzerdefinierter gegenseitiger Ausschluss enthalten.</span><span class="sxs-lookup"><span data-stu-id="efaac-169">For example, a file can contain both bit-rate-based mutual exclusion and custom mutual exclusion.</span></span> <span data-ttu-id="efaac-170">Wenn Sie einen anderen Datenstrom als den Standardwert im benutzerdefinierten gegenseitigen Ausschluss auswählen möchten, müssen Sie die manuelle Datenstrom Auswahl verwenden.</span><span class="sxs-lookup"><span data-stu-id="efaac-170">To select a stream other than the default in the custom mutual exclusion, you must use manual stream selection.</span></span> <span data-ttu-id="efaac-171">Wenn Sie jedoch die manuelle Datenstrom Auswahl verwenden, wählt der Reader den multibitrate-Stream nicht automatisch aus.</span><span class="sxs-lookup"><span data-stu-id="efaac-171">If you use manual stream selection, however, the reader will not automatically select the multiple bit rate stream.</span></span> <span data-ttu-id="efaac-172">Sie müssen diese Eventualität in der Anwendung planen, wenn Sie beabsichtigen, mehrere Typen von gegenseitigem Ausschluss in einer einzelnen Datei zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="efaac-172">You must plan for this eventuality in your application if you plan to support multiple types of mutual exclusion in a single file.</span></span> <span data-ttu-id="efaac-173">In der Regel bedeutet dies, dass Sie eigene streamauswahlroutinen für normalerweise automatische Typen von gegenseitigem Ausschluss erstellen.</span><span class="sxs-lookup"><span data-stu-id="efaac-173">Typically this means creating your own stream selection routines for normally automatic types of mutual exclusion.</span></span>

## <a name="related-topics"></a><span data-ttu-id="efaac-174">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="efaac-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="efaac-175">**Funktionen der ASF-Datei**</span><span class="sxs-lookup"><span data-stu-id="efaac-175">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="efaac-176">**Verwenden von gegenseitigem Ausschluss**</span><span class="sxs-lookup"><span data-stu-id="efaac-176">**Using Mutual Exclusion**</span></span>](using-mutual-exclusion.md)
</dt> </dl>

 

 




