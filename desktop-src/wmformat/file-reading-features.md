---
title: Funktionen zum Lesen von Dateien
description: Funktionen zum Lesen von Dateien
ms.assetid: ba6dd328-2250-4867-94e0-f66c70ac1bac
keywords:
- Windows Media-Format-SDK, Datei Lesefunktionen
- Windows Media-Format-SDK, asynchrones Lesen von Dateien
- Windows Media-Format-SDK, synchrone Datei Lesevorgänge
- Advanced Systems Format (ASF), Datei Lesefunktionen
- ASF (Advanced Systems Format), Datei Lesefunktionen
- Advanced Systems Format (ASF), asynchrones Lesen von Dateien
- ASF (Advanced Systems Format), asynchrones Lesen von Dateien
- Advanced Systems Format (ASF), synchrones Lesen von Dateien
- ASF (Advanced Systems Format), synchrones Lesen von Dateien
- asynchrones Lesen von Dateien
- synchrone Datei Lesevorgänge
- synchrone Reader, Datei Lesefunktionen
- Datei Lesevorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a83d3ce112d0d9e47626b4f7850f760da5c6583e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311268"
---
# <a name="file-reading-features"></a><span data-ttu-id="1240c-116">Funktionen zum Lesen von Dateien</span><span class="sxs-lookup"><span data-stu-id="1240c-116">File Reading Features</span></span>

<span data-ttu-id="1240c-117">Das Lesen von ASF-Dateien ist eines der wichtigsten Features des Windows Media-SDK.</span><span class="sxs-lookup"><span data-stu-id="1240c-117">Reading ASF files is one of the primary features of the Windows Media Format SDK.</span></span> <span data-ttu-id="1240c-118">Zwei Lese Typen werden unterstützt: asynchron und synchron.</span><span class="sxs-lookup"><span data-stu-id="1240c-118">Two types of reading are supported: asynchronous and synchronous.</span></span> <span data-ttu-id="1240c-119">Asynchrones Lesen von Dateien wird vom Reader-Objekt verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="1240c-119">Asynchronous file reading is handled by the reader object.</span></span> <span data-ttu-id="1240c-120">Das synchrone Reader-Objekt wird verwendet, um Dateien synchron zu lesen.</span><span class="sxs-lookup"><span data-stu-id="1240c-120">The synchronous reader object is used to read files synchronously.</span></span> <span data-ttu-id="1240c-121">Weitere Informationen zu den unterschiedlichen Lese Objekten finden Sie unter [Reader-Objekt](reader-object.md) und [synchrones Reader-Objekt](synchronous-reader-object.md).</span><span class="sxs-lookup"><span data-stu-id="1240c-121">For more information about the different reading objects, see [Reader Object](reader-object.md) and [Synchronous Reader Object](synchronous-reader-object.md).</span></span>

<span data-ttu-id="1240c-122">Im grundlegendsten asynchronen Datei Lese Szenario müssen Sie eine Rückruf Methode implementieren, die vom Reader-Objekt aufgerufen wird, wenn Beispiele bereit sind.</span><span class="sxs-lookup"><span data-stu-id="1240c-122">In the most basic asynchronous file reading scenario, you must implement a callback method that the reader object will call when samples are ready.</span></span> <span data-ttu-id="1240c-123">Nachdem Sie mit dem Lesen einer Datei begonnen haben, wartet die Anwendung darauf, dass die Beispiele an Ihre Rückruf Methode übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="1240c-123">After you begin reading a file, your application waits for the samples to be delivered to your callback method.</span></span> <span data-ttu-id="1240c-124">Asynchrones Lesen ist für Player Anwendungen nützlich und unterstützt Funktionen, die mit synchronem lesen nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="1240c-124">Asynchronous reading is useful for player applications, and supports features not available with synchronous reading.</span></span> <span data-ttu-id="1240c-125">Wenn Ihre Anwendung Dateien von einem Netzwerk Speicherort lesen oder mit einem Server interagieren muss, auf dem Windows Media Services ausgeführt wird, müssen Sie das Reader-Objekt verwenden.</span><span class="sxs-lookup"><span data-stu-id="1240c-125">If your application needs to read files from a network location, or interact with a server running Windows Media Services, you must use the reader object.</span></span> <span data-ttu-id="1240c-126">Der Nachteil des Reader-Objekts besteht darin, dass ein separater Thread für jede gelieferte Ausgabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1240c-126">The disadvantage of the reader object is that a separate thread is used for each output delivered.</span></span> <span data-ttu-id="1240c-127">Außerdem ist das Reader-Objekt nicht so flexibel wie der synchrone Reader in der Möglichkeit, Beispiele zu liefern.</span><span class="sxs-lookup"><span data-stu-id="1240c-127">Additionally, the reader object is not as flexible as the synchronous reader in how it can deliver samples.</span></span>

<span data-ttu-id="1240c-128">Mit dem synchronen Reader müssen keine Rückruf Methoden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1240c-128">With the synchronous reader you do not need to use any callback methods.</span></span> <span data-ttu-id="1240c-129">Stattdessen wählen Sie einen Teil der Datei aus, um die Beispiele einzeln mit Methoden aufrufen zu lesen und abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1240c-129">Instead, you select a portion of the file to read and retrieve the samples one at a time with method calls.</span></span> <span data-ttu-id="1240c-130">Der synchrone Reader eignet sich gut für die Anforderungen von Anwendungen zur Inhalts Bearbeitung, bei denen der schnelle Zugriff auf bestimmte Beispiele unabdingbar ist.</span><span class="sxs-lookup"><span data-stu-id="1240c-130">The synchronous reader is well suited to the needs of content-editing applications, where quick access to specific samples is essential.</span></span> <span data-ttu-id="1240c-131">Da vom synchronen Reader keine Rückruf Methoden verwendet werden, können Sie Anwendungen zum Lesen von ASF-Dateien mit minimalem Codierungsaufwand erstellen.</span><span class="sxs-lookup"><span data-stu-id="1240c-131">Because no callback methods are used by the synchronous reader, you can create applications to read ASF files with a minimum of coding overhead.</span></span> <span data-ttu-id="1240c-132">Der synchrone Reader kann jedoch keine Datei von einem Netzwerk Speicherort öffnen oder mit einem Server interagieren, auf dem Windows Media Services ausgeführt wird, oder Dateien lesen, die mit [*DRM*](wmformat-glossary.md)geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="1240c-132">However, the synchronous reader cannot open a file from a network location, or interact with a server running Windows Media Services, or read files protected with [*DRM*](wmformat-glossary.md).</span></span>

<span data-ttu-id="1240c-133">In den folgenden Themen werden die Funktionen des Readers und des synchronen Readers erläutert.</span><span class="sxs-lookup"><span data-stu-id="1240c-133">The following topics discuss the features of the reader and the synchronous reader.</span></span>



| <span data-ttu-id="1240c-134">Thema</span><span class="sxs-lookup"><span data-stu-id="1240c-134">Topic</span></span>                                                              | <span data-ttu-id="1240c-135">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1240c-135">Description</span></span>                                                                                                        |
|--------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1240c-136">Vom Benutzer zugewiesene Beispiel Unterstützung</span><span class="sxs-lookup"><span data-stu-id="1240c-136">User Allocated Sample Support</span></span>](user-allocated-sample-support.md) | <span data-ttu-id="1240c-137">Erläutert die Puffer Zuordnung im Reader und im synchronen Reader und wie die Benutzer Zuordnung die Leistung verbessern kann.</span><span class="sxs-lookup"><span data-stu-id="1240c-137">Discusses buffer allocation in the reader and synchronous reader, and how user allocation can improve performance.</span></span> |
| [<span data-ttu-id="1240c-138">Ausgabe Format-Enumeration</span><span class="sxs-lookup"><span data-stu-id="1240c-138">Output Format Enumeration</span></span>](output-format-enumeration.md)         | <span data-ttu-id="1240c-139">Erläutert die Enumeration des Ausgabeformats.</span><span class="sxs-lookup"><span data-stu-id="1240c-139">Discusses output format enumeration.</span></span>                                                                               |



 

<span data-ttu-id="1240c-140">Außerdem gelten die folgenden Themen aus dem Abschnitt Schreiben von Features auch für das Lesen von Dateien:</span><span class="sxs-lookup"><span data-stu-id="1240c-140">In addition, the following topics from the writing features section also apply to file reading:</span></span>

-   [<span data-ttu-id="1240c-141">Ändern der Größe von Videos</span><span class="sxs-lookup"><span data-stu-id="1240c-141">Video Resizing</span></span>](video-resizing.md)
-   [<span data-ttu-id="1240c-142">Farb Raum Konvertierung</span><span class="sxs-lookup"><span data-stu-id="1240c-142">Color Space Conversion</span></span>](color-space-conversion.md)
-   [<span data-ttu-id="1240c-143">Audioprobennahme</span><span class="sxs-lookup"><span data-stu-id="1240c-143">Audio Resampling</span></span>](audio-resampling.md)

## <a name="related-topics"></a><span data-ttu-id="1240c-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1240c-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1240c-145">**Aspekte**</span><span class="sxs-lookup"><span data-stu-id="1240c-145">**Features**</span></span>](features.md)
</dt> <dt>

[<span data-ttu-id="1240c-146">**Lesen von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="1240c-146">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




