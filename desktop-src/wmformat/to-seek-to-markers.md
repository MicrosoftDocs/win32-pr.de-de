---
title: So suchen Sie Marker
description: So suchen Sie Marker
ms.assetid: 2d5efebf-dcbd-4fb8-933e-cc6d3a99adf8
keywords:
- Advanced Systems Format (ASF), suchen nach Markern
- ASF (Advanced Systems Format), suchen nach Markern
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- Advanced Systems Format (ASF), Marker
- ASF (Advanced Systems Format), Marker
- asynchrone Leser, suchen nach Markern
- asynchrone Leser, Marker
- Marker, suchen
- Marker, asynchrone Leser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a16cb4fef99a5c735a12f03f8d2e962d6caf9c2a
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "106338652"
---
# <a name="to-seek-to-markers"></a><span data-ttu-id="804fb-113">So suchen Sie Marker</span><span class="sxs-lookup"><span data-stu-id="804fb-113">To Seek to Markers</span></span>

<span data-ttu-id="804fb-114">Ein Marker ist ein benannter Speicherort in einer ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="804fb-114">A marker is a named location in an ASF file.</span></span> <span data-ttu-id="804fb-115">Sie können die Wiedergabe nur über den Speicherort eines Markers starten, indem Sie den asynchronen Reader verwenden.</span><span class="sxs-lookup"><span data-stu-id="804fb-115">You can only start playback from the location of a marker by using the asynchronous reader.</span></span> <span data-ttu-id="804fb-116">Sie können die Wiedergabe an einem Marker starten, indem Sie die folgenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="804fb-116">You can begin playback at a marker by following these steps.</span></span>

1.  <span data-ttu-id="804fb-117">Rufen Sie **iwmreader:: QueryInterface** auf, um einen Zeiger auf die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="804fb-117">Call **IWMReader::QueryInterface** to obtain a pointer to the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) interface.</span></span>
2.  <span data-ttu-id="804fb-118">Rufen Sie die Gesamtanzahl der Marker in der Datei ab, indem Sie [**iwmheaderinfo:: getmarkercount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="804fb-118">Retrieve the total number of markers in the file by calling [**IWMHeaderInfo::GetMarkerCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarkercount).</span></span>
3.  <span data-ttu-id="804fb-119">Durchlaufen Sie die Marker mithilfe der in Schritt 2 abgerufenen markeranzahl.</span><span class="sxs-lookup"><span data-stu-id="804fb-119">Loop through the markers, using the marker count retrieved in step 2.</span></span> <span data-ttu-id="804fb-120">Rufen Sie den Namen und die Uhrzeit der einzelnen Marker durch Aufrufen von [**iwmheaderinfo:: getmarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) für jeden Marker ab.</span><span class="sxs-lookup"><span data-stu-id="804fb-120">Retrieve the name and time of each marker by calling [**IWMHeaderInfo::GetMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getmarker) for each.</span></span> <span data-ttu-id="804fb-121">Speichern Sie den Index des gewünschten Markers.</span><span class="sxs-lookup"><span data-stu-id="804fb-121">Save the index of the desired marker.</span></span>
4.  <span data-ttu-id="804fb-122">Rufen Sie **iwmreader:: QueryInterface** auf, um einen Zeiger auf die [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="804fb-122">Call **IWMReader::QueryInterface** to obtain a pointer to the [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) interface.</span></span>
5.  <span data-ttu-id="804fb-123">Geben Sie den Marker an, an dem die Wiedergabe durch Aufrufen von [**IWMReaderAdvanced2:: startatmarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker)gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="804fb-123">Specify the marker at which to start playback by calling [**IWMReaderAdvanced2::StartAtMarker**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-startatmarker).</span></span> <span data-ttu-id="804fb-124">Sie müssen den Index des gewünschten Markers übergeben, den Sie in Schritt 3 gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="804fb-124">You must pass the index of the desired marker, which you saved in step 3.</span></span>
6.  <span data-ttu-id="804fb-125">Behandeln Sie die Beispiele wie in der Implementierung der [**iwmreadercallback:: onsample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) -Methode.</span><span class="sxs-lookup"><span data-stu-id="804fb-125">Handle the samples as you normally would in your implementation of the [**IWMReaderCallback::OnSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreadercallback-onsample) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="804fb-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="804fb-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="804fb-127">**Marker**</span><span class="sxs-lookup"><span data-stu-id="804fb-127">**Markers**</span></span>](markers.md)
</dt> <dt>

[<span data-ttu-id="804fb-128">**Lesen von Dateien mit dem asynchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="804fb-128">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="804fb-129">**Arbeiten mit Indizes**</span><span class="sxs-lookup"><span data-stu-id="804fb-129">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




