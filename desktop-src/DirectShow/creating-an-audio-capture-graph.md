---
description: Erstellen eines audioerfassungs Diagramms
ms.assetid: 2302bb40-a5db-473a-afeb-71905ac41f47
title: Erstellen eines audioerfassungs Diagramms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bd3c731a7dc498fcb7180bc56ae6a7f94dbec6d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346419"
---
# <a name="creating-an-audio-capture-graph"></a><span data-ttu-id="7a1e7-103">Erstellen eines audioerfassungs Diagramms</span><span class="sxs-lookup"><span data-stu-id="7a1e7-103">Creating an Audio Capture Graph</span></span>

<span data-ttu-id="7a1e7-104">Der erste Schritt für eine audioerfassungs Anwendung ist die Erstellung eines Filter Diagramms.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-104">The first step for an audio capture application is to build a filter graph.</span></span> <span data-ttu-id="7a1e7-105">Die Konfiguration des Diagramms hängt von dem Typ der Datei ab, die Sie erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-105">The configuration of the graph depends on the type of file that you want to create.</span></span>

-   <span data-ttu-id="7a1e7-106">Reine Audiodatei: audioerfassungs Filter nach [AVI MUX](avi-mux-filter.md) -Filter und AVI MUX in [File Writer](file-writer-filter.md) Filter.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-106">Audio-only AVI file: Audio Capture Filter to [AVI Mux](avi-mux-filter.md) filter, and AVI Mux to [File Writer](file-writer-filter.md) filter.</span></span>
-   <span data-ttu-id="7a1e7-107">WAV-Datei: audioerfassungs Filter für [wavdest Filter Sample](wavdest-filter-sample.md) to File Writer Filter</span><span class="sxs-lookup"><span data-stu-id="7a1e7-107">WAV file: Audio Capture Filter to [WavDest Filter Sample](wavdest-filter-sample.md) to File Writer Filter</span></span>
-   <span data-ttu-id="7a1e7-108">Windows Media Audio Datei (. WMA): audioerfassungs Filter für den [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-108">Windows Media Audio (.wma) file: Audio Capture Filter to [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span>

<span data-ttu-id="7a1e7-109">Der wavdest-Filter wird als SDK-Beispiel bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-109">The WavDest filter is provided as an SDK sample.</span></span> <span data-ttu-id="7a1e7-110">Um es zu verwenden, müssen Sie den Filter erstellen und registrieren.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-110">To use it, you must build and register the filter.</span></span>

<span data-ttu-id="7a1e7-111">Wenn Sie den ASF-Writer-Filter verwenden möchten, müssen Sie das Windows Media SDK installieren und einen Software Schlüssel abrufen, um den Filter zu entsperren.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-111">To use the ASF Writer filter, you must install the Windows Media SDK and obtain a software key to unlock the filter.</span></span> <span data-ttu-id="7a1e7-112">Weitere Informationen finden Sie unter [Verwenden von Windows Media in DirectShow](using-windows-media-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e7-112">For more information, see [Using Windows Media in DirectShow](using-windows-media-in-directshow.md).</span></span>

<span data-ttu-id="7a1e7-113">Sie können das Filter Diagramm mit dem [Erfassungs Diagramm](capture-graph-builder.md) -Generator-Objekt erstellen, oder Sie können das Diagramm manuell erstellen. Das heißt, dass die Anwendung jeden Filterprogramm gesteuert hinzufügen und verbinden kann.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-113">You can build the filter graph using the [Capture Graph Builder](capture-graph-builder.md) object, or you can build the graph "manually"; that is, have the application programmatically add and connect each filter.</span></span> <span data-ttu-id="7a1e7-114">In diesem Artikel wird die manuelle Vorgehensweise beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-114">This article describes the manual approach.</span></span> <span data-ttu-id="7a1e7-115">Weitere Informationen zur Verwendung des Erfassungs Diagramm-Generators finden Sie unter [Video Aufzeichnung](video-capture.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e7-115">For more information about using the Capture Graph Builder, see [Video Capture](video-capture.md).</span></span> <span data-ttu-id="7a1e7-116">Ein Großteil der Informationen in diesem Artikel gilt für reine audiodiagramme.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-116">Much of the information in that article applies to audio-only graphs.</span></span>

<span data-ttu-id="7a1e7-117">Hinzufügen des audioerfassungs Geräts</span><span class="sxs-lookup"><span data-stu-id="7a1e7-117">Adding the Audio Capture Device</span></span>

<span data-ttu-id="7a1e7-118">Da der audioerfassungs Filter mit einem bestimmten Hardware Gerät kommuniziert, können Sie nicht einfach **cokreateinstance** aufrufen, um den Filter zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-118">Because the Audio Capture Filter communicates with a specific hardware device, you cannot simply call **CoCreateInstance** to create the filter.</span></span> <span data-ttu-id="7a1e7-119">Verwenden Sie stattdessen den [Enumerator "System Geräte](system-device-enumerator.md) ", um alle Geräte in der Kategorie "audioerfassungs Quellen" aufzulisten, die durch den Klassen Bezeichner CLSID \_ audioinputdevicecategory gekennzeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-119">Instead, use the [System Device Enumerator](system-device-enumerator.md) to enumerate all of the devices in the "Audio Capture Sources" category, which is identified by the class identifier CLSID\_AudioInputDeviceCategory.</span></span>

<span data-ttu-id="7a1e7-120">Der Enumerator für System Geräte gibt eine Liste der Moniker für die Geräte zurück. der Anzeige Name jedes Monikers entspricht dem Namen des Geräts.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-120">The System Device Enumerator returns a list of monikers for the devices; each moniker's friendly name corresponds to the name of the device.</span></span> <span data-ttu-id="7a1e7-121">Wählen Sie einen der zurückgegebenen Moniker aus, und verwenden Sie ihn zum Erstellen einer Instanz des audioerfassungs Filters für dieses Gerät.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-121">Choose one of the returned monikers and use it to create an instance of the Audio Capture Filter for that device.</span></span> <span data-ttu-id="7a1e7-122">Fügen Sie den Filter dem Filter Diagramm hinzu.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-122">Add the filter to the filter graph.</span></span> <span data-ttu-id="7a1e7-123">Das bevorzugte audioaufzeichnungs Gerät des Benutzers wird zuerst in der monikerliste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-123">The user's preferred audio recording device appears first in the moniker list.</span></span> <span data-ttu-id="7a1e7-124">(Der Benutzer wählt ein bevorzugtes Gerät aus, indem er in der Systemsteuerung auf Sounds und Multimedia klickt.)</span><span class="sxs-lookup"><span data-stu-id="7a1e7-124">(The user selects a preferred device by clicking Sounds and Multimedia in Control Panel.)</span></span>

<span data-ttu-id="7a1e7-125">Weitere Informationen finden Sie unter [using the System Device Enumerator](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e7-125">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="7a1e7-126">Zum Angeben der Eingabe, die von erfasst werden soll, rufen Sie die [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) -Schnittstelle aus dem audioerfassungs Filter ab und rufen die **Put \_ enable** -Methode auf, um die Eingabe anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-126">To specify which input to capture from, obtain the [**IAMAudioInputMixer**](/windows/desktop/api/Strmif/nn-strmif-iamaudioinputmixer) interface from the Audio Capture filter and call the **put\_Enable** method to specify the input.</span></span> <span data-ttu-id="7a1e7-127">Eine Einschränkung dieser Methode besteht jedoch darin, dass unterschiedliche Hardware Geräte verschiedene Zeichen folgen verwenden können, um Ihre Eingaben zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-127">One limitation of this method, however, is that different hardware devices may use different strings to identify their inputs.</span></span> <span data-ttu-id="7a1e7-128">Beispielsweise kann eine Karte "Mikrofon" verwenden, um die Mikrofon Eingabe zu identifizieren, und eine andere Karte kann "MIC" verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-128">For example, one card may use "Microphone" to identify the microphone input and another card may use "Mic".</span></span> <span data-ttu-id="7a1e7-129">Um den Zeichen folgen Bezeichner für eine bestimmte Eingabe zu ermitteln, verwenden Sie die Windows Multimedia Functions [**WaveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixeropen**](/previous-versions//dd757308(v=vs.85))und [**mixergetlineinfo**](/previous-versions//dd757303(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7a1e7-129">To determine the string identifier for a given input, use the Windows Multimedia functions [**waveOutOpen**](/previous-versions//dd743866(v=vs.85)), [**mixerOpen**](/previous-versions//dd757308(v=vs.85)), and [**mixerGetLineInfo**](/previous-versions//dd757303(v=vs.85)).</span></span> <span data-ttu-id="7a1e7-130">Weitere Informationen finden Sie im MSDN-Thema [Mixer Geräte Abfragen](/windows/desktop/Multimedia/mixer-device-queries) .</span><span class="sxs-lookup"><span data-stu-id="7a1e7-130">See the MSDN topic [Mixer Device Queries](/windows/desktop/Multimedia/mixer-device-queries) for more information.</span></span>

<span data-ttu-id="7a1e7-131">Hinzufügen von Multiplexer und dateiwriter</span><span class="sxs-lookup"><span data-stu-id="7a1e7-131">Adding the Multiplexer and the File Writer</span></span>

<span data-ttu-id="7a1e7-132">Ein audioerfassungs Diagramm muss einen Multiplexer und einen dateiwriter enthalten.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-132">An audio capture graph must contain a multiplexer and a file writer.</span></span>

<span data-ttu-id="7a1e7-133">Ein *Multiplexer* ist ein Filter, der einen oder mehrere Streams in einem einzigen Stream mit einem bestimmten Format kombiniert.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-133">A *multiplexer* is a filter that combines one or more streams into a single stream with a particular format.</span></span> <span data-ttu-id="7a1e7-134">Der AVI MUX-Filter kombiniert z. b. Audio-und Videostreams in einem verschachtelten AVI-Stream.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-134">For example, the AVI Mux filter combines audio and video streams into an interleaved AVI stream.</span></span> <span data-ttu-id="7a1e7-135">Für die Audioerfassung gibt es in der Regel nur einen einzigen Audiostream, aber die Audiodaten müssen immer noch in ein Format gepackt werden, das auf dem Datenträger gespeichert werden kann. hierfür ist ein Multiplexer erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-135">For audio capture, there is typically only a single audio stream, but the audio data must still be packaged into a format that can be saved to disk, which requires a multiplexer.</span></span> <span data-ttu-id="7a1e7-136">Die Auswahl von Multiplexer ist vom Zielformat abhängig:</span><span class="sxs-lookup"><span data-stu-id="7a1e7-136">The choice of multiplexer depends on the target format:</span></span>

-   <span data-ttu-id="7a1e7-137">AVI: AVI Multiplexer</span><span class="sxs-lookup"><span data-stu-id="7a1e7-137">AVI: AVI Multiplexer</span></span>
-   <span data-ttu-id="7a1e7-138">WAV: wavdest</span><span class="sxs-lookup"><span data-stu-id="7a1e7-138">WAV: WavDest</span></span>
-   <span data-ttu-id="7a1e7-139">WMA: ASF-Writer</span><span class="sxs-lookup"><span data-stu-id="7a1e7-139">WMA: ASF Writer</span></span>

<span data-ttu-id="7a1e7-140">Ein *dateiwriter* ist ein Filter, der eingehende Daten in eine Datei schreibt.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-140">A *file writer* is a filter that writes incoming data to a file.</span></span> <span data-ttu-id="7a1e7-141">Verwenden Sie für AVI-oder WAV-Dateien den [dateiwriter-Filter](file-writer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="7a1e7-141">For AVI or WAV files, use the [File Writer Filter](file-writer-filter.md).</span></span> <span data-ttu-id="7a1e7-142">Bei WMA-Dateien fungiert der ASF-Writer sowohl als Multiplexer als auch als dateiwriter.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-142">For WMA files, the ASF Writer acts as both multiplexer and file writer.</span></span>

<span data-ttu-id="7a1e7-143">Nachdem Sie die Filter erstellt und dem Diagramm hinzugefügt haben, verbinden Sie die Ausgabe-PIN des audioerfassungs Filters mit der Eingabe-PIN des Multiplexers, und verbinden Sie die Ausgabe-PIN des Multiplexers mit der Eingabe-PIN des filterwriters (angenommen, dies sind separate Filter).</span><span class="sxs-lookup"><span data-stu-id="7a1e7-143">After you create the filters and add them to the graph, connect the Audio Capture Filter's output pin to the multiplexer's input pin, and connect the multiplexer's output pin to the filter writer's input pin (assuming these are separate filters).</span></span> <span data-ttu-id="7a1e7-144">Um den Dateinamen anzugeben, Fragen Sie den dateiwriter nach der [**ifilesinkfilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) -Schnittstelle ab, und nennen Sie die [**ifilesinkfilter:: setFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) -Methode.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-144">To specify the file name, query the file writer for the [**IFileSinkFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter) interface and call the [**IFileSinkFilter::SetFileName**](/windows/desktop/api/Strmif/nf-strmif-ifilesinkfilter-setfilename) method.</span></span>

### <a name="example-code"></a><span data-ttu-id="7a1e7-145">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="7a1e7-145">Example Code</span></span>

<span data-ttu-id="7a1e7-146">Im folgenden Beispiel wird gezeigt, wie ein audioerfassungs Diagramm mit dem wavdest-Filter erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-146">The following example shows how to build an audio capture graph using the WavDest filter.</span></span> <span data-ttu-id="7a1e7-147">Die gleichen Prinzipien gelten für die anderen Dateitypen.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-147">The same principles apply for the other file types.</span></span>


```C++
IBaseFilter *pSrc = NULL, *pWaveDest = NULL, *pWriter = NULL;
IFileSinkFilter *pSink= NULL;
IGraphBuilder *pGraph;

// Create the Filter Graph Manager.
hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER,
    IID_IGraphBuilder, (void**)&pGraph);

// This example omits error handling.

// Not shown: Use the System Device Enumerator to create the 
// audio capture filter.

// Add the audio capture filter to the filter graph. 
hr = pGraph->AddFilter(pSrc, L"Capture");

// Add the WavDest and the File Writer.
hr = AddFilterByCLSID(pGraph, CLSID_WavDest, L"WavDest", &pWaveDest);
hr = AddFilterByCLSID(pGraph, CLSID_FileWriter, L"File Writer", &pWriter);

// Set the file name.
hr = pWriter->QueryInterface(IID_IFileSinkFilter, (void**)&pSink);
hr = pSink->SetFileName(L"C:\\MyWavFile.wav", NULL);

// Connect the filters.
hr = ConnectFilters(pGraph, pSrc, pWaveDest);
hr = ConnectFilters(pGraph, pWaveDest, pWriter);

// Not shown: Release interface pointers.

```



<span data-ttu-id="7a1e7-148">In diesem Beispiel `AddFilterByCLSID` wird die unter [Hinzufügen eines Filters nach CLSID](add-a-filter-by-clsid.md)beschriebene Funktion und die `ConnectFilters` in Verbinden von [zwei Filtern](connect-two-filters.md)beschriebene Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-148">This example uses the `AddFilterByCLSID` function described in [Add a Filter by CLSID](add-a-filter-by-clsid.md), and the `ConnectFilters` function described in [Connect Two Filters](connect-two-filters.md).</span></span> <span data-ttu-id="7a1e7-149">Keines dieser APIs ist eine DirectShow-API.</span><span class="sxs-lookup"><span data-stu-id="7a1e7-149">Neither of these is a DirectShow API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7a1e7-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7a1e7-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a1e7-151">Audioerfassung</span><span class="sxs-lookup"><span data-stu-id="7a1e7-151">Audio Capture</span></span>](audio-capture.md)
</dt> </dl>

 

 
