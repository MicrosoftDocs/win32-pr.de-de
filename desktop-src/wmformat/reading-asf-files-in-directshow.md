---
title: Lesen von ASF-Dateien in DirectShow (Windows Media-Format 11 SDK)
description: Lesen von ASF-Dateien in DirectShow
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, Lesen von ASF-Dateien
- Windows Media-Format-SDK, WM-ASF-Reader-Filter
- Windows Media-Format-SDK, imediaseeking-Schnittstelle
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Lesen von Dateien
- ASF (Advanced Systems Format), Lesen von Dateien
- Advanced Systems Format (ASF), WM-ASF-Lesefilter
- ASF (Advanced Systems Format), WM-ASF-Lesefilter
- Advanced Systems Format (ASF), imediaseeking-Schnittstelle
- ASF (Advanced Systems Format), imediaseeking-Schnittstelle
- DirectShow, Lesen von ASF-Dateien
- DirectShow, WM-ASF-Reader-Filter
- DirectShow, imediaseeking-Schnittstelle
- WM-ASF-Lesefilter
- Imediaseeking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1ddf7ba34444f4a3b46f4413958bd26ba4bafc8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104340147"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="353ab-120">Lesen von ASF-Dateien in DirectShow (Windows Media-Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="353ab-120">Reading ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="353ab-121">Die Wiedergabe von ASF-Dateien wird vom [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter behandelt.</span><span class="sxs-lookup"><span data-stu-id="353ab-121">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="353ab-122">Wenn der WM-ASF-Reader eine Datei liest, erstellt er automatisch eine Ausgabe-PIN für jeden Stream, einschließlich Webstreams, Skript befehlsstreams und beliebiger anderer Typen von beliebigem Stream.</span><span class="sxs-lookup"><span data-stu-id="353ab-122">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including Web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="353ab-123">Im Fall von Dateien mit mehreren Bitraten werden Pins nur für die aktuell ausgewählten Streams erstellt.</span><span class="sxs-lookup"><span data-stu-id="353ab-123">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span>

<span data-ttu-id="353ab-124">Der WM-ASF-Reader unterstützt die Schnittstelle DirectShow **imediaseeking** , mit der Anwendungen eine temporale Suche innerhalb der Datei durchführen können.</span><span class="sxs-lookup"><span data-stu-id="353ab-124">The WM ASF Reader supports the DirectShow **IMediaSeeking** interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="353ab-125">Die Wiedergabe mit einer anderen Geschwindigkeit als 1,0 (wie in **imediaseeking::**\* angegeben) wird jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="353ab-125">However, playback at speeds other than 1.0 (as specified in **IMediaSeeking::SetRate**) is not supported.</span></span>

<span data-ttu-id="353ab-126">Der Filter macht auch mehrere Windows Media-Format-SDK-Schnittstellen verfügbar, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="353ab-126">The filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span>



| <span data-ttu-id="353ab-127">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="353ab-127">Interface</span></span>                                        | <span data-ttu-id="353ab-128">Verfügbar gemacht</span><span class="sxs-lookup"><span data-stu-id="353ab-128">How exposed</span></span>                            | <span data-ttu-id="353ab-129">Kommentare</span><span class="sxs-lookup"><span data-stu-id="353ab-129">Comments</span></span>                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="353ab-130">**Iwmdrmreader**</span><span class="sxs-lookup"><span data-stu-id="353ab-130">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="353ab-131">Über **IServiceProvider** beim Filter</span><span class="sxs-lookup"><span data-stu-id="353ab-131">Through **IServiceProvider** on filter</span></span> | <span data-ttu-id="353ab-132">Wird für Anwendungen bereitgestellt, die durch Digital Rights Management (DRM) geschützte Inhalte wiedergeben müssen.</span><span class="sxs-lookup"><span data-stu-id="353ab-132">Provided for applications that need to play content protected by Digital Rights Management (DRM).</span></span> <span data-ttu-id="353ab-133">Diese Schnittstelle kann auch verwendet werden, um andere Schnittstellen des Reader-Objekts direkt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="353ab-133">This interface can also be used to obtain other interfaces on the Reader Object directly.</span></span> |
| [<span data-ttu-id="353ab-134">**Iwmheaderinfo**</span><span class="sxs-lookup"><span data-stu-id="353ab-134">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="353ab-135">**QueryInterface** bei Filter</span><span class="sxs-lookup"><span data-stu-id="353ab-135">**QueryInterface** on filter</span></span>           | <span data-ttu-id="353ab-136">Bereitgestellt, damit Anwendungen Datei-und Inhalts Attribute sowie Marker-und Skriptinformationen sowie Metadaten lesen können.</span><span class="sxs-lookup"><span data-stu-id="353ab-136">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>                                                                  |
| [<span data-ttu-id="353ab-137">**Iwmreaderadvanced**</span><span class="sxs-lookup"><span data-stu-id="353ab-137">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="353ab-138">**QueryInterface** bei Filter</span><span class="sxs-lookup"><span data-stu-id="353ab-138">**QueryInterface** on filter</span></span>           | <span data-ttu-id="353ab-139">Teilweise für den Filter implementiert, damit Anwendungen auf die Informationsmethoden des WM-Reader-Objekts zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="353ab-139">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>                                                                      |
| [<span data-ttu-id="353ab-140">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="353ab-140">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="353ab-141">**QueryInterface** bei Filter</span><span class="sxs-lookup"><span data-stu-id="353ab-141">**QueryInterface** on filter</span></span>           | <span data-ttu-id="353ab-142">Teilweise für den Filter implementiert, damit Anwendungen auf die Informationsmethoden des Reader-Objekts zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="353ab-142">Partially implemented on the filter so that applications can access the informational methods on the Reader Object.</span></span>                                                                         |



 

<span data-ttu-id="353ab-143">Der [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter wurde zuerst in DirectShow 8,0 verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="353ab-143">The [WM ASF Reader](wm-asf-reader-filter.md) filter was first made available in DirectShow 8.0.</span></span> <span data-ttu-id="353ab-144">Die Version des Filters, die im Lieferumfang von DirectShow 8,1 und 9,0 enthalten ist, unterstützt Version 7. *x* des SDK für den Windows Media-Format.</span><span class="sxs-lookup"><span data-stu-id="353ab-144">The version of the filter that ships with DirectShow 8.1 and 9.0 supports version 7.*x* of the Windows Media Format SDK.</span></span> <span data-ttu-id="353ab-145">Die neueste Version des Filters, zusammen mit den anderen qasf-Komponenten, ist im Lieferumfang des SDK der Windows Media-Serie 9 und höher enthalten und unterstützt das Windows Media-Format der Serie 9 und höhere Versionen und ersetzt den Filter in DirectX 9,0.</span><span class="sxs-lookup"><span data-stu-id="353ab-145">The most recent version of the filter, along with the other QASF components, ships with and supports the Windows Media Format 9 Series SDK, and later versions, and it supersedes the filter in DirectX 9.0.</span></span> <span data-ttu-id="353ab-146">Wenn Sie das Windows Media-Format-SDK nach der Installation von DirectX 8 installieren. *x* oder 9. *x* SDK: Sie überschreiben die DirectX-Version von qasf.dll mit der Version 9 der Serie.</span><span class="sxs-lookup"><span data-stu-id="353ab-146">If you install the Windows Media Format SDK after installing the DirectX 8.*x* or 9.*x* SDK, you will overwrite the DirectX version of qasf.dll with the 9 Series version.</span></span> <span data-ttu-id="353ab-147">Dies sollte keine Probleme darstellen, außer möglicherweise in einem Szenario, in dem es zu einem anderen Verhalten in der DirectShow **igraphbuilder:: RenderFile** -Methode führt.</span><span class="sxs-lookup"><span data-stu-id="353ab-147">This should not present any problems except possibly in one scenario where it will result in different behavior in the DirectShow **IGraphBuilder::RenderFile** method.</span></span> <span data-ttu-id="353ab-148">Die SDK-Version des Windows Media Format 9-Formats des WM-ASF-Readers ist der Standard Quell Filter für die Dateinamen Erweiterungen ". ASF", ". wmv" und ". wma".</span><span class="sxs-lookup"><span data-stu-id="353ab-148">The Windows Media Format 9 Series SDK version of the WM ASF Reader is the default source filter for the .asf, .wmv, and .wma file name extensions.</span></span> <span data-ttu-id="353ab-149">Dies bedeutet, dass der WM-ASF-Reader vom Filter Graph-Manager in Methoden wie **igraphbuilder:: RenderFile** oder **igraphbuilder:: addsourcefilter** automatisch erstellt und dem Filter Diagramm hinzugefügt wird, wenn eine Datei dieses Typs angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="353ab-149">This means that the WM ASF Reader is automatically created and added to the filter graph by the Filter Graph Manager in methods such as **IGraphBuilder::RenderFile** or **IGraphBuilder::AddSourceFilter** when a file of this type is specified.</span></span> <span data-ttu-id="353ab-150">In DirectX 9,0 und früheren Versionen und Windows XP Service Pack 1 und früher verwendet die **RenderFile** -Methode den älteren Windows Media-Quell Filter.</span><span class="sxs-lookup"><span data-stu-id="353ab-150">In DirectX 9.0 and earlier, and Windows XP Service Pack 1 and earlier, the **RenderFile** method uses the older Windows Media Source Filter.</span></span> <span data-ttu-id="353ab-151">Dieses Verhalten wurde beibehalten, um die Abwärtskompatibilität mit Anwendungen sicherzustellen, die Windows Media Player 6,4 verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="353ab-151">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="353ab-152">Weitere Informationen zum Legacy-Windows Media-Quell Filter finden Sie in der DirectShow SDK-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="353ab-152">For more information about the legacy Windows Media Source Filter, see the DirectShow SDK Documentation.</span></span>

<span data-ttu-id="353ab-153">Um eine ASF-Datei mit Windows Media – basierten Inhalt mithilfe des WM-ASF-Readers wiederzugeben, müssen Sie zunächst eine Instanz des Filter Graph-Managers erstellen, **igraphbuilder:: RenderFile** zum Erstellen des Diagramms und dann **IMediaControl:: Run** zum Wiedergeben der Datei abrufen.</span><span class="sxs-lookup"><span data-stu-id="353ab-153">To play an ASF file with Windows Media–based content using the WM ASF Reader, the three primary steps are to create an instance of the Filter Graph Manager, call **IGraphBuilder::RenderFile** to create the graph, and then call **IMediaControl::Run** to play the file.</span></span> <span data-ttu-id="353ab-154">Das folgende Codebeispiel ist ein umfassendes Programm, das eine ASF-Datei mithilfe von DirectShow wieder gibt.</span><span class="sxs-lookup"><span data-stu-id="353ab-154">The following code example is a complete program that plays an ASF file using DirectShow.</span></span> <span data-ttu-id="353ab-155">Zum Ausführen dieses Beispiels müssen Sie das DirectX SDK installiert haben, und ihre Buildumgebung muss gemäß den Anweisungen im DirectShow SDK-Dokumentations Thema "Einrichten der Buildumgebung" konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="353ab-155">To run this example, you must have the DirectX SDK installed and your build environment must be configured according to the instructions in the DirectShow SDK documentation topic "Setting Up the Build Environment."</span></span> <span data-ttu-id="353ab-156">Außerdem müssen Sie im **RenderFile**-aufruppenbefehl eine Datei auf Ihrem Computer angeben.</span><span class="sxs-lookup"><span data-stu-id="353ab-156">Also, you must specify a file on your computer in the call to **RenderFile**.</span></span>


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



<span data-ttu-id="353ab-157">Beachten Sie, dass der Anwendungscode für dieses einfache Beispiel nie auf den WM-ASF-Reader verweist.</span><span class="sxs-lookup"><span data-stu-id="353ab-157">Note that the application code for this simple example never references the WM ASF Reader specifically.</span></span> <span data-ttu-id="353ab-158">Dieser Filter wird erstellt, verbunden, ausgeführt und schließlich vom Filter Graph-Manager freigegeben.</span><span class="sxs-lookup"><span data-stu-id="353ab-158">That filter is created, connected, run, and eventually released by the Filter Graph Manager.</span></span> <span data-ttu-id="353ab-159">In vielen Szenarien empfiehlt es sich jedoch, den WM-ASF-Reader vor der Wiedergabe zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="353ab-159">In many scenarios, however, you may want to configure the WM ASF Reader before beginning playback.</span></span>

 

 




