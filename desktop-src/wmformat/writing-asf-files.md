---
title: Schreiben von ASF-Dateien
description: Schreiben von ASF-Dateien
ms.assetid: d722b676-bf65-4f91-8118-bb12d3bbb6cb
keywords:
- Windows Media-Format-SDK, Schreiben von ASF-Dateien
- Windows Media-Format-SDK, Erstellen von ASF-Dateien
- Windows Media-Format-SDK, Advanced Systems Format (ASF)
- Advanced Systems Format (ASF), Schreiben von Dateien
- ASF (Advanced Systems Format), Schreiben von Dateien
- Advanced Systems Format (ASF), Erstellen von Dateien
- ASF (Advanced Systems Format), Erstellen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c13c1af0d3699c89d26f007e00675ea563639c4e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103858007"
---
# <a name="writing-asf-files"></a><span data-ttu-id="da27d-110">Schreiben von ASF-Dateien</span><span class="sxs-lookup"><span data-stu-id="da27d-110">Writing ASF Files</span></span>

<span data-ttu-id="da27d-111">Sie können das Writer-Objekt des SDK für den Windows Media-Format verwenden, um ASF-Dateien aus digitalen Mediendaten zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="da27d-111">You can use the writer object of the Windows Media Format SDK to create ASF files from digital media data.</span></span> <span data-ttu-id="da27d-112">Um eine Instanz des Writer-Objekts zu erstellen, rufen Sie die [**wmkreatewriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="da27d-112">To create an instance of the writer object, call the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function.</span></span> <span data-ttu-id="da27d-113">Das Writer-Objekt koordiniert die Funktionalität einer Reihe von Komponenten, einschließlich Codecs, die für das Windows Media-Format-SDK extern sind.</span><span class="sxs-lookup"><span data-stu-id="da27d-113">The writer object coordinates the functionality of a number of components, including codecs, which are external to the Windows Media Format SDK.</span></span>

<span data-ttu-id="da27d-114">Die grundlegende Funktionalität des Writer-Objekts kann in die folgenden Schritte aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="da27d-114">The basic functionality of the writer object can be broken down into the following steps.</span></span> <span data-ttu-id="da27d-115">In den folgenden Schritten bezieht sich "die Anwendung" auf das Programm, das Sie mit dem Windows Media-Format-SDK schreiben.</span><span class="sxs-lookup"><span data-stu-id="da27d-115">In these steps, "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="da27d-116">Die Anwendung stellt dem Writer ein Profil zur Verfügung, das beim Erstellen der ASF-Datei verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="da27d-116">The application supplies the writer with a profile to use in creating the ASF file.</span></span> <span data-ttu-id="da27d-117">Wenn der Writer die Profildaten lädt, wird jeder Verbindung des Profils eine Eingabe Nummer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="da27d-117">When the writer loads the profile data, it assigns an input number to each connection of the profile.</span></span>
2.  <span data-ttu-id="da27d-118">Die Anwendung stellt dem Writer einen Ausgabe Dateinamen für die Datei zur Verfügung, die geschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="da27d-118">The application supplies the writer with an output file name for the file to be written.</span></span> <span data-ttu-id="da27d-119">Der Writer erstellt ein Writer-Datei-Sink-Objekt, um die Erstellung und Eingabe von Dateien zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="da27d-119">The writer creates a writer file sink object to manage the file creation and input.</span></span> <span data-ttu-id="da27d-120">Weitere Informationen finden Sie unter [Writer File Sink Object](writer-file-sink-object.md).</span><span class="sxs-lookup"><span data-stu-id="da27d-120">For more information, see [Writer File Sink Object](writer-file-sink-object.md).</span></span>
3.  <span data-ttu-id="da27d-121">Der Writer erstellt basierend auf den Informationen im Profil einen Header für die neue Datei.</span><span class="sxs-lookup"><span data-stu-id="da27d-121">The writer creates a header for the new file based on information in the profile.</span></span>
4.  <span data-ttu-id="da27d-122">Die Anwendung übergibt nicht komprimierte Beispiele an den Writer.</span><span class="sxs-lookup"><span data-stu-id="da27d-122">The application passes uncompressed samples to the writer.</span></span> <span data-ttu-id="da27d-123">Die Beispiele werden nacheinander in Puffern in Puffer Objekten übermittelt.</span><span class="sxs-lookup"><span data-stu-id="da27d-123">Samples are passed one at a time in buffers wrapped in buffer objects.</span></span> <span data-ttu-id="da27d-124">Die Anwendung sollte die Beispiele für jeden Stream gleichzeitig übergeben, damit der Writer alle Beispiele in der Präsentationszeit Reihenfolge empfängt.</span><span class="sxs-lookup"><span data-stu-id="da27d-124">The application should pass samples for each stream concurrently so that the writer receives all samples in presentation-time order.</span></span>
5.  <span data-ttu-id="da27d-125">Der Writer übergibt die Beispiele für die Komprimierung an den entsprechenden Codec.</span><span class="sxs-lookup"><span data-stu-id="da27d-125">The writer passes the samples to the appropriate codec for compression.</span></span> <span data-ttu-id="da27d-126">Wenn der Writer die komprimierten Beispiele empfängt, werden diese mit Beispielen aus den anderen Datenströmen verknüpft, sodass Beispiele unabhängig vom Stream in der Präsentationszeit Reihenfolge in die Datei gelangen.</span><span class="sxs-lookup"><span data-stu-id="da27d-126">When the writer receives the compressed samples, it interleaves them with samples from the other streams so that samples go into the file in presentation time order irrespective of stream.</span></span> <span data-ttu-id="da27d-127">Die Beispiel Daten werden dann in Pakete erstellt und in den Daten Abschnitt der Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="da27d-127">The sample data is then made into packets and written to the data section of the file.</span></span>
6.  <span data-ttu-id="da27d-128">Wenn alle Beispiele verarbeitet werden, kann der Writer der Datei einen Index hinzufügen, um die Suchleistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="da27d-128">When all samples are processed, the writer can add an index to the file to enhance seeking performance.</span></span>

<span data-ttu-id="da27d-129">Diese Schritte werden unter anderem in der wmstats-Beispielanwendung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="da27d-129">These steps are illustrated in the WMStats sample application, among others.</span></span> <span data-ttu-id="da27d-130">Weitere Informationen finden Sie unter [Beispielanwendungen](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="da27d-130">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="da27d-131">Der Writer unterstützt auch erweiterte Funktionen, sodass Sie die folgenden Aufgaben ausführen können:</span><span class="sxs-lookup"><span data-stu-id="da27d-131">The writer also supports more advanced functionality, enabling you to do the following:</span></span>

-   <span data-ttu-id="da27d-132">Bearbeiten Sie die Metadaten im Header der Datei.</span><span class="sxs-lookup"><span data-stu-id="da27d-132">Edit metadata in the header of the file.</span></span>
-   <span data-ttu-id="da27d-133">Schreiben Sie vorkomprimierte Beispiele.</span><span class="sxs-lookup"><span data-stu-id="da27d-133">Write precompressed samples.</span></span>
-   <span data-ttu-id="da27d-134">Schreiben in Netzwerk senken für das Streamen von Livedaten.</span><span class="sxs-lookup"><span data-stu-id="da27d-134">Write to network sinks for streaming live data.</span></span>
-   <span data-ttu-id="da27d-135">Schreiben in Datei senken für erweiterte Optionen für die Datei Steuerung.</span><span class="sxs-lookup"><span data-stu-id="da27d-135">Write to file sinks for advanced file control options.</span></span>
-   <span data-ttu-id="da27d-136">Schreiben Sie in pushsenken für die Verteilung auf Server, die Endbenutzern Inhalte bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="da27d-136">Write to push sinks for distribution to servers that will deliver content to end users.</span></span>
-   <span data-ttu-id="da27d-137">Übermitteln Sie Postview-Beispiele für die Überprüfung der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="da27d-137">Deliver postview samples for verification of output.</span></span>
-   <span data-ttu-id="da27d-138">Übermitteln von Writer-Leistungsstatistiken.</span><span class="sxs-lookup"><span data-stu-id="da27d-138">Deliver writer-performance statistics.</span></span>

<span data-ttu-id="da27d-139">In den folgenden Abschnitten wird die Verwendung des Writer-Objekts ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="da27d-139">The following sections describe the use of the writer object in detail.</span></span>



| <span data-ttu-id="da27d-140">`Section`</span><span class="sxs-lookup"><span data-stu-id="da27d-140">Section</span></span>                                                                    | <span data-ttu-id="da27d-141">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da27d-141">Description</span></span>                                                                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="da27d-142">Verwenden von Profilen mit dem Writer</span><span class="sxs-lookup"><span data-stu-id="da27d-142">To Use Profiles with the Writer</span></span>](to-use-profiles-with-the-writer.md)     | <span data-ttu-id="da27d-143">Beschreibt, wie Sie ein Profil angeben, das mit dem Writer verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="da27d-143">Describes how to specify a profile to use with the writer.</span></span>                                             |
| [<span data-ttu-id="da27d-144">Arbeiten mit Eingaben</span><span class="sxs-lookup"><span data-stu-id="da27d-144">Working with Inputs</span></span>](working-with-inputs.md)                             | <span data-ttu-id="da27d-145">Beschreibt, wie die Eingabeeinstellungen im Writer identifiziert und konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="da27d-145">Describes how to identify and configure the input settings in the writer.</span></span>                              |
| [<span data-ttu-id="da27d-146">So bearbeiten Sie Metadaten mit dem Writer</span><span class="sxs-lookup"><span data-stu-id="da27d-146">To Edit Metadata with the Writer</span></span>](to-edit-metadata-with-the-writer.md)   | <span data-ttu-id="da27d-147">Beschreibt, wie der Writer zum Bearbeiten von Metadaten für eine neue Datei verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="da27d-147">Describes how to use the writer to edit metadata for a new file.</span></span>                                       |
| [<span data-ttu-id="da27d-148">So schreiben Sie Beispiele</span><span class="sxs-lookup"><span data-stu-id="da27d-148">To Write Samples</span></span>](to-write-samples.md)                                   | <span data-ttu-id="da27d-149">Beschreibt, wie Beispiele an den Writer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="da27d-149">Describes how to pass samples to the writer.</span></span>                                                           |
| [<span data-ttu-id="da27d-150">Festlegen von Dateneinheiten Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="da27d-150">Setting Data Unit Extensions</span></span>](setting-data-unit-extensions.md)           | <span data-ttu-id="da27d-151">Hier wird beschrieben, wie Sie den Beispielen erweiterte Daten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="da27d-151">Describes how to add extended data to samples.</span></span>                                                         |
| [<span data-ttu-id="da27d-152">Schreiben von komprimierten Beispielen</span><span class="sxs-lookup"><span data-stu-id="da27d-152">Writing Compressed Samples</span></span>](writing-compressed-samples.md)               | <span data-ttu-id="da27d-153">Beschreibt, wie vorkomprimierte Beispiele an den Writer übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="da27d-153">Describes how to pass pre-compressed samples to the writer.</span></span>                                            |
| [<span data-ttu-id="da27d-154">Schreiben von bildstreams</span><span class="sxs-lookup"><span data-stu-id="da27d-154">Writing Image Streams</span></span>](writing-image-streams.md)                         | <span data-ttu-id="da27d-155">Beschreibt, wie eine Eingabe für einen Bildstream konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="da27d-155">Describes how to configure an input for an image stream.</span></span>                                               |
| [<span data-ttu-id="da27d-156">Schreiben von Video Bildbeispielen</span><span class="sxs-lookup"><span data-stu-id="da27d-156">Writing Video Image Samples</span></span>](writing-video-image-samples.md)             | <span data-ttu-id="da27d-157">Beschreibt, wie Video Bildbeispiele konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="da27d-157">Describes how to configure Video Image samples.</span></span>                                                        |
| [<span data-ttu-id="da27d-158">Schreiben von variablenbitrate-Streams</span><span class="sxs-lookup"><span data-stu-id="da27d-158">Writing Variable Bit Rate Streams</span></span>](writing-variable-bit-rate-streams.md) | <span data-ttu-id="da27d-159">Beschreibt das Schreiben von Datenströmen variabler Bitrate (VBR).</span><span class="sxs-lookup"><span data-stu-id="da27d-159">Describes how to write variable bit rate (VBR) streams.</span></span>                                                |
| [<span data-ttu-id="da27d-160">Verwenden von Two-Pass Codierung</span><span class="sxs-lookup"><span data-stu-id="da27d-160">Using Two-Pass Encoding</span></span>](using-two-pass-encoding.md)                     | <span data-ttu-id="da27d-161">Beschreibt, wie der Codec einen vorläufigen Durchlauf vor dem Schreiben der Datei durchführt.</span><span class="sxs-lookup"><span data-stu-id="da27d-161">Describes how to have the codec perform a preliminary pass before writing the file.</span></span>                    |
| [<span data-ttu-id="da27d-162">So erzwingen Sie Key-Frame einfügen</span><span class="sxs-lookup"><span data-stu-id="da27d-162">To Force Key-Frame Insertion</span></span>](to-force-key-frame-insertion.md)           | <span data-ttu-id="da27d-163">Beschreibt, wie der Codec manuell erzwungen wird, um ein Beispiel als Keyframe zu codieren.</span><span class="sxs-lookup"><span data-stu-id="da27d-163">Describes how to manually force the codec to encode a sample as a key frame.</span></span>                           |
| [<span data-ttu-id="da27d-164">So verwalten Sie die Schreib Latenz</span><span class="sxs-lookup"><span data-stu-id="da27d-164">To Manage Writer Latency</span></span>](to-manage-writer-latency.md)                   | <span data-ttu-id="da27d-165">Beschreibt, wie Sie die Zeit minimieren, die der Writer zum Verarbeiten von Beispielen in eine Ausgabedatei oder-Senke benötigt.</span><span class="sxs-lookup"><span data-stu-id="da27d-165">Describes how to minimize the time it takes the writer to process samples into an output file or sink.</span></span> |
| [<span data-ttu-id="da27d-166">Arbeiten mit Writer-senken</span><span class="sxs-lookup"><span data-stu-id="da27d-166">Working with Writer Sinks</span></span>](working-with-writer-sinks.md)                 | <span data-ttu-id="da27d-167">Beschreibt die Verwendung von Writer-senken zum Übermitteln Ihrer Inhalte an Dateien oder Netzwerkspeicher Orte.</span><span class="sxs-lookup"><span data-stu-id="da27d-167">Describes how to use writer sinks to deliver your content to files or network locations.</span></span>               |
| [<span data-ttu-id="da27d-168">So erhalten Sie eine Writer-Statistik</span><span class="sxs-lookup"><span data-stu-id="da27d-168">To Get Writer Statistics</span></span>](to-get-writer-statistics.md)                   | <span data-ttu-id="da27d-169">Beschreibt, wie Statistiken für den Writer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="da27d-169">Describes how to get statistics for the writer.</span></span>                                                        |
| [<span data-ttu-id="da27d-170">So verwenden Sie die Writer-Postview</span><span class="sxs-lookup"><span data-stu-id="da27d-170">To Use Writer Postview</span></span>](to-use-writer-postview.md)                       | <span data-ttu-id="da27d-171">Beschreibt, wie nicht komprimierte Beispiele beim Schreiben einer Datei zur Überprüfung erhalten werden.</span><span class="sxs-lookup"><span data-stu-id="da27d-171">Describes how to get uncompressed samples as you write a file for verification.</span></span>                        |



 

## <a name="related-topics"></a><span data-ttu-id="da27d-172">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="da27d-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="da27d-173">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="da27d-173">**Programming Guide**</span></span>](programming-guide.md)
</dt> <dt>

[<span data-ttu-id="da27d-174">**Writer-Dateisenke (Objekt)**</span><span class="sxs-lookup"><span data-stu-id="da27d-174">**Writer File Sink Object**</span></span>](writer-file-sink-object.md)
</dt> <dt>

[<span data-ttu-id="da27d-175">**Writer-netzwerksink-Objekt**</span><span class="sxs-lookup"><span data-stu-id="da27d-175">**Writer Network Sink Object**</span></span>](writer-network-sink-object.md)
</dt> <dt>

[<span data-ttu-id="da27d-176">**Writer-Objekt**</span><span class="sxs-lookup"><span data-stu-id="da27d-176">**Writer Object**</span></span>](writer-object.md)
</dt> </dl>

 

 




