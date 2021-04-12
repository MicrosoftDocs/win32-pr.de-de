---
title: Lesen von Dateien mit dem synchronen Reader
description: Lesen von Dateien mit dem synchronen Reader
ms.assetid: 18c6c0cd-478f-4325-b23e-571c33779a96
keywords:
- Windows Media-Format-SDK, Lesen von Dateien
- SDK für den Windows Media-Format, synchrone Reader
- Advanced Systems Format (ASF), synchrone Reader
- ASF (Advanced Systems Format), synchrone Reader
- Advanced Systems Format (ASF), Lesen von Dateien
- ASF (Advanced Systems Format), Lesen von Dateien
- synchrone Reader, iwmreadercallback-Schnittstelle
- Iwmreadercallback, synchrone Reader
- synchrone Leser, Lesen von Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 893a1bd324cdc91968e423f2084bfdba5ef57c8e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389850"
---
# <a name="reading-files-with-the-synchronous-reader"></a><span data-ttu-id="eb118-112">Lesen von Dateien mit dem synchronen Reader</span><span class="sxs-lookup"><span data-stu-id="eb118-112">Reading Files with the Synchronous Reader</span></span>

<span data-ttu-id="eb118-113">Sie können den synchronen Reader verwenden, um eine ASF-Datei mit synchronen Aufrufen anstelle der asynchronen Methoden im Reader-Objekt zu lesen.</span><span class="sxs-lookup"><span data-stu-id="eb118-113">You can use the synchronous reader to read an ASF file using synchronous calls instead of the asynchronous methods in the reader object.</span></span> <span data-ttu-id="eb118-114">Die Verwendung von synchronen Aufrufen reduziert die Anzahl der Threads, die zum Lesen einer Datei erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="eb118-114">Using synchronous calls reduces the number of threads required to read a file.</span></span> <span data-ttu-id="eb118-115">Der asynchrone Reader verwendet mehrere Threads, um Datenströme zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="eb118-115">The asynchronous reader uses multiple threads for processing streams.</span></span> <span data-ttu-id="eb118-116">Für Dateien mit mehreren Streams kann die Anzahl der verwendeten Threads sehr groß werden.</span><span class="sxs-lookup"><span data-stu-id="eb118-116">For files with multiple streams, the number of threads used can become very large.</span></span> <span data-ttu-id="eb118-117">Der synchrone Reader verwendet nur einen Thread.</span><span class="sxs-lookup"><span data-stu-id="eb118-117">The synchronous reader uses only one thread.</span></span>

<span data-ttu-id="eb118-118">Der synchrone Reader wurde entwickelt, um die Anforderungen der Inhaltserstellung und der Datei Bearbeitungsanwendungen zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="eb118-118">The synchronous reader was designed to meet the needs of content creation and file editing applications.</span></span> <span data-ttu-id="eb118-119">Sie können den synchronen Reader für andere Anwendungen verwenden, seine Funktionalität ist jedoch begrenzt.</span><span class="sxs-lookup"><span data-stu-id="eb118-119">You can use the synchronous reader for other applications, but its functionality is limited.</span></span>

<span data-ttu-id="eb118-120">Der synchrone Reader kann lokale Dateien oder Dateien in einem Netzwerk mithilfe des UNC-Pfadnamens öffnen (z \\ \\ . b. "someshare \\ somedirectory \\ somefile. wmv").</span><span class="sxs-lookup"><span data-stu-id="eb118-120">The synchronous reader can open files that are local, or files on a network using the UNC path name (such as "\\\\someshare\\somedirectory\\somefile.wmv").</span></span> <span data-ttu-id="eb118-121">Sie können keine Dateien an den synchronen Reader streamen oder Dateien von einem Internet Speicherort aus öffnen.</span><span class="sxs-lookup"><span data-stu-id="eb118-121">You cannot stream files to the synchronous reader, or open files from an Internet location.</span></span> <span data-ttu-id="eb118-122">Der synchrone Reader bietet auch Unterstützung für die Verwendung der **IStream** -com-Schnittstelle als Quelle.</span><span class="sxs-lookup"><span data-stu-id="eb118-122">The synchronous reader also provides support for using the **IStream** COM interface as a source.</span></span>

<span data-ttu-id="eb118-123">Der synchrone Reader bietet mehr Flexibilität beim Abrufen von Beispielen aus einer ASF-Datei als der asynchrone Reader.</span><span class="sxs-lookup"><span data-stu-id="eb118-123">The synchronous reader provides more versatility for retrieving samples from an ASF file than the asynchronous reader.</span></span> <span data-ttu-id="eb118-124">Der synchrone Reader kann Beispiele nach streamnummer und Ausgabe bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="eb118-124">The synchronous reader can deliver samples by stream number as well as by output.</span></span> <span data-ttu-id="eb118-125">Die von der Datenstrom Nummer übermittelten Beispiele können komprimiert oder dekomprimiert werden.</span><span class="sxs-lookup"><span data-stu-id="eb118-125">Samples delivered by stream number can be compressed or uncompressed.</span></span> <span data-ttu-id="eb118-126">Der synchrone Reader kann während der Wiedergabe auch zwischen komprimierter und nicht komprimierter Übermittlung wechseln. Diese Funktion wird als "schnelles bearbeiten" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="eb118-126">The synchronous reader can also switch between compressed and uncompressed delivery during playback; this feature is known as "fast editing."</span></span> <span data-ttu-id="eb118-127">Diese Funktion ermöglicht es einer Bearbeitungs Anwendung, Windows Media-basierte Inhalte zu lesen und direkt an den Writer weiterzuleiten, bis ein gewünschter Frame erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="eb118-127">This feature enables an editing application to read Windows Media-based content and pass it directly through to the writer until a desired frame is reached.</span></span> <span data-ttu-id="eb118-128">An diesem Punkt kann die Anwendung den Reader anweisen, nicht komprimierte Inhalte bereitzustellen, die von der Anwendung dann geändert und zur erneuten Komprimierung an den Writer übergeben werden können.</span><span class="sxs-lookup"><span data-stu-id="eb118-128">At that point the application can tell the reader to start delivering uncompressed content, which the application can then modify and pass to the writer for recompression.</span></span> <span data-ttu-id="eb118-129">Wenn die Anwendung das Ändern der angegebenen Frames abgeschlossen hat, kann Sie den Reader anweisen, mit der Übermittlung von komprimierten Frames zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="eb118-129">When the application has finished modifying the specified frames, it can tell the reader to start delivering compressed frames again.</span></span>

<span data-ttu-id="eb118-130">Die grundlegende Funktionalität des synchronen Reader-Objekts kann in die folgenden Schritte aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="eb118-130">The most basic functionality of the synchronous reader object can be broken down into the following steps.</span></span> <span data-ttu-id="eb118-131">In den folgenden Schritten bezieht sich "die Anwendung" auf das Programm, das Sie mit dem Windows Media-Format-SDK schreiben.</span><span class="sxs-lookup"><span data-stu-id="eb118-131">In these steps "the application" refers to the program you write using the Windows Media Format SDK.</span></span>

1.  <span data-ttu-id="eb118-132">Die Anwendung übergibt dem synchronen Reader den Namen einer zu lesenden Datei.</span><span class="sxs-lookup"><span data-stu-id="eb118-132">The application passes to the synchronous reader the name of a file to read.</span></span> <span data-ttu-id="eb118-133">Wenn die Datei vom synchronen Reader geöffnet wird, wird jedem Stream eine Ausgabe Nummer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="eb118-133">When the synchronous reader opens the file, it assigns an output number to each stream.</span></span> <span data-ttu-id="eb118-134">Wenn die Datei einen gegenseitigen Ausschluss verwendet, weist der Reader eine einzelne Ausgabe für alle sich gegenseitig ausschließenden Streams zu.</span><span class="sxs-lookup"><span data-stu-id="eb118-134">If the file uses mutual exclusion, the reader assigns a single output for all of the mutually exclusive streams.</span></span>
2.  <span data-ttu-id="eb118-135">Die Anwendung ruft Informationen zur Konfiguration der verschiedenen Ausgaben des Readers ab.</span><span class="sxs-lookup"><span data-stu-id="eb118-135">The application gets information about the configuration of the various outputs from the reader.</span></span> <span data-ttu-id="eb118-136">Die gesammelten Informationen ermöglichen der Anwendung das ordnungsgemäße Rendering von Medien Beispielen.</span><span class="sxs-lookup"><span data-stu-id="eb118-136">The information gathered will enable the application to properly render media samples.</span></span>
3.  <span data-ttu-id="eb118-137">Die Anwendung beginnt, nacheinander Beispiele vom synchronen Reader anzufordern.</span><span class="sxs-lookup"><span data-stu-id="eb118-137">The application begins requesting samples, one at a time, from the synchronous reader.</span></span> <span data-ttu-id="eb118-138">Der synchrone Reader stellt jedes Beispiel in einem Puffer Objekt bereit, für das es die [**inssbuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) -Schnittstelle übermittelt.</span><span class="sxs-lookup"><span data-stu-id="eb118-138">The synchronous reader delivers each sample in a buffer object for which it delivers the [**INSSBuffer**](/previous-versions/windows/desktop/api/wmsbuffer/nn-wmsbuffer-inssbuffer) interface.</span></span>
4.  <span data-ttu-id="eb118-139">Die Anwendung ist für das Rendern von Daten verantwortlich, nachdem Sie vom Reader zugestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="eb118-139">The application is responsible for rendering data after it is delivered by the reader.</span></span> <span data-ttu-id="eb118-140">Das Windows Media-Format-SDK stellt keine renderingroutinen bereit.</span><span class="sxs-lookup"><span data-stu-id="eb118-140">The Windows Media Format SDK does not provide any rendering routines.</span></span> <span data-ttu-id="eb118-141">In der Regel verwenden Anwendungen andere SDKs zum Rendering von Daten, z. b. das Microsoft Direct X SDK, oder die Multimedia-Funktionen des Microsoft Windows Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="eb118-141">Typically, applications will use other SDKs to render data, such as the Microsoft Direct X SDK, or the multimedia functions of the Microsoft Windows Platform SDK.</span></span>

<span data-ttu-id="eb118-142">Diese Schritte werden in der Beispielanwendung wmsynkreader veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="eb118-142">These steps are illustrated in the WMSyncReader sample application.</span></span> <span data-ttu-id="eb118-143">Weitere Informationen finden Sie unter [Beispielanwendungen](sample-applications.md).</span><span class="sxs-lookup"><span data-stu-id="eb118-143">For more information, see [Sample Applications](sample-applications.md).</span></span>

<span data-ttu-id="eb118-144">Der synchrone Reader unterstützt auch erweiterte Funktionen.</span><span class="sxs-lookup"><span data-stu-id="eb118-144">The synchronous reader also supports more advanced functionality.</span></span> <span data-ttu-id="eb118-145">Der synchrone Reader ermöglicht Ihnen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="eb118-145">The synchronous reader enables you to do the following:</span></span>

-   <span data-ttu-id="eb118-146">Geben Sie einen Bereich von Stichproben an, die nach Zeit oder nach Frame Nummer abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eb118-146">Specify a range of samples to retrieve by time or by frame number.</span></span>
-   <span data-ttu-id="eb118-147">Steuern der Streamauswahl für sich gegenseitig ausschließende Streams.</span><span class="sxs-lookup"><span data-stu-id="eb118-147">Control stream selection for mutually exclusive streams.</span></span>
-   <span data-ttu-id="eb118-148">Öffnen Sie eine Datei mit der Standard-COM-Schnittstelle **IStream**.</span><span class="sxs-lookup"><span data-stu-id="eb118-148">Open a file using the standard COM interface, **IStream**.</span></span>
-   <span data-ttu-id="eb118-149">Liest Profildaten aus dem Dateiheader.</span><span class="sxs-lookup"><span data-stu-id="eb118-149">Read profile data from the file header.</span></span>
-   <span data-ttu-id="eb118-150">Lesen von Metadaten aus dem Dateiheader.</span><span class="sxs-lookup"><span data-stu-id="eb118-150">Read metadata from the file header.</span></span>
-   <span data-ttu-id="eb118-151">Wechsel zwischen Stream-und Ausgabe Beispielen während der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="eb118-151">Switch between stream and output samples during playback.</span></span>
-   <span data-ttu-id="eb118-152">Zwischen komprimierten und unkomprimierten streambeispielen während der Wiedergabe wechseln.</span><span class="sxs-lookup"><span data-stu-id="eb118-152">Switch between compressed and uncompressed stream samples during playback.</span></span>

<span data-ttu-id="eb118-153">In den folgenden Abschnitten wird die Verwendung des synchronen Reader-Objekts ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="eb118-153">The following sections describe the use of the synchronous reader object in detail.</span></span>

-   [<span data-ttu-id="eb118-154">So erstellen Sie einen synchronen Reader und öffnen eine Datei</span><span class="sxs-lookup"><span data-stu-id="eb118-154">To Create a Synchronous Reader and Open a File</span></span>](to-create-a-synchronous-reader-and-open-a-file.md)
-   [<span data-ttu-id="eb118-155">So suchen Sie nach streamnummern und Ausgabe Nummern</span><span class="sxs-lookup"><span data-stu-id="eb118-155">To Find Stream Numbers and Output Numbers</span></span>](to-find-stream-numbers-and-output-numbers.md)
-   [<span data-ttu-id="eb118-156">So rufen Sie Medien Beispiele mit dem synchronen Reader ab</span><span class="sxs-lookup"><span data-stu-id="eb118-156">To Retrieve Media Samples with the Synchronous Reader</span></span>](to-retrieve-media-samples-with-the-synchronous-reader.md)
-   [<span data-ttu-id="eb118-157">So suchen Sie nach Zeit mithilfe des synchronen Readers</span><span class="sxs-lookup"><span data-stu-id="eb118-157">To Seek By Time Using the Synchronous Reader</span></span>](to-seek-by-time-using-the-synchronous-reader.md)
-   [<span data-ttu-id="eb118-158">So suchen Sie nach Frame Nummer mithilfe des synchronen Readers</span><span class="sxs-lookup"><span data-stu-id="eb118-158">To Seek By Frame Number Using the Synchronous Reader</span></span>](to-seek-by-frame-number-using-the-synchronous-reader.md)
-   [<span data-ttu-id="eb118-159">So suchen Sie nach SMPTE-Zeit Code mithilfe des synchronen Readers</span><span class="sxs-lookup"><span data-stu-id="eb118-159">To Seek By SMPTE Time Code Using the Synchronous Reader</span></span>](to-seek-by-smpte-time-code-using-the-synchronous-reader.md)
-   [<span data-ttu-id="eb118-160">So rufen Sie streambeispiele mit dem synchronen Reader ab</span><span class="sxs-lookup"><span data-stu-id="eb118-160">To Retrieve Stream Samples with the Synchronous Reader</span></span>](to-retrieve-stream-samples-with-the-synchronous-reader.md)
-   [<span data-ttu-id="eb118-161">So rufen Sie komprimierte Beispiele mit dem synchronen Reader ab</span><span class="sxs-lookup"><span data-stu-id="eb118-161">To Retrieve Compressed Samples with the Synchronous Reader</span></span>](to-retrieve-compressed-samples-with-the-synchronous-reader.md)

<span data-ttu-id="eb118-162">**Beispiel Code**</span><span class="sxs-lookup"><span data-stu-id="eb118-162">**Example Code**</span></span>

<span data-ttu-id="eb118-163">Der folgende Beispielcode zeigt, wie Sie mit dem synchronen Reader Beispiele aus einer ASF-Datei lesen.</span><span class="sxs-lookup"><span data-stu-id="eb118-163">The following example code shows how to read samples from an ASF file using the synchronous reader.</span></span> <span data-ttu-id="eb118-164">Er gibt nach Frame Nummer einen Bereich von zu über liegende Stichproben an.</span><span class="sxs-lookup"><span data-stu-id="eb118-164">It specifies by frame number a range of samples to deliver.</span></span>


```C++
IWMSyncReader* pSyncReader = NULL;
INSSBuffer*    pMyBuffer   = NULL;

QWORD cnsSampleTime = 0;
QWORD cnsSampleDuration = 0;
DWORD dwFlags = 0;
DWORD dwOutputNumber;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a synchronous reader.
hr = WMCreateSyncReader(NULL, WMT_RIGHT_PLAYBACK, &pSyncReader);

// Open an ASF file.
hr = pSyncReader->Open(L"c:\\somefile.wmv");

// TODO: Identify the properties for each output. This works 
// exactly as it does with the asynchronous reader.

// Specify a playback range from frame number 100 of the video 
// stream to the end of the file. Assume that the video stream 
// is stream number 2.
hr = pSyncReader->SetRangeByFrame(2, 100, 0);

// Loop through all the samples in the specified range.
do
{
   // Get the next sample, regardless of its stream number.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

pSyncReader->Release();
pSyncReader = NULL;

```



## <a name="related-topics"></a><span data-ttu-id="eb118-165">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eb118-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb118-166">**Iwmsynkreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="eb118-166">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="eb118-167">**Lesen von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="eb118-167">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> <dt>

[<span data-ttu-id="eb118-168">**Synchrones Reader-Objekt**</span><span class="sxs-lookup"><span data-stu-id="eb118-168">**Synchronous Reader Object**</span></span>](synchronous-reader-object.md)
</dt> </dl>

 

 




