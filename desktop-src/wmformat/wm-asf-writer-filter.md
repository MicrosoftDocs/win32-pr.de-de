---
title: WM ASF Writer Filter (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über den WM ASF Writer-Filter für das Windows Media Format 11 SDK. Überprüfen Sie die Filterinformationen, und sehen Sie sich verwandte Themen an.
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK, WM ASF Writer
- DirectShow, WM ASF Writer
- QASF-Filter, WM ASF Writer
- WM ASF Writer,about
- Advanced Systems Format (ASF), WM ASF Writer
- ASF (Advanced Systems Format), WM ASF Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24ee013b55455c3100ee23e076b767d70fb3ffda
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119665"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a><span data-ttu-id="10d05-110">WM ASF Writer Filter (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="10d05-110">WM ASF Writer Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="10d05-111">Der WM ASF Writer-Filter akzeptiert eine variable Anzahl von Eingabestreams und erstellt eine ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="10d05-111">The WM ASF Writer filter accepts a variable number of input streams and creates an ASF file.</span></span> <span data-ttu-id="10d05-112">Der Filter verarbeitet alle Komprimierungen und Multiplexings (obwohl der Komprimierungsmechanismus umgangen werden kann).</span><span class="sxs-lookup"><span data-stu-id="10d05-112">The filter handles all compression and multiplexing (although the compression mechanism can be bypassed).</span></span> <span data-ttu-id="10d05-113">Sie können den WM ASF Writer-Filter in verschiedenen Szenarien verwenden, einschließlich der Erfassung digitaler Videos (DV), der Audiorekomprimierung und der Konvertierung von Audio-Video Interleaved -Dateien (AVI) oder MPEG-Digitalmediendateien für das Netzwerkstreaming.</span><span class="sxs-lookup"><span data-stu-id="10d05-113">You can use the WM ASF Writer filter in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG digital media files for network streaming.</span></span> <span data-ttu-id="10d05-114">Dieser Filter bietet die einzige Möglichkeit, Microsoft-Windows Media Audio und Windows Media Video in DirectShow zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="10d05-114">This filter provides the only way to create Microsoft Windows Media Audio and Windows Media Video files in DirectShow.</span></span>

<span data-ttu-id="10d05-115">Weitere Informationen finden Sie unter [Erstellen von ASF-Dateien in DirectShow.](creating-asf-files-in-directshow.md)</span><span class="sxs-lookup"><span data-stu-id="10d05-115">For more information, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="10d05-116">Die folgende Tabelle enthält Informationen zum WM ASF Writer-Filter, z. B. die unterstützten Schnittstellen und Medientypen.</span><span class="sxs-lookup"><span data-stu-id="10d05-116">The following table contains information about the WM ASF Writer filter, such as the interfaces and media types it supports.</span></span>



| <span data-ttu-id="10d05-117">Filterinformationen</span><span class="sxs-lookup"><span data-stu-id="10d05-117">Filter Information</span></span>                       |  <span data-ttu-id="10d05-118">Typen</span><span class="sxs-lookup"><span data-stu-id="10d05-118">Types</span></span>                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="10d05-119">Filtern von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="10d05-119">Filter interfaces</span></span>      | <span data-ttu-id="10d05-120">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="10d05-120">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span></span> |
| <span data-ttu-id="10d05-121">Eingabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="10d05-121">Input pin media types</span></span>  | <span data-ttu-id="10d05-122">Abhängig vom Profil.</span><span class="sxs-lookup"><span data-stu-id="10d05-122">Dependent on the profile.</span></span> <span data-ttu-id="10d05-123">In der Regel unkomprimierte Typen wie MEDIATYPE Audio oder MEDIATYPE Video, obwohl komprimierte Typen akzeptiert werden können, wenn \_ sie mit dem Profil \_ übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="10d05-123">Typically uncompressed types like MEDIATYPE\_Audio or MEDIATYPE\_Video, although compressed types can be accepted if they match the profile</span></span>                                                   |
| <span data-ttu-id="10d05-124">Eingabepinschnittstellen</span><span class="sxs-lookup"><span data-stu-id="10d05-124">Input pin interfaces</span></span>   | <span data-ttu-id="10d05-125">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (über **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="10d05-125">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                         |
| <span data-ttu-id="10d05-126">Ausgabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="10d05-126">Output pin media types</span></span> | <span data-ttu-id="10d05-127">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="10d05-127">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="10d05-128">Schnittstellen für Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="10d05-128">Output pin interfaces</span></span>  | <span data-ttu-id="10d05-129">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="10d05-129">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="10d05-130">Filtern der CLSID</span><span class="sxs-lookup"><span data-stu-id="10d05-130">Filter CLSID</span></span>           | <span data-ttu-id="10d05-131">CLSID \_ WMAsfWriter</span><span class="sxs-lookup"><span data-stu-id="10d05-131">CLSID\_WMAsfWriter</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="10d05-132">Eigenschaftenseite CLSID</span><span class="sxs-lookup"><span data-stu-id="10d05-132">Property page CLSID</span></span>    | <span data-ttu-id="10d05-133">CLSID \_ WMAsfWriterProperties</span><span class="sxs-lookup"><span data-stu-id="10d05-133">CLSID\_WMAsfWriterProperties</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="10d05-134">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="10d05-134">Executable</span></span>             | <span data-ttu-id="10d05-135">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="10d05-135">Qasf.dll</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="10d05-136">Verdienst</span><span class="sxs-lookup"><span data-stu-id="10d05-136">Merit</span></span>                  | <span data-ttu-id="10d05-137">NICHT \_ \_ VERWENDEN \_</span><span class="sxs-lookup"><span data-stu-id="10d05-137">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="10d05-138">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="10d05-138">Filter Category</span></span>        | <span data-ttu-id="10d05-139">Nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="10d05-139">Not specified</span></span>                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="10d05-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10d05-140">Remarks</span></span>

<span data-ttu-id="10d05-141">Die Anzahl der Eingabepins für den Filter hängt vom Profil ab, das an den Filter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="10d05-141">The number of input pins on the filter depends on the profile that is passed to the filter.</span></span> <span data-ttu-id="10d05-142">Für jeden im Profil definierten Stream wird ein Pin des entsprechenden Medientyps erstellt.</span><span class="sxs-lookup"><span data-stu-id="10d05-142">One pin of the appropriate media type is created for each stream defined in the profile.</span></span>

<span data-ttu-id="10d05-143">Die Eingabepins unterstützen eine Methode der **IAMStreamConfig-Schnittstelle:** **IAMStreamConfig::GetFormat**.</span><span class="sxs-lookup"><span data-stu-id="10d05-143">The input pins support one method from the **IAMStreamConfig** interface: **IAMStreamConfig::GetFormat**.</span></span> <span data-ttu-id="10d05-144">Alle anderen Methoden geben E \_ NOTIMPL zurück.</span><span class="sxs-lookup"><span data-stu-id="10d05-144">All other methods return E\_NOTIMPL.</span></span> <span data-ttu-id="10d05-145">Rufen Sie die **GetFormat-Methode** auf, um das Zielkomprimierungsformat des Pins abfragt, das durch das aktuelle Profil definiert wird.</span><span class="sxs-lookup"><span data-stu-id="10d05-145">Call the **GetFormat** method to query the pin's destination compression format, which is defined by the current profile.</span></span> <span data-ttu-id="10d05-146">Verwenden Sie die [**IConfigAsfWriter-Schnittstelle**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) zum Festlegen des Profils.</span><span class="sxs-lookup"><span data-stu-id="10d05-146">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface to set the profile.</span></span>

<span data-ttu-id="10d05-147">Mit der **IServiceProvider-Schnittstelle** des Filters können Anwendungen die [**IMMWriterAdvanced2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) abrufen, die im Windows Media Format SDK definiert ist.</span><span class="sxs-lookup"><span data-stu-id="10d05-147">The filter's **IServiceProvider** interface enables applications to retrieve the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface, which is defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="10d05-148">Die **IWMWriterAdvanced2-Schnittstelle** steuert das Videodeinterlacing und [](wmformat-glossary.md) ist nützlich, wenn es sich bei der Eingabe um eine Verschachtelungsquelle handelt, z. B. DV (digitales Video).</span><span class="sxs-lookup"><span data-stu-id="10d05-148">The **IWMWriterAdvanced2** interface controls video deinterlacing, and is useful if the input is an [*interlaced*](wmformat-glossary.md) source, such as DV (digital video).</span></span> <span data-ttu-id="10d05-149">Verwenden Sie **die Methoden GetInputSetting** und **SetInputSetting,** um das Deinterlacing zu steuern.</span><span class="sxs-lookup"><span data-stu-id="10d05-149">Use the **GetInputSetting** and **SetInputSetting** methods to control deinterlacing.</span></span> <span data-ttu-id="10d05-150">Es wird nicht empfohlen, dass Clients eine der anderen Methoden auf dieser Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="10d05-150">It is not recommended that clients use any of the other methods on this interface.</span></span> <span data-ttu-id="10d05-151">Diese Schnittstelle kann erst nach dem Hinzufügen des Filters zum Filterdiagramm ermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="10d05-151">This interface can only be obtained after the filter has been added to the filter graph.</span></span> <span data-ttu-id="10d05-152">Das folgende Beispiel zeigt, wie Sie diese Schnittstelle abfragen:</span><span class="sxs-lookup"><span data-stu-id="10d05-152">The following example shows how to query for this interface:</span></span>


```C++
// Assume that m_pGraph is a valid IGraphBuilder interface pointer,
// and that pAsfWriter points to the IBaseFilter interface
// on the WM ASF Writer filter.

IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = m_pGraph->AddFilter(pAsfWriter, L"WM ASF Writer");
...
hr = pAsfWriter->QueryInterface(IID_IServiceProvider, (void**)&pProvider)
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, (void**)&pWMWA2);
    pProvider->Release();
}

```



## <a name="related-topics"></a><span data-ttu-id="10d05-153">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="10d05-153">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10d05-154">**DirectShow QASF-Referenz**</span><span class="sxs-lookup"><span data-stu-id="10d05-154">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 
