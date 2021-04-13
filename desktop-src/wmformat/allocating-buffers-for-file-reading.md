---
title: Puffer für Datei Lesevorgänge werden zugewiesen.
description: Puffer für Datei Lesevorgänge werden zugewiesen.
ms.assetid: da66ef5b-ec92-445c-90ba-5ee89e0def36
keywords:
- Windows Media-Format-SDK, Lesen von ASF-Dateien
- Advanced Systems Format (ASF), Lesen von Dateien
- ASF (Advanced Systems Format), Lesen von Dateien
- Windows Media-Format-SDK, Zuordnen von Puffern
- Advanced Systems Format (ASF), Zuordnen von Puffern
- ASF (Advanced Systems Format), Zuordnen von Puffern
- Advanced Systems Format (ASF), Puffer Zuordnung
- ASF (Advanced Systems Format), Puffer Zuordnung
- Puffer Zuordnung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecdf9ba0a333bbe25c94ec087911237b68f38f74
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104389832"
---
# <a name="allocating-buffers-for-file-reading"></a><span data-ttu-id="cd273-112">Puffer für Datei Lesevorgänge werden zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="cd273-112">Allocating Buffers for File Reading</span></span>

<span data-ttu-id="cd273-113">Im grundlegendsten Datei Lese Szenario werden die Puffer, die zum Übermitteln von Beispielen verwendet werden, vom Lese Objekt (dem Reader-Objekt oder dem synchronen Reader-Objekt) zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cd273-113">In the most basic file-reading scenario, the buffers used to deliver samples are allocated by the reading object (the reader object or the synchronous reader object).</span></span> <span data-ttu-id="cd273-114">Sie können Puffer jedoch selbst zuweisen.</span><span class="sxs-lookup"><span data-stu-id="cd273-114">You can, however, allocate buffers yourself.</span></span> <span data-ttu-id="cd273-115">Weitere Informationen zu den Vorteilen der Zuordnung eigener Puffer finden Sie unter vom [Benutzer zugewiesene Beispiel Unterstützung](user-allocated-sample-support.md).</span><span class="sxs-lookup"><span data-stu-id="cd273-115">For more information about the benefits of allocating your own buffers, see [User Allocated Sample Support](user-allocated-sample-support.md).</span></span>

<span data-ttu-id="cd273-116">Führen Sie die folgenden Schritte aus, um Ihre eigenen Puffer zum Lesen von Dateien zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cd273-116">To use your own buffers for file reading, perform the following steps.</span></span>

1.  <span data-ttu-id="cd273-117">Implementieren Sie einen Rückruf oder Rückrufe, die der Reader aufrufen soll, wenn er einen Puffer benötigt.</span><span class="sxs-lookup"><span data-stu-id="cd273-117">Implement a callback or callbacks for the reader to call when it needs a buffer.</span></span> <span data-ttu-id="cd273-118">Wenn Sie Ausgabe Beispiele lesen, verwenden Sie [**iwmreaderindecatorex:: depcateforoutputex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex).</span><span class="sxs-lookup"><span data-stu-id="cd273-118">If you are reading output samples, use [**IWMReaderAllocatorEx::AllocateForOutputEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforoutputex).</span></span> <span data-ttu-id="cd273-119">Wenn Sie streambeispiele lesen, verwenden Sie " [**iwmreaderdepcatorex:: depcateforstreamex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex)".</span><span class="sxs-lookup"><span data-stu-id="cd273-119">If you are reading stream samples, use [**IWMReaderAllocatorEx::AllocateForStreamEx**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderallocatorex-allocateforstreamex).</span></span> <span data-ttu-id="cd273-120">Fügen Sie die Logik zum Verwalten von Puffern ein, die für Ihre Anwendung geeignet</span><span class="sxs-lookup"><span data-stu-id="cd273-120">Include whatever logic for managing buffers that suits your application.</span></span>
2.  <span data-ttu-id="cd273-121">Weisen Sie einen Pufferpool zu, den Sie für das Lesen von Dateien verwenden werden.</span><span class="sxs-lookup"><span data-stu-id="cd273-121">Allocate a pool of buffers that you will use for file reading.</span></span>
    -   <span data-ttu-id="cd273-122">Suchen Sie die Größe, die für die Puffer erforderlich ist, indem Sie für jede Ausgabe und/oder jeden Stream, für die der Puffer verwendet wird, [**iwmreaderadvanced:: getmaxoutputsamplesize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) oder [**iwmreaderadvanced:: getmaxstreamsamplesize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cd273-122">Find the size required for your buffers by calling [**IWMReaderAdvanced::GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxoutputsamplesize) or [**IWMReaderAdvanced::GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getmaxstreamsamplesize) for each output and/or stream for which the buffer is used.</span></span> <span data-ttu-id="cd273-123">Wenn Sie den synchronen Reader verwenden, verwenden Sie stattdessen [**iwmsynkreader:: getmaxoutputsamplesize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) oder [**iwmsynkreader:: getmaxstreamsamplesize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) .</span><span class="sxs-lookup"><span data-stu-id="cd273-123">If using the synchronous reader, use [**IWMSyncReader::GetMaxOutputSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxoutputsamplesize) or [**IWMSyncReader::GetMaxStreamSampleSize**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getmaxstreamsamplesize) instead.</span></span>
    -   <span data-ttu-id="cd273-124">Erstellen Sie jeden Puffer für den Pool.</span><span class="sxs-lookup"><span data-stu-id="cd273-124">Create each buffer for the pool.</span></span>
3.  <span data-ttu-id="cd273-125">Einrichten des Readers oder des synchronen Readers zum Lesen.</span><span class="sxs-lookup"><span data-stu-id="cd273-125">Set up the reader or synchronous reader for reading.</span></span> <span data-ttu-id="cd273-126">Weitere Informationen finden Sie unter [Lesen von Dateien mit dem asynchronen Reader](reading-files-with-the-asynchronous-reader.md) oder [Lesen von Dateien mit dem synchronen Reader](reading-files-with-the-synchronous-reader.md).</span><span class="sxs-lookup"><span data-stu-id="cd273-126">For more information see [Reading Files with the Asynchronous Reader](reading-files-with-the-asynchronous-reader.md) or [Reading Files with the Synchronous Reader](reading-files-with-the-synchronous-reader.md).</span></span>
4.  <span data-ttu-id="cd273-127">Bevor Sie mit dem Schreiben beginnen, nennen Sie [**iwmreaderadvanced:: setallocateforoutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) oder [**iwmreaderadvanced:: setallocateforstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) für jede Ausgabe und jeden Datenstrom, für den Sie Puffer mithilfe des Reader-Objekts zuordnen.</span><span class="sxs-lookup"><span data-stu-id="cd273-127">Before beginning writing, call [**IWMReaderAdvanced::SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforoutput) or [**IWMReaderAdvanced::SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setallocateforstream) for each output and stream for which you are allocating buffers using the reader object.</span></span> <span data-ttu-id="cd273-128">Für den synchronen Reader müssen Sie stattdessen [**IWMSyncReader2:: Log-locateforoutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) bzw. [**IWMSyncReader2:: abslocateforstream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) abrufen.</span><span class="sxs-lookup"><span data-stu-id="cd273-128">For the synchronous reader, call [**IWMSyncReader2::SetAllocateForOutput**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforoutput) or [**IWMSyncReader2::SetAllocateForStream**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader2-setallocateforstream) instead.</span></span>
5.  <span data-ttu-id="cd273-129">Beginnen Sie mit dem Lesen der Datei.</span><span class="sxs-lookup"><span data-stu-id="cd273-129">Begin reading the file.</span></span>

<span data-ttu-id="cd273-130">Das Lese Objekt ruft den entsprechenden zuordnerrückruf auf und ruft Beispiele von Ihrer Anwendung ab.</span><span class="sxs-lookup"><span data-stu-id="cd273-130">The reading object will make calls to the appropriate allocator callback and get samples from your application.</span></span> <span data-ttu-id="cd273-131">Ihre Puffer Verwaltungs Logik muss eine Möglichkeit enthalten, um zu signalisieren, dass ein Puffer frei verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="cd273-131">Your buffer management logic must include a way to signal that a buffer is free to be used again.</span></span> <span data-ttu-id="cd273-132">In der Regel wird ein Puffer wieder im Pool abgelegt, wenn sein Inhalt gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="cd273-132">Typically, a buffer is put back into the pool when its contents are rendered.</span></span> <span data-ttu-id="cd273-133">Abhängig von Ihrer Anwendung benötigen Sie möglicherweise nur wenige Puffer im Pool oder viele.</span><span class="sxs-lookup"><span data-stu-id="cd273-133">Depending upon your application, you may need just a few buffers in the pool or many.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd273-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cd273-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd273-135">**Lesen von ASF-Dateien**</span><span class="sxs-lookup"><span data-stu-id="cd273-135">**Reading ASF Files**</span></span>](reading-asf-files.md)
</dt> </dl>

 

 




