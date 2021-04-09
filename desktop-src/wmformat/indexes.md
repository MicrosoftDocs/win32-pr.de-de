---
title: Indizes
description: Indizes
ms.assetid: 54c694f6-3c10-4d7c-bcd1-f2b17d652e8e
keywords:
- Windows Media-Format-SDK, Indizes
- Advanced Systems Format (ASF), Indizes
- ASF (Advanced Systems Format), Indizes
- Windows Media-Format-SDK, Temporale Indizes
- Advanced Systems Format (ASF), Temporale Indizes
- ASF (Advanced Systems Format), Temporale Indizes
- Windows Media-Format-SDK, Frame basierte Indizes
- Advanced Systems Format (ASF), Frame basierte Indizes
- ASF (Advanced Systems Format), Frame basierte Indizes
- Windows Media-Format-SDK, SMPTE-Zeit Codes
- Advanced Systems Format (ASF), SMPTE-Zeit Codes
- ASF (Advanced Systems Format), SMPTE-Zeit Codes
- Indizes, Informationen
- Temporale Indizes
- Frame basierte Indizes
- SMPTE-Zeit Codes, Indizes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d2e5a194f9c495720cbc40ccdb192509723eee0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856696"
---
# <a name="indexes"></a><span data-ttu-id="21e1b-119">Indizes</span><span class="sxs-lookup"><span data-stu-id="21e1b-119">Indexes</span></span>

<span data-ttu-id="21e1b-120">Eine häufige Anforderung für Anwendungen, die digitale Mediendateien lesen, ist die Möglichkeit, zu einem bestimmten Punkt im Inhalt zu suchen.</span><span class="sxs-lookup"><span data-stu-id="21e1b-120">A common requirement for applications that read digital media files is the ability to seek to a specific point in the content.</span></span> <span data-ttu-id="21e1b-121">Die Suche kann schwierig sein, da es keine Garantie dafür gibt, dass die verschiedenen Streams in einer Datei über Beispiele mit gleichzeitigen Startzeiten verfügen.</span><span class="sxs-lookup"><span data-stu-id="21e1b-121">Seeking can be difficult because there is no guarantee that the various streams in a file have samples with concurrent start times.</span></span> <span data-ttu-id="21e1b-122">Dieses Problem wird durch die Verwendung von *Indizes* gelöst.</span><span class="sxs-lookup"><span data-stu-id="21e1b-122">This problem is addressed with the use of *indexes*.</span></span> <span data-ttu-id="21e1b-123">Ein Index ist ein Objekt in einer ASF-Datei, das Videobeispiele mit ihren Präsentations Zeiten gleichsetzt.</span><span class="sxs-lookup"><span data-stu-id="21e1b-123">An index is an object in an ASF file that equates video samples with their presentation times.</span></span> <span data-ttu-id="21e1b-124">Für Audiostreams ist kein Index erforderlich, da Audiodaten enger mit der Präsentationszeit verbunden sind, als Videodaten.</span><span class="sxs-lookup"><span data-stu-id="21e1b-124">No index is required for audio streams because audio data is more closely connected with presentation time than video data is.</span></span>

<span data-ttu-id="21e1b-125">Das Indexer-Objekt des Windows Media Format SDK kann drei verschiedene Typen von Indizes erstellen: Temporale Indizes, Frame basierte Indizes und SMPTE-Zeit Code Indizes.</span><span class="sxs-lookup"><span data-stu-id="21e1b-125">The indexer object of the Windows Media Format SDK can create three different types of indexes: temporal indexes, frame-based indexes, and SMPTE time code indexes.</span></span>

<span data-ttu-id="21e1b-126">Temporale Indizes sind der häufigste Typ.</span><span class="sxs-lookup"><span data-stu-id="21e1b-126">Temporal indexes are the most common type.</span></span> <span data-ttu-id="21e1b-127">Sie entsprechen einfach Videobeispielen mit den entsprechenden Präsentations Zeiten.</span><span class="sxs-lookup"><span data-stu-id="21e1b-127">They simply equate video samples with the corresponding presentation times.</span></span>

<span data-ttu-id="21e1b-128">Ein Frame basierter Index entspricht Videobeispielen mit Video Frame Nummern und Präsentations Zeiten.</span><span class="sxs-lookup"><span data-stu-id="21e1b-128">A frame-based index equates video samples with video frame numbers and presentation times.</span></span> <span data-ttu-id="21e1b-129">Frame Nummern sind besonders nützlich für Anwendungen, die Video bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="21e1b-129">Frame numbers are particularly useful in applications that edit video.</span></span>

<span data-ttu-id="21e1b-130">Ein SMTPE-Zeit Code Index ist der seltenste Indextyp.</span><span class="sxs-lookup"><span data-stu-id="21e1b-130">A SMTPE time code index is the rarest type of index.</span></span> <span data-ttu-id="21e1b-131">Der SMPTE-Zeit Code wird als Grundlage für den Index verwendet und kann nur in Streams verwendet werden, für die in den Beispielen SMPTE-Zeitstempel enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="21e1b-131">It uses SMPTE time code as the basis of the index and can be used only on streams that have SMPTE time stamps included with their samples.</span></span> <span data-ttu-id="21e1b-132">Weitere Informationen zum SMPTE-Zeit Code finden Sie [unter Unterstützung von SMPTE-Zeit Code](smpte-time-code-support.md).</span><span class="sxs-lookup"><span data-stu-id="21e1b-132">For more information about SMPTE time code, see [SMPTE Time Code Support](smpte-time-code-support.md).</span></span>

<span data-ttu-id="21e1b-133">Eine ASF-Datei kann einen Index jedes Typs für jeden enthaltenen Videostream enthalten.</span><span class="sxs-lookup"><span data-stu-id="21e1b-133">An ASF file can contain an index of each type for each video stream it contains.</span></span> <span data-ttu-id="21e1b-134">Standardmäßig wird ein Temporaler Index für jeden Videostream in Dateien eingeschlossen, die vom Writer-Objekt erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="21e1b-134">As a default, a temporal index is included for each video stream in files created by the writer object.</span></span> <span data-ttu-id="21e1b-135">Sie können die Einstellungen für die automatische Indizierung für Ihre Dateien entsprechend Ihren Anforderungen ändern.</span><span class="sxs-lookup"><span data-stu-id="21e1b-135">You can change the automatic indexing settings for your files to suit your needs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="21e1b-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="21e1b-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="21e1b-137">**Funktionen der ASF-Datei**</span><span class="sxs-lookup"><span data-stu-id="21e1b-137">**ASF File Features**</span></span>](asf-file-features.md)
</dt> <dt>

[<span data-ttu-id="21e1b-138">**Arbeiten mit Indizes**</span><span class="sxs-lookup"><span data-stu-id="21e1b-138">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> <dt>

[<span data-ttu-id="21e1b-139">**Lesen von Dateien mit dem asynchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="21e1b-139">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="21e1b-140">**Lesen von Dateien mit dem synchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="21e1b-140">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




