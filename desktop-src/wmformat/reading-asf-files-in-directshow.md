---
title: Lesen von ASF-Dateien in DirectShow (Windows Media Format 11 SDK)
description: Die Wiedergabe von ASF-Dateien wird vom WM ASF-Readerfilter verarbeitet. Erfahren Sie mehr über das Lesen von ASF-Dateien in DirectShow im Windows Media Format 11 SDK.
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- Windows Media Format SDK, DirectShow
- Windows Media Format SDK, Lesen von ASF-Dateien
- Windows Media Format SDK, WM ASF-Readerfilter
- Windows Media Format SDK, IMediaSeeking-Schnittstelle
- Advanced Systems Format (ASF),DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Lesen von Dateien
- ASF (Advanced Systems Format), Lesen von Dateien
- Advanced Systems Format (ASF), WM ASF-Readerfilter
- ASF (Advanced Systems Format), WM ASF-Readerfilter
- Advanced Systems Format (ASF), IMediaSeeking-Schnittstelle
- ASF (Advanced Systems Format), IMediaSeeking-Schnittstelle
- DirectShow,Lesen von ASF-Dateien
- Filter "DirectShow", "WM ASF Reader"
- DirectShow,IMediaSeeking-Schnittstelle
- WM ASF-Readerfilter
- IMediaSeeking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aaab64798011eb21edbe43f49438db99d0bae6b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404323"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="a5c72-121">Lesen von ASF-Dateien in DirectShow (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="a5c72-121">Reading ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="a5c72-122">Die Wiedergabe von ASF-Dateien wird vom [WM ASF-Readerfilter](wm-asf-reader-filter.md) verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="a5c72-122">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="a5c72-123">Wenn der WM ASF-Reader eine Datei liest, erstellt er automatisch einen Ausgabepin für jeden Stream, einschließlich Webstreams, Skriptbefehlsstreams und jeder anderen Art von beliebigem Stream.</span><span class="sxs-lookup"><span data-stu-id="a5c72-123">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including Web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="a5c72-124">Bei Dateien mit mehreren Bitraten werden Pins nur für die aktuell ausgewählten Streams erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5c72-124">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span>

<span data-ttu-id="a5c72-125">Der WM ASF-Reader unterstützt die DirectShow **IMediaSeeking-Schnittstelle,** mit der Anwendungen temporale Suchmöglichkeiten innerhalb der Datei ausführen können.</span><span class="sxs-lookup"><span data-stu-id="a5c72-125">The WM ASF Reader supports the DirectShow **IMediaSeeking** interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="a5c72-126">Die Wiedergabe mit anderen Geschwindigkeiten als 1.0 (wie in **IMediaSeeking::SetRate** angegeben) wird jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a5c72-126">However, playback at speeds other than 1.0 (as specified in **IMediaSeeking::SetRate**) is not supported.</span></span>

<span data-ttu-id="a5c72-127">Der Filter macht auch mehrere Windows Media Format SDK-Schnittstellen verfügbar, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="a5c72-127">The filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span>



| <span data-ttu-id="a5c72-128">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a5c72-128">Interface</span></span>                                        | <span data-ttu-id="a5c72-129">Verfügbar gemacht</span><span class="sxs-lookup"><span data-stu-id="a5c72-129">How exposed</span></span>                            | <span data-ttu-id="a5c72-130">Kommentare</span><span class="sxs-lookup"><span data-stu-id="a5c72-130">Comments</span></span>                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a5c72-131">**IWMDRMReader**</span><span class="sxs-lookup"><span data-stu-id="a5c72-131">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="a5c72-132">Über **IServiceProvider** für Filter</span><span class="sxs-lookup"><span data-stu-id="a5c72-132">Through **IServiceProvider** on filter</span></span> | <span data-ttu-id="a5c72-133">Wird für Anwendungen bereitgestellt, die Inhalte wieder geben müssen, die durch Digital Rights Management (DRM) geschützt sind.</span><span class="sxs-lookup"><span data-stu-id="a5c72-133">Provided for applications that need to play content protected by Digital Rights Management (DRM).</span></span> <span data-ttu-id="a5c72-134">Diese Schnittstelle kann auch verwendet werden, um andere Schnittstellen für das Readerobjekt direkt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a5c72-134">This interface can also be used to obtain other interfaces on the Reader Object directly.</span></span> |
| [<span data-ttu-id="a5c72-135">**IWMHeaderInfo**</span><span class="sxs-lookup"><span data-stu-id="a5c72-135">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="a5c72-136">**QueryInterface für** Filter</span><span class="sxs-lookup"><span data-stu-id="a5c72-136">**QueryInterface** on filter</span></span>           | <span data-ttu-id="a5c72-137">Wird bereitgestellt, damit Anwendungen Datei- und Inhaltsattribute sowie Marker- und Skriptinformationen und Metadaten lesen können.</span><span class="sxs-lookup"><span data-stu-id="a5c72-137">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>                                                                  |
| [<span data-ttu-id="a5c72-138">**IWMReaderAdvanced**</span><span class="sxs-lookup"><span data-stu-id="a5c72-138">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="a5c72-139">**QueryInterface für** Filter</span><span class="sxs-lookup"><span data-stu-id="a5c72-139">**QueryInterface** on filter</span></span>           | <span data-ttu-id="a5c72-140">Teilweise im Filter implementiert, sodass Anwendungen auf die Informationsmethoden im WM-Reader-Objekt zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="a5c72-140">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>                                                                      |
| [<span data-ttu-id="a5c72-141">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="a5c72-141">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="a5c72-142">**QueryInterface für** Filter</span><span class="sxs-lookup"><span data-stu-id="a5c72-142">**QueryInterface** on filter</span></span>           | <span data-ttu-id="a5c72-143">Teilweise im Filter implementiert, sodass Anwendungen auf die Informationsmethoden des Readerobjekts zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="a5c72-143">Partially implemented on the filter so that applications can access the informational methods on the Reader Object.</span></span>                                                                         |



 

<span data-ttu-id="a5c72-144">Der [WM ASF-Readerfilter](wm-asf-reader-filter.md) wurde erstmals in DirectShow 8.0 verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="a5c72-144">The [WM ASF Reader](wm-asf-reader-filter.md) filter was first made available in DirectShow 8.0.</span></span> <span data-ttu-id="a5c72-145">Die version of the filter that ships with DirectShow 8.1 and 9.0 supports version 7. *x* des Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="a5c72-145">The version of the filter that ships with DirectShow 8.1 and 9.0 supports version 7.*x* of the Windows Media Format SDK.</span></span> <span data-ttu-id="a5c72-146">Die neueste Version des Filters wird zusammen mit den anderen QASF-Komponenten im Windows Media Format 9 Series SDK und in späteren Versionen bereitgestellt und unterstützt es und ersetzt den Filter in DirectX 9.0.</span><span class="sxs-lookup"><span data-stu-id="a5c72-146">The most recent version of the filter, along with the other QASF components, ships with and supports the Windows Media Format 9 Series SDK, and later versions, and it supersedes the filter in DirectX 9.0.</span></span> <span data-ttu-id="a5c72-147">Wenn Sie das Windows Media Format SDK nach der Installation von DirectX 8 installieren. *x* oder 9. *x* SDK: Sie überschreiben die DirectX-Version qasf.dll Version der 9er Serie.</span><span class="sxs-lookup"><span data-stu-id="a5c72-147">If you install the Windows Media Format SDK after installing the DirectX 8.*x* or 9.*x* SDK, you will overwrite the DirectX version of qasf.dll with the 9 Series version.</span></span> <span data-ttu-id="a5c72-148">Dies sollte keine Probleme verursachen, außer möglicherweise in einem Szenario, in dem es zu einem anderen Verhalten in der DirectShow **IGraphBuilder::RenderFile-Methode** führt.</span><span class="sxs-lookup"><span data-stu-id="a5c72-148">This should not present any problems except possibly in one scenario where it will result in different behavior in the DirectShow **IGraphBuilder::RenderFile** method.</span></span> <span data-ttu-id="a5c72-149">Die SDK-Version des Windows Media Format 9 Series des WM ASF-Readers ist der Standardquellenfilter für die Erweiterungen ASF, WMV und WMA.</span><span class="sxs-lookup"><span data-stu-id="a5c72-149">The Windows Media Format 9 Series SDK version of the WM ASF Reader is the default source filter for the .asf, .wmv, and .wma file name extensions.</span></span> <span data-ttu-id="a5c72-150">Dies bedeutet, dass der WM ASF-Reader automatisch erstellt und dem Filterdiagramm durch den Filtergraph-Manager in Methoden wie **IGraphBuilder::RenderFile** oder **IGraphBuilder::AddSourceFilter** hinzugefügt wird, wenn eine Datei dieses Typs angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="a5c72-150">This means that the WM ASF Reader is automatically created and added to the filter graph by the Filter Graph Manager in methods such as **IGraphBuilder::RenderFile** or **IGraphBuilder::AddSourceFilter** when a file of this type is specified.</span></span> <span data-ttu-id="a5c72-151">In DirectX 9.0 und früher und Windows XP Service Pack 1 und früher verwendet die **RenderFile-Methode** den älteren Windows Media Source Filter.</span><span class="sxs-lookup"><span data-stu-id="a5c72-151">In DirectX 9.0 and earlier, and Windows XP Service Pack 1 and earlier, the **RenderFile** method uses the older Windows Media Source Filter.</span></span> <span data-ttu-id="a5c72-152">Dieses Verhalten wurde beibehalten, um die Abwärtskompatibilität mit Anwendungen sicherzustellen, die Windows Media Player 6.4 verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="a5c72-152">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="a5c72-153">Weitere Informationen zum älteren Windows Media Source-Filter finden Sie in der DirectShow SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="a5c72-153">For more information about the legacy Windows Media Source Filter, see the DirectShow SDK Documentation.</span></span>

<span data-ttu-id="a5c72-154">Um eine ASF-Datei mit Windows Media-basiertem Inhalt mithilfe des WM ASF-Readers wiederderherzustellen, müssen Sie in den drei Hauptschritten eine Instanz des Filterdiagramm-Managers erstellen, **IGraphBuilder::RenderFile** aufrufen, um das Diagramm zu erstellen, und dann **IMediaControl::Run** aufrufen, um die Datei wieder zu spielen.</span><span class="sxs-lookup"><span data-stu-id="a5c72-154">To play an ASF file with Windows Media–based content using the WM ASF Reader, the three primary steps are to create an instance of the Filter Graph Manager, call **IGraphBuilder::RenderFile** to create the graph, and then call **IMediaControl::Run** to play the file.</span></span> <span data-ttu-id="a5c72-155">Das folgende Codebeispiel ist ein vollständiges Programm, das eine ASF-Datei mit DirectShow wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="a5c72-155">The following code example is a complete program that plays an ASF file using DirectShow.</span></span> <span data-ttu-id="a5c72-156">Um dieses Beispiel ausführen zu können, muss das DirectX SDK installiert sein, und Ihre Buildumgebung muss gemäß den Anweisungen im DirectShow SDK-Dokumentationsthema "Einrichten der Buildumgebung" konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="a5c72-156">To run this example, you must have the DirectX SDK installed and your build environment must be configured according to the instructions in the DirectShow SDK documentation topic "Setting Up the Build Environment."</span></span> <span data-ttu-id="a5c72-157">Außerdem müssen Sie im Aufruf von RenderFile eine Datei auf Ihrem **Computer angeben.**</span><span class="sxs-lookup"><span data-stu-id="a5c72-157">Also, you must specify a file on your computer in the call to **RenderFile**.</span></span>


```C++
#include <dshow.h>
#include <stdio.h>

void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the Filter Graph Manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file
    // on your system.
    hr = pGraph->RenderFile(L"test.wmv", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}

```



<span data-ttu-id="a5c72-158">Beachten Sie, dass der Anwendungscode für dieses einfache Beispiel nie speziell auf den WM ASF-Reader verweist.</span><span class="sxs-lookup"><span data-stu-id="a5c72-158">Note that the application code for this simple example never references the WM ASF Reader specifically.</span></span> <span data-ttu-id="a5c72-159">Dieser Filter wird vom Filterdiagramm-Manager erstellt, verbunden, ausgeführt und schließlich freigegeben.</span><span class="sxs-lookup"><span data-stu-id="a5c72-159">That filter is created, connected, run, and eventually released by the Filter Graph Manager.</span></span> <span data-ttu-id="a5c72-160">In vielen Szenarien sollten Sie jedoch den WM ASF-Reader konfigurieren, bevor Sie mit der Wiedergabe beginnen.</span><span class="sxs-lookup"><span data-stu-id="a5c72-160">In many scenarios, however, you may want to configure the WM ASF Reader before beginning playback.</span></span>

 

 




