---
title: WM-ASF-Writer-Filter (Windows Media Format 11 SDK)
description: WM-ASF-Writer-Filter
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media-Format-SDK, WM-ASF-Writer
- DirectShow, WM-ASF-Writer
- Qasf-Filter, WM-ASF-Writer
- WM-ASF-Writer, Informationen zu
- Advanced Systems Format (ASF), WM-ASF-Writer
- ASF (Advanced Systems Format), WM-ASF-Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0de34bcf4b4047673f832d78f40377f98e94d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106340551"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a><span data-ttu-id="e5d20-109">WM-ASF-Writer-Filter (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="e5d20-109">WM ASF Writer Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="e5d20-110">Der WM-ASF-Writer-Filter akzeptiert eine Variable Anzahl von Eingabedaten strömen und erstellt eine ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="e5d20-110">The WM ASF Writer filter accepts a variable number of input streams and creates an ASF file.</span></span> <span data-ttu-id="e5d20-111">Der Filter verarbeitet alle Komprimierungen und Multiplexing (obwohl der Komprimierungs Mechanismus umgangen werden kann).</span><span class="sxs-lookup"><span data-stu-id="e5d20-111">The filter handles all compression and multiplexing (although the compression mechanism can be bypassed).</span></span> <span data-ttu-id="e5d20-112">Sie können den WM-ASF-Writer-Filter in verschiedenen Szenarien verwenden, einschließlich digitaler Video Erfassung (DV), audioneukomprimierung und Konvertierung von Audio-Video Interleaved (AVI) oder MPEG Digital Media Files for Network Streaming.</span><span class="sxs-lookup"><span data-stu-id="e5d20-112">You can use the WM ASF Writer filter in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG digital media files for network streaming.</span></span> <span data-ttu-id="e5d20-113">Dieser Filter stellt die einzige Möglichkeit zum Erstellen von Microsoft-Windows Media Audio und Windows Media Video Dateien in DirectShow dar.</span><span class="sxs-lookup"><span data-stu-id="e5d20-113">This filter provides the only way to create Microsoft Windows Media Audio and Windows Media Video files in DirectShow.</span></span>

<span data-ttu-id="e5d20-114">Weitere Informationen finden Sie unter [Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="e5d20-114">For more information, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="e5d20-115">Die folgende Tabelle enthält Informationen zum WM-ASF-Writer-Filter, z. b. die Schnittstellen und die unterstützten Medientypen.</span><span class="sxs-lookup"><span data-stu-id="e5d20-115">The following table contains information about the WM ASF Writer filter, such as the interfaces and media types it supports.</span></span>



|                        |                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5d20-116">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e5d20-116">Filter interfaces</span></span>      | <span data-ttu-id="e5d20-117">**Iamfilterfehlflags**, **ibasefilter**, **iconfigasfwriter**, **IFileSinkFilter2**, imediaseeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **iwmheaderinfo**, **IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="e5d20-117">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span></span> |
| <span data-ttu-id="e5d20-118">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="e5d20-118">Input pin media types</span></span>  | <span data-ttu-id="e5d20-119">Abhängig vom Profil.</span><span class="sxs-lookup"><span data-stu-id="e5d20-119">Dependent on the profile.</span></span> <span data-ttu-id="e5d20-120">In der Regel unkomprimierte Typen wie MediaType \_ -Audiodaten oder MediaType- \_ Video, obwohl komprimierte Typen akzeptiert werden können, wenn Sie dem Profil entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e5d20-120">Typically uncompressed types like MEDIATYPE\_Audio or MEDIATYPE\_Video, although compressed types can be accepted if they match the profile</span></span>                                                   |
| <span data-ttu-id="e5d20-121">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="e5d20-121">Input pin interfaces</span></span>   | <span data-ttu-id="e5d20-122">**IPin**, **IMemInputPin**, **iamstreamconfig**, **IServiceProvider**, **iamwmbufferpass**, **IWMStreamConfig2** (über **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="e5d20-122">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                         |
| <span data-ttu-id="e5d20-123">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="e5d20-123">Output pin media types</span></span> | <span data-ttu-id="e5d20-124">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="e5d20-124">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="e5d20-125">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="e5d20-125">Output pin interfaces</span></span>  | <span data-ttu-id="e5d20-126">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="e5d20-126">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="e5d20-127">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="e5d20-127">Filter CLSID</span></span>           | <span data-ttu-id="e5d20-128">CLSID- \_ wmasberwriter</span><span class="sxs-lookup"><span data-stu-id="e5d20-128">CLSID\_WMAsfWriter</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="e5d20-129">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="e5d20-129">Property page CLSID</span></span>    | <span data-ttu-id="e5d20-130">CLSID \_ wmasf-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="e5d20-130">CLSID\_WMAsfWriterProperties</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="e5d20-131">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="e5d20-131">Executable</span></span>             | <span data-ttu-id="e5d20-132">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="e5d20-132">Qasf.dll</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="e5d20-133">Verdienst</span><span class="sxs-lookup"><span data-stu-id="e5d20-133">Merit</span></span>                  | <span data-ttu-id="e5d20-134">das Verdienst wird \_ \_ nicht \_ verwendet.</span><span class="sxs-lookup"><span data-stu-id="e5d20-134">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="e5d20-135">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="e5d20-135">Filter Category</span></span>        | <span data-ttu-id="e5d20-136">Nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="e5d20-136">Not specified</span></span>                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="e5d20-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e5d20-137">Remarks</span></span>

<span data-ttu-id="e5d20-138">Die Anzahl der Eingabe Pins im Filter hängt von dem Profil ab, das an den Filter weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="e5d20-138">The number of input pins on the filter depends on the profile that is passed to the filter.</span></span> <span data-ttu-id="e5d20-139">Für jeden Stream, der im Profil definiert ist, wird eine PIN des entsprechenden Medientyps erstellt.</span><span class="sxs-lookup"><span data-stu-id="e5d20-139">One pin of the appropriate media type is created for each stream defined in the profile.</span></span>

<span data-ttu-id="e5d20-140">Die Eingabe Pins unterstützen eine Methode aus der **iamstreamconfig** -Schnittstelle: **iamstreamconfig:: GetFormat**.</span><span class="sxs-lookup"><span data-stu-id="e5d20-140">The input pins support one method from the **IAMStreamConfig** interface: **IAMStreamConfig::GetFormat**.</span></span> <span data-ttu-id="e5d20-141">Alle anderen Methoden geben E \_ notimpl zurück.</span><span class="sxs-lookup"><span data-stu-id="e5d20-141">All other methods return E\_NOTIMPL.</span></span> <span data-ttu-id="e5d20-142">Aufrufen der **GetFormat** -Methode, um das Ziel Komprimierungs Format der PIN abzufragen, das durch das aktuelle Profil definiert wird.</span><span class="sxs-lookup"><span data-stu-id="e5d20-142">Call the **GetFormat** method to query the pin's destination compression format, which is defined by the current profile.</span></span> <span data-ttu-id="e5d20-143">Verwenden Sie die [**iconfigasfwriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) -Schnittstelle, um das Profil festzulegen.</span><span class="sxs-lookup"><span data-stu-id="e5d20-143">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface to set the profile.</span></span>

<span data-ttu-id="e5d20-144">Die **IServiceProvider** -Schnittstelle des Filters ermöglicht Anwendungen das Abrufen der [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) -Schnittstelle, die im Windows Media-Format-SDK definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e5d20-144">The filter's **IServiceProvider** interface enables applications to retrieve the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface, which is defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="e5d20-145">Die **IWMWriterAdvanced2** -Schnittstelle steuert das Video Deinterlacing und ist nützlich, wenn die [*Eingabe eine Zeilen*](wmformat-glossary.md) Sprung Quelle ist, z. b. DV (digitales Video).</span><span class="sxs-lookup"><span data-stu-id="e5d20-145">The **IWMWriterAdvanced2** interface controls video deinterlacing, and is useful if the input is an [*interlaced*](wmformat-glossary.md) source, such as DV (digital video).</span></span> <span data-ttu-id="e5d20-146">Verwenden Sie die **getinputsetting** -Methode und die-Methode für die **Einstellungs** Methode, um Deinterlacing zu steuern.</span><span class="sxs-lookup"><span data-stu-id="e5d20-146">Use the **GetInputSetting** and **SetInputSetting** methods to control deinterlacing.</span></span> <span data-ttu-id="e5d20-147">Es wird nicht empfohlen, dass Clients eine andere Methode für diese Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="e5d20-147">It is not recommended that clients use any of the other methods on this interface.</span></span> <span data-ttu-id="e5d20-148">Diese Schnittstelle kann nur abgerufen werden, nachdem dem Filter Diagramm der Filter hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="e5d20-148">This interface can only be obtained after the filter has been added to the filter graph.</span></span> <span data-ttu-id="e5d20-149">Im folgenden Beispiel wird gezeigt, wie Sie diese Schnittstelle Abfragen:</span><span class="sxs-lookup"><span data-stu-id="e5d20-149">The following example shows how to query for this interface:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="e5d20-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e5d20-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5d20-151">**DirectShow-qasf-Referenz**</span><span class="sxs-lookup"><span data-stu-id="e5d20-151">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 
