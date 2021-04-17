---
title: Lesen von Dateien mit dem asynchronen Reader
description: Lesen von Dateien mit dem asynchronen Reader
ms.assetid: 3cc72f8d-bf1f-416d-bc90-21dfb92a55aa
keywords:
- Windows Media-Format-SDK, Lesen von Dateien
- SDK für den Windows Media-Format, asynchrone Leser
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- Advanced Systems Format (ASF), Lesen von Dateien
- ASF (Advanced Systems Format), Lesen von Dateien
- asynchrone Reader, iwmreadercallback-Schnittstelle
- Iwmreadercallback, asynchrone Reader
- asynchrone Leser, Lesen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0807c0701dd596f943010ad613b08ef9fe2c415c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389851"
---
# <a name="reading-files-with-the-asynchronous-reader"></a><span data-ttu-id="f7a74-112">Lesen von Dateien mit dem asynchronen Reader</span><span class="sxs-lookup"><span data-stu-id="f7a74-112">Reading Files with the Asynchronous Reader</span></span>

<span data-ttu-id="f7a74-113">Der asynchrone Reader liest den Inhalt aus den ASF-Dateien mit mehreren Threads und asynchronen Aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f7a74-113">The asynchronous reader reads the content from ASF files using multiple threads and asynchronous calls.</span></span> <span data-ttu-id="f7a74-114">Die Funktionen, die vom asynchronen Reader unterstützt werden, eignen sich gut für Anwendungen, die Inhalte für Endbenutzer darstellen.</span><span class="sxs-lookup"><span data-stu-id="f7a74-114">The features supported by the asynchronous reader make it well suited for applications that render content to end users.</span></span>

<span data-ttu-id="f7a74-115">Die grundlegende Funktionalität des Reader-Objekts kann in die folgenden Schritte aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="f7a74-115">The most basic functionality of the reader object can be broken down into the following steps.</span></span> <span data-ttu-id="f7a74-116">In den folgenden Schritten bezieht sich "die Anwendung" auf das Programm, das Sie mit dem Windows Media-Format-SDK schreiben.</span><span class="sxs-lookup"><span data-stu-id="f7a74-116">In these steps "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="f7a74-117">Die Anwendung implementiert die [**iwmreadercallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) -Schnittstelle zum Verarbeiten von Nachrichten vom Reader.</span><span class="sxs-lookup"><span data-stu-id="f7a74-117">The application implements the [**IWMReaderCallback**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadercallback) interface to handle messages from the reader.</span></span> <span data-ttu-id="f7a74-118">Dies schließt zwei Rückruf Methoden ein: **OnStatus**, das Nachrichten im Zusammenhang mit dem Status verschiedener Aspekte von Reader und **onsample** empfängt, die nicht komprimierte Beispiele vom Reader empfangen.</span><span class="sxs-lookup"><span data-stu-id="f7a74-118">This includes two callback methods: **OnStatus**, which receives messages relating to the status of various aspects of the reader and **OnSample**, which receives uncompressed samples from the reader.</span></span>
2.  <span data-ttu-id="f7a74-119">Die Anwendung übergibt an den Reader den Namen einer zu lesenden Datei.</span><span class="sxs-lookup"><span data-stu-id="f7a74-119">The application passes to the reader the name of a file to read.</span></span> <span data-ttu-id="f7a74-120">Wenn der Reader die Datei öffnet, wird jedem Stream eine Ausgabe Nummer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="f7a74-120">When the reader opens the file, it assigns an output number to each stream.</span></span> <span data-ttu-id="f7a74-121">Wenn die Datei einen gegenseitigen Ausschluss verwendet, weist der Reader eine einzelne Ausgabe für alle sich gegenseitig ausschließenden Streams zu.</span><span class="sxs-lookup"><span data-stu-id="f7a74-121">If the file uses mutual exclusion, the reader assigns a single output for all of the mutually exclusive streams.</span></span>
3.  <span data-ttu-id="f7a74-122">Die Anwendung ruft Informationen zur Konfiguration der verschiedenen Ausgaben des Readers ab.</span><span class="sxs-lookup"><span data-stu-id="f7a74-122">The application gets information about the configuration of the various outputs from the reader.</span></span> <span data-ttu-id="f7a74-123">Die gesammelten Informationen ermöglichen der Anwendung das ordnungsgemäße Rendering von Medien Beispielen.</span><span class="sxs-lookup"><span data-stu-id="f7a74-123">The information gathered will enable the application to properly render media samples.</span></span>
4.  <span data-ttu-id="f7a74-124">Die Anwendung weist den Reader an, mit dem Lesen von Daten aus der Datei zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="f7a74-124">The application instructs the reader to begin reading data from the file.</span></span> <span data-ttu-id="f7a74-125">Der Reader beginnt mit der Bereitstellung von nicht komprimierten Beispielen für den **onsample** -Rückruf nacheinander in Puffern, die in Puffer Objekten eingebunden sind.</span><span class="sxs-lookup"><span data-stu-id="f7a74-125">The reader begins delivering uncompressed samples to the **OnSample** callback one at a time in buffers wrapped in buffer objects.</span></span> <span data-ttu-id="f7a74-126">Die vom Reader gelieferten Beispiele sind in der Präsentationszeit sortiert.</span><span class="sxs-lookup"><span data-stu-id="f7a74-126">The samples delivered by the reader are in presentation-time order.</span></span> <span data-ttu-id="f7a74-127">Der Reader liefert weiterhin Beispiele, bis die Anwendung beendet wird oder bis das Ende der Datei erreicht ist.</span><span class="sxs-lookup"><span data-stu-id="f7a74-127">The reader will continue delivering samples until stopped by the application or until the end of the file is reached.</span></span>
5.  <span data-ttu-id="f7a74-128">Die Anwendung ist für das Rendern von Daten verantwortlich, nachdem Sie vom Reader zugestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f7a74-128">The application is responsible for rendering data after it is delivered by the reader.</span></span> <span data-ttu-id="f7a74-129">Das Windows Media-Format-SDK stellt keine renderingroutinen bereit.</span><span class="sxs-lookup"><span data-stu-id="f7a74-129">The Windows Media Format SDK does not provide any rendering routines.</span></span> <span data-ttu-id="f7a74-130">In der Regel verwenden Anwendungen andere SDKs zum Rendering von Daten, wie z. b. das Microsoft DirectX® SDK oder die Multimedia-Funktionen des Microsoft Windows Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="f7a74-130">Typically, applications will use other SDKs to render data, such as the Microsoft DirectX® SDK, or the multimedia functions of the Microsoft Windows Platform SDK.</span></span>
6.  <span data-ttu-id="f7a74-131">Wenn der Lesevorgang abgeschlossen ist, weist die Anwendung den Reader an, die Datei zu schließen.</span><span class="sxs-lookup"><span data-stu-id="f7a74-131">When reading is complete, the application instructs the reader to close the file.</span></span>

<span data-ttu-id="f7a74-132">Diese Schritte werden unter anderem in der Audioplayer-Beispielanwendung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f7a74-132">These steps are illustrated in the AudioPlayer sample application, among others.</span></span> <span data-ttu-id="f7a74-133">Weitere Informationen finden Sie unter [Beispielanwendungen](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="f7a74-133">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="f7a74-134">Der Reader unterstützt auch erweiterte Funktionen.</span><span class="sxs-lookup"><span data-stu-id="f7a74-134">The reader also supports more advanced functionality.</span></span> <span data-ttu-id="f7a74-135">Der Reader ermöglicht Ihnen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f7a74-135">The reader enables you to do the following:</span></span>

-   <span data-ttu-id="f7a74-136">Hält die Wiedergabe einer Datei an.</span><span class="sxs-lookup"><span data-stu-id="f7a74-136">Pause playback of a file.</span></span>
-   <span data-ttu-id="f7a74-137">Abrufen von Leistungsstatistiken für Reader.</span><span class="sxs-lookup"><span data-stu-id="f7a74-137">Retrieve reader performance statistics.</span></span>
-   <span data-ttu-id="f7a74-138">Steuern der Streamauswahl für sich gegenseitig ausschließende Streams.</span><span class="sxs-lookup"><span data-stu-id="f7a74-138">Control stream selection for mutually exclusive streams.</span></span>
-   <span data-ttu-id="f7a74-139">Puffer für Ausgabe manuell zuordnen.</span><span class="sxs-lookup"><span data-stu-id="f7a74-139">Manually allocate buffers for output.</span></span>
-   <span data-ttu-id="f7a74-140">Geben Sie eine eigene Uhr an.</span><span class="sxs-lookup"><span data-stu-id="f7a74-140">Provide your own clock.</span></span>
-   <span data-ttu-id="f7a74-141">Abrufen des Status von Datei Vorgängen (Pufferung, herunterladen oder speichern).</span><span class="sxs-lookup"><span data-stu-id="f7a74-141">Retrieve the status of file operations (buffering, download, or save).</span></span>
-   <span data-ttu-id="f7a74-142">Öffnen Sie eine Datei mit der Standard-COM-Schnittstelle **IStream**.</span><span class="sxs-lookup"><span data-stu-id="f7a74-142">Open a file using the standard COM interface, **IStream**.</span></span>
-   <span data-ttu-id="f7a74-143">Suchen Sie nach bestimmten Punkten in einer ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="f7a74-143">Seek to specific points in an ASF file.</span></span>
-   <span data-ttu-id="f7a74-144">Liest Profildaten aus dem Header der Datei.</span><span class="sxs-lookup"><span data-stu-id="f7a74-144">Read profile data from the header of the file.</span></span>

<span data-ttu-id="f7a74-145">In den folgenden Abschnitten wird die Verwendung des Reader-Objekts ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f7a74-145">The following sections describe the use of the reader object in detail.</span></span>

-   [<span data-ttu-id="f7a74-146">So implementieren Sie readernachrichten im OnStatus-Rückruf</span><span class="sxs-lookup"><span data-stu-id="f7a74-146">To Implement Reader Messages in the OnStatus Callback</span></span>](to-implement-reader-messages-in-the-onstatus-callback.md)
-   [<span data-ttu-id="f7a74-147">So implementieren Sie den onsample-Rückruf</span><span class="sxs-lookup"><span data-stu-id="f7a74-147">To Implement the OnSample Callback</span></span>](to-implement-the-onsample-callback.md)
-   [<span data-ttu-id="f7a74-148">So erstellen Sie einen Reader und öffnen eine Datei</span><span class="sxs-lookup"><span data-stu-id="f7a74-148">To Create a Reader and Open a File</span></span>](to-create-a-reader-and-open-a-file.md)
-   [<span data-ttu-id="f7a74-149">So rufen Sie Medien Beispiele mit dem asynchronen Reader ab</span><span class="sxs-lookup"><span data-stu-id="f7a74-149">To Retrieve Media Samples with the Asynchronous Reader</span></span>](to-retrieve-media-samples-with-the-asynchronous-reader.md)
-   [<span data-ttu-id="f7a74-150">So suchen Sie nach Zeit mithilfe des asynchronen Readers</span><span class="sxs-lookup"><span data-stu-id="f7a74-150">To Seek By Time Using the Asynchronous Reader</span></span>](to-seek-by-time-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="f7a74-151">So suchen Sie nach der Frame Nummer mithilfe des asynchronen Readers</span><span class="sxs-lookup"><span data-stu-id="f7a74-151">To Seek By Frame Number Using the Asynchronous Reader</span></span>](to-seek-by-frame-number-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="f7a74-152">So suchen Sie nach SMPTE-Zeit Code mithilfe des asynchronen Readers</span><span class="sxs-lookup"><span data-stu-id="f7a74-152">To Seek By SMPTE Time Code Using the Asynchronous Reader</span></span>](to-seek-by-smpte-time-code-using-the-asynchronous-reader.md)
-   [<span data-ttu-id="f7a74-153">So suchen Sie Marker</span><span class="sxs-lookup"><span data-stu-id="f7a74-153">To Seek to Markers</span></span>](to-seek-to-markers.md)
-   [<span data-ttu-id="f7a74-154">Anhalten oder Anhalten der Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="f7a74-154">To Pause or Stop Playback</span></span>](to-pause-or-stop-playback.md)
-   [<span data-ttu-id="f7a74-155">So erhalten Sie Leistungsstatistiken für Leser</span><span class="sxs-lookup"><span data-stu-id="f7a74-155">To Get Reader Performance Statistics</span></span>](to-get-reader-performance-statistics.md)
-   [<span data-ttu-id="f7a74-156">So verwenden Sie die manuelle Datenstrom Auswahl</span><span class="sxs-lookup"><span data-stu-id="f7a74-156">To Use Manual Stream Selection</span></span>](to-use-manual-stream-selection.md)
-   [<span data-ttu-id="f7a74-157">So liefern Sie komprimierte Beispiele mit dem asynchronen Reader</span><span class="sxs-lookup"><span data-stu-id="f7a74-157">To Deliver Compressed Samples with the Asynchronous Reader</span></span>](to-deliver-compressed-samples-with-the-asynchronous-reader.md)

## <a name="related-topics"></a><span data-ttu-id="f7a74-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f7a74-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7a74-159">**Lesen von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="f7a74-159">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="f7a74-160">**Reader-Objekt**</span><span class="sxs-lookup"><span data-stu-id="f7a74-160">**Reader Object**</span></span>](reader-object.md)
</dt> </dl>

 

 




