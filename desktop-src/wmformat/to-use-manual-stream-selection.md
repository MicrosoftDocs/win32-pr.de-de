---
title: So verwenden Sie die manuelle Datenstrom Auswahl
description: So verwenden Sie die manuelle Datenstrom Auswahl
ms.assetid: 49ec283f-670a-4a0e-9477-c60a80919a1e
keywords:
- Advanced Systems Format (ASF), manuelle Datenstrom Auswahl
- ASF (Advanced Systems Format), manuelle Datenstrom Auswahl
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- Advanced Systems Format (ASF), Streamauswahl
- ASF (Advanced Systems Format), Streamauswahl
- Advanced Systems Format (ASF), gegenseitiger Ausschluss
- ASF (Advanced Systems Format), gegenseitiger Ausschluss
- asynchrone Leser, manuelle Datenstrom Auswahl
- asynchrone Leser, Streamauswahl
- Streams, manuelle Auswahl
- gegenseitiger Ausschluss, manuelle Datenstrom Auswahl
- Streams, asynchrone Leser
- gegenseitiger Ausschluss, asynchrone Leser
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a87c493bc8f41bc2a03ba15832ed402939adbeff
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106341914"
---
# <a name="to-use-manual-stream-selection"></a><span data-ttu-id="ee4d2-117">So verwenden Sie die manuelle Datenstrom Auswahl</span><span class="sxs-lookup"><span data-stu-id="ee4d2-117">To Use Manual Stream Selection</span></span>

<span data-ttu-id="ee4d2-118">Wenn Sie nicht komprimierte Beispiele mit dem Reader-Objekt bereitstellt, können Sie diese nur anhand der Ausgabe Nummer übermitteln.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-118">When delivering uncompressed samples with the reader object, you can deliver them only by output number.</span></span> <span data-ttu-id="ee4d2-119">Im Fall von sich gegenseitig ausschließenden Streams bedeutet dies, dass Sie nur Beispiele von einem Stream im gegenseitigen Ausschluss gleichzeitig empfangen können.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-119">In the case of mutually exclusive streams, this means that you can receive samples only from one stream in the mutual exclusion at a time.</span></span> <span data-ttu-id="ee4d2-120">Der Prozess der Auswahl des zu über liegende, sich gegenseitig ausschließenden Streams wird als Streamauswahl bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-120">The process of choosing which mutually exclusive stream to deliver is called stream selection.</span></span>

<span data-ttu-id="ee4d2-121">Bei einem gegenseitigen Bitrate-Ausschluss macht der Reader die Streamauswahl automatisch basierend auf den Bedingungen auf dem Host Computer bei der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-121">For bit-rate mutual exclusion, the reader makes stream selections automatically based on the conditions on the host machine at playback.</span></span> <span data-ttu-id="ee4d2-122">Bei anderen Typen von gegenseitigem Ausschluss liefert der Reader Beispiele aus dem Standardstream, es sei denn, Sie wählen selbst manuell einen anderen Stream aus.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-122">For other types of mutual exclusion, the reader will deliver samples from the default stream unless you manually select a different stream yourself.</span></span> <span data-ttu-id="ee4d2-123">Es können auch Instanzen vorhanden sein, wenn Sie einen Stream manuell aus einem Bitrate gegenseitigen Ausschluss auswählen möchten.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-123">There may also be instances when you want to select a stream manually from a bit-rate mutual exclusion.</span></span>

<span data-ttu-id="ee4d2-124">Die manuelle Datenstrom Auswahl ist für die gesamte Datei entweder ein-oder ausgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-124">Manual stream selection is either on or off for the entire file.</span></span> <span data-ttu-id="ee4d2-125">Wenn eine Datei einen Bitrate gegenseitigen Ausschluss und einen anderen gegenseitigen Ausschluss Typ enthält, müssen Sie die Bitrate basierten Streams manuell auswählen.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-125">If a file contains bit-rate mutual exclusion and some other mutual exclusion type, you must select the bit rate based streams manually.</span></span>

<span data-ttu-id="ee4d2-126">Führen Sie die folgenden Schritte aus, um einen sich gegenseitig ausschließenden Stream manuell auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-126">To select a mutually exclusive stream manually, you must perform the following steps.</span></span>

1.  <span data-ttu-id="ee4d2-127">Abrufen eines Zeigers auf die [**iwmreaderadvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) -Schnittstelle des Reader-Objekts durch Aufrufen von **iwmreader:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-127">Retrieve a pointer to the [**IWMReaderAdvanced**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced) interface of the reader object by calling **IWMReader::QueryInterface**.</span></span>
2.  <span data-ttu-id="ee4d2-128">Aktivieren Sie die manuelle Datenstrom Auswahl durch Aufrufen von [**iwmreaderadvanced:: setmanualstreamselection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).</span><span class="sxs-lookup"><span data-stu-id="ee4d2-128">Enable manual stream selection by calling [**IWMReaderAdvanced::SetManualStreamSelection**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setmanualstreamselection).</span></span>
3.  <span data-ttu-id="ee4d2-129">Um herauszufinden, ob ein bestimmter Stream ausgewählt ist, nennen Sie [**iwmreaderadvanced:: getstreamselected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected).</span><span class="sxs-lookup"><span data-stu-id="ee4d2-129">To find out if a particular stream is selected, call [**IWMReaderAdvanced::GetStreamSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstreamselected).</span></span> <span data-ttu-id="ee4d2-130">Sie müssen einen Zeiger an eine Variable des Enumerationstyps der [**WMT-Daten \_ Strom \_ Auswahl**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) übergeben.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-130">You must pass a pointer to a variable of the [**WMT\_STREAM\_SELECTION**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_stream_selection) enumeration type.</span></span> <span data-ttu-id="ee4d2-131">Wenn der-Rückruf zurückgegeben wird, beschreibt der Wert in der Variablen den aktuellen Auswahltyp des Streams.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-131">When the call returns, the value in the variable will describe the current selection type of the stream.</span></span>
4.  <span data-ttu-id="ee4d2-132">Um einen Stream auszuwählen, nennen Sie [**iwmreaderadvanced:: setstreamssgewählt**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected).</span><span class="sxs-lookup"><span data-stu-id="ee4d2-132">To select a stream, call [**IWMReaderAdvanced::SetStreamsSelected**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setstreamsselected).</span></span> <span data-ttu-id="ee4d2-133">Diese Methode ermöglicht es Ihnen, mehrere Streams gleichzeitig für den synchronisierten Streamwechsel anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ee4d2-133">This method enables you to specify multiple streams at the same time for synchronized stream switching.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee4d2-134">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee4d2-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee4d2-135">**Lesen von Dateien mit dem asynchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="ee4d2-135">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> </dl>

 

 




