---
title: Verwenden von Dateisenken
description: Verwenden von Dateisenken
ms.assetid: 0cc4320a-c975-452d-bd1c-394d43bd4585
keywords:
- Advanced Systems Format (ASF), Datei senken
- ASF (Advanced Systems Format), Datei senken
- Advanced Systems Format (ASF), senken
- ASF (Advanced Systems Format), senken
- senken, Datei senken
- Datei senken, Informationen zu
- Datei senken, erstellen
- Datei senken, beenden
- Datei senken, starten
- Datei senken, schließen
- senken, Statistiken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c7a7f09a08788128719ea80a2a06d339f6398e6
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101343"
---
# <a name="using-file-sinks"></a><span data-ttu-id="8341c-114">Verwenden von Dateisenken</span><span class="sxs-lookup"><span data-stu-id="8341c-114">Using File Sinks</span></span>

<span data-ttu-id="8341c-115">Normalerweise können Sie dem Writer einfach einen Ausgabe Dateinamen mithilfe der [**iwmwriter:: setoutputfilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) -Methode übergeben, und das Writer-Objekt schreibt die Datei automatisch auf den Datenträger.</span><span class="sxs-lookup"><span data-stu-id="8341c-115">Under normal circumstances, you can simply pass the writer an output file name using the [**IWMWriter::SetOutputFilename**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename) method, and the writer object will write the file to disk automatically.</span></span> <span data-ttu-id="8341c-116">In diesem Fall erstellt und steuert der Writer tatsächlich ein Writer-Datei-Sink-Objekt, das das Schreiben der Datei auf den Datenträger behandelt.</span><span class="sxs-lookup"><span data-stu-id="8341c-116">In this case, the writer is actually creating and controlling a writer file sink object that handles writing the file to disk.</span></span> <span data-ttu-id="8341c-117">Ein Writer-Datei-Senkenobjekt steuert den Datenfluss vom Writer-Objekt zu einer einzelnen Datei.</span><span class="sxs-lookup"><span data-stu-id="8341c-117">A writer file sink object controls the flow of data from the writer object to a single file.</span></span>

<span data-ttu-id="8341c-118">Sie können eigene dateisenken erstellen, um mehr Kontrolle darüber zu erhalten, wie die Senke die Datei schreibt.</span><span class="sxs-lookup"><span data-stu-id="8341c-118">You can create your own file sinks to get more control over how the sink writes the file.</span></span> <span data-ttu-id="8341c-119">Sie können auch auf die standardmäßige Writer-Datei-Senke zugreifen, die vom Writer als Reaktion auf einen Aufrufen von **setoutputfilename** erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8341c-119">You can also access the default writer file sink created by the writer in response to a call to **SetOutputFilename**.</span></span>

## <a name="creating-file-sinks"></a><span data-ttu-id="8341c-120">Erstellen von Datei senken</span><span class="sxs-lookup"><span data-stu-id="8341c-120">Creating File Sinks</span></span>

<span data-ttu-id="8341c-121">Führen Sie die folgenden Schritte aus, um eine Datei Senke zu erstellen und Sie dem Writer hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="8341c-121">To create a file sink and add it to the writer, perform the following steps.</span></span>

1.  <span data-ttu-id="8341c-122">Erstellen Sie eine neue Senke, indem Sie die [**wmcreateschreiterfilesink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8341c-122">Create a new sink by calling the [**WMCreateWriterFileSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink) function.</span></span>
2.  <span data-ttu-id="8341c-123">Geben Sie einen Dateinamen für die Senke an, indem Sie [**iwmschreiterfilesink:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8341c-123">Supply a file name for the sink by calling [**IWMWriterFileSink::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink-open).</span></span>
3.  <span data-ttu-id="8341c-124">Fügen Sie dem Writer die File-Senke hinzu, indem Sie [**iwmschreiteradvanced:: addsink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8341c-124">Add the file sink to the writer by calling [**IWMWriterAdvanced::AddSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink).</span></span>
4.  <span data-ttu-id="8341c-125">Führen Sie Schreibvorgänge auf die übliche Weise aus.</span><span class="sxs-lookup"><span data-stu-id="8341c-125">Perform writing in the usual way.</span></span>
5.  <span data-ttu-id="8341c-126">Nachdem das Schreiben abgeschlossen ist, wird die Datei automatisch von der Senke geschlossen.</span><span class="sxs-lookup"><span data-stu-id="8341c-126">After writing is completed, the sink will close the file automatically.</span></span>

## <a name="stopping-and-starting-file-sinks"></a><span data-ttu-id="8341c-127">Beenden und starten von Datei senken</span><span class="sxs-lookup"><span data-stu-id="8341c-127">Stopping and Starting File Sinks</span></span>

<span data-ttu-id="8341c-128">Nachdem das Schreiben von Vorgängen begonnen hat, können Sie das Schreiben in eine Datei Senke durch Aufrufen von [**IWMWriterFileSink2:: Beendigung**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop)abbrechen.</span><span class="sxs-lookup"><span data-stu-id="8341c-128">After writing operations begin, you can stop writing to a file sink by calling [**IWMWriterFileSink2::Stop**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-stop).</span></span>

<span data-ttu-id="8341c-129">Es gibt viele mögliche Gründe, warum das Schreiben in eine Senke beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8341c-129">There are many potential reasons why you would want to stop writing to a sink.</span></span> <span data-ttu-id="8341c-130">Wenn Sie z. b. von einer Live Quelle aufzeichnen, sind Sie möglicherweise nur an einem Teil des Inhalts interessiert.</span><span class="sxs-lookup"><span data-stu-id="8341c-130">For example, if you are recording from a live source, you may only be interested in some of the content.</span></span>

<span data-ttu-id="8341c-131">Sie können das Schreiben in eine Datei Senke fortsetzen, indem Sie [**IWMWriterFileSink2:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8341c-131">You can resume writing to a file sink by calling [**IWMWriterFileSink2::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-start).</span></span> <span data-ttu-id="8341c-132">Sowohl **Beenden** als auch **starten** verwenden Präsentations Zeiten, um ungefähr zu steuern, wann der Befehl ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8341c-132">Both **Stop** and **Start** use presentation times to control approximately when the command is executed.</span></span> <span data-ttu-id="8341c-133">Sie können die [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) -Methoden verwenden, um mehr Kontrolle über Start-und Endzeit Zeiten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8341c-133">You can use the [**IWMWriterFileSink3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3) methods to gain more control over start and stop times.</span></span>

## <a name="closing-file-sinks"></a><span data-ttu-id="8341c-134">Schließen von Datei senken</span><span class="sxs-lookup"><span data-stu-id="8341c-134">Closing File Sinks</span></span>

<span data-ttu-id="8341c-135">Normalerweise wird eine Datei Senke automatisch geschlossen.</span><span class="sxs-lookup"><span data-stu-id="8341c-135">Normally, a file sink is closed automatically.</span></span> <span data-ttu-id="8341c-136">Wenn Sie mit dem Schreiben in eine Senke fertig sind, aber das Schreiben von Vorgängen in andere senken fortgesetzt wird, sollten Sie die Senke explizit schließen, um Ressourcen zu sparen.</span><span class="sxs-lookup"><span data-stu-id="8341c-136">If you are finished writing to a sink, but writing operations to other sinks are continuing, you should explicitly close the sink to conserve resources.</span></span> <span data-ttu-id="8341c-137">Um eine File-Senke zu schließen, nennen Sie [**IWMWriterFileSink2:: Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).</span><span class="sxs-lookup"><span data-stu-id="8341c-137">To close a file sink, call [**IWMWriterFileSink2::Close**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-close).</span></span>

## <a name="getting-sink-statistics"></a><span data-ttu-id="8341c-138">Senke Statistiken werden erhalten</span><span class="sxs-lookup"><span data-stu-id="8341c-138">Getting Sink Statistics</span></span>

<span data-ttu-id="8341c-139">Sie können die Dateigröße und-Dauer für eine geöffnete Senke abrufen, indem Sie [**IWMWriterFileSink2:: GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) und [**IWMWriterFileSink2:: getfileduration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8341c-139">You can get the file size and duration for an open sink by calling [**IWMWriterFileSink2::GetFileSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfilesize) and [**IWMWriterFileSink2::GetFileDuration**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink2-getfileduration) respectively.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8341c-140">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8341c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8341c-141">**Iwmschreiterfilesink-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8341c-141">**IWMWriterFileSink Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink)
</dt> <dt>

[<span data-ttu-id="8341c-142">**IWMWriterFileSink2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8341c-142">**IWMWriterFileSink2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink2)
</dt> <dt>

[<span data-ttu-id="8341c-143">**IWMWriterFileSink3-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="8341c-143">**IWMWriterFileSink3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterfilesink3)
</dt> <dt>

[<span data-ttu-id="8341c-144">**Writer-Dateisenke (Objekt)**</span><span class="sxs-lookup"><span data-stu-id="8341c-144">**Writer File Sink Object**</span></span>](writer-file-sink-object.md)
</dt> <dt>

[<span data-ttu-id="8341c-145">**Schreiben von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="8341c-145">**Writing ASF Files**</span></span>](writing-asf-files.md)
</dt> </dl>

 

 




