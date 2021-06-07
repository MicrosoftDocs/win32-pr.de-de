---
title: WM ASF Writer-Filter (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über den WM ASF Writer-Filter.
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK, WM ASF Writer
- DirectShow,WM ASF Writer
- QASF-Filter, WM ASF Writer
- WM ASF Writer, Informationen
- Advanced Systems Format (ASF), WM ASF Writer
- ASF (Advanced Systems Format), WM ASF Writer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0fbd6e36a8178f6ebd1943cdaac214597e0ba4e
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444701"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a><span data-ttu-id="0f947-109">WM ASF Writer-Filter (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="0f947-109">WM ASF Writer Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="0f947-110">Der WM ASF Writer-Filter akzeptiert eine variable Anzahl von Eingabestreams und erstellt eine ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="0f947-110">The WM ASF Writer filter accepts a variable number of input streams and creates an ASF file.</span></span> <span data-ttu-id="0f947-111">Der Filter verarbeitet die gesamte Komprimierung und das Multiplexing (obwohl der Komprimierungsmechanismus umgangen werden kann).</span><span class="sxs-lookup"><span data-stu-id="0f947-111">The filter handles all compression and multiplexing (although the compression mechanism can be bypassed).</span></span> <span data-ttu-id="0f947-112">Sie können den WM ASF Writer-Filter in verschiedenen Szenarien verwenden, z. B. digitale Videoaufzeichnung (DV), Audiorekomprimierung und Konvertierung von Audio-Video Interleaved (AVI) oder MPEG Digital Media Files für das Netzwerkstreaming.</span><span class="sxs-lookup"><span data-stu-id="0f947-112">You can use the WM ASF Writer filter in various scenarios including digital video (DV) capture, audio recompression, and conversion of Audio-Video Interleaved (AVI) or MPEG digital media files for network streaming.</span></span> <span data-ttu-id="0f947-113">Dieser Filter bietet die einzige Möglichkeit, Microsoft Windows Media Audio- und Windows Media Video-Dateien in DirectShow zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0f947-113">This filter provides the only way to create Microsoft Windows Media Audio and Windows Media Video files in DirectShow.</span></span>

<span data-ttu-id="0f947-114">Weitere Informationen finden Sie unter [Erstellen von ASF-Dateien in DirectShow.](creating-asf-files-in-directshow.md)</span><span class="sxs-lookup"><span data-stu-id="0f947-114">For more information, see [Creating ASF Files in DirectShow](creating-asf-files-in-directshow.md).</span></span>

<span data-ttu-id="0f947-115">Die folgende Tabelle enthält Informationen zum WM ASF Writer-Filter, z. B. die unterstützten Schnittstellen und Medientypen.</span><span class="sxs-lookup"><span data-stu-id="0f947-115">The following table contains information about the WM ASF Writer filter, such as the interfaces and media types it supports.</span></span>



| <span data-ttu-id="0f947-116">Filterinformationen</span><span class="sxs-lookup"><span data-stu-id="0f947-116">Filter Information</span></span>                       |  <span data-ttu-id="0f947-117">Typen</span><span class="sxs-lookup"><span data-stu-id="0f947-117">Types</span></span>                                                                                                                                                                                                                       |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f947-118">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="0f947-118">Filter interfaces</span></span>      | <span data-ttu-id="0f947-119">**IAMFilterMiscFlags,** **IBaseFilter,** **IConfigAsfWriter,** **IFileSinkFilter2,** IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2,** **IWMHeaderInfo,** **IWMWriterAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="0f947-119">**IAMFilterMiscFlags**, **IBaseFilter**, **IConfigAsfWriter**, **IFileSinkFilter2**, IMediaSeeking, IPersistStream, IServiceProvider, ISpecifyPropertyPages, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2**</span></span> |
| <span data-ttu-id="0f947-120">Eingabepinmedientypen</span><span class="sxs-lookup"><span data-stu-id="0f947-120">Input pin media types</span></span>  | <span data-ttu-id="0f947-121">Abhängig vom Profil.</span><span class="sxs-lookup"><span data-stu-id="0f947-121">Dependent on the profile.</span></span> <span data-ttu-id="0f947-122">In der Regel nicht komprimierte Typen wie MEDIATYPE \_ Audio oder MEDIATYPE \_ Video, obwohl komprimierte Typen akzeptiert werden können, wenn sie mit dem Profil übereinstimmen</span><span class="sxs-lookup"><span data-stu-id="0f947-122">Typically uncompressed types like MEDIATYPE\_Audio or MEDIATYPE\_Video, although compressed types can be accepted if they match the profile</span></span>                                                   |
| <span data-ttu-id="0f947-123">Eingabepinschnittstellen</span><span class="sxs-lookup"><span data-stu-id="0f947-123">Input pin interfaces</span></span>   | <span data-ttu-id="0f947-124">**IPin,** **IMemInputPin,** **IAMStreamConfig,** **IServiceProvider,** **IAMWMBufferPass,** **IWMStreamConfig2** (über **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="0f947-124">**IPin**, **IMemInputPin**, **IAMStreamConfig**, **IServiceProvider**, **IAMWMBufferPass**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                         |
| <span data-ttu-id="0f947-125">Medientypen des Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="0f947-125">Output pin media types</span></span> | <span data-ttu-id="0f947-126">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="0f947-126">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="0f947-127">Ausgabepinschnittstellen</span><span class="sxs-lookup"><span data-stu-id="0f947-127">Output pin interfaces</span></span>  | <span data-ttu-id="0f947-128">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="0f947-128">Not applicable</span></span>                                                                                                                                                                                                          |
| <span data-ttu-id="0f947-129">Filtern von CLSID</span><span class="sxs-lookup"><span data-stu-id="0f947-129">Filter CLSID</span></span>           | <span data-ttu-id="0f947-130">CLSID \_ WMAsfWriter</span><span class="sxs-lookup"><span data-stu-id="0f947-130">CLSID\_WMAsfWriter</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="0f947-131">CLSID der Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="0f947-131">Property page CLSID</span></span>    | <span data-ttu-id="0f947-132">CLSID \_ WMAsfWriterProperties</span><span class="sxs-lookup"><span data-stu-id="0f947-132">CLSID\_WMAsfWriterProperties</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="0f947-133">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="0f947-133">Executable</span></span>             | <span data-ttu-id="0f947-134">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="0f947-134">Qasf.dll</span></span>                                                                                                                                                                                                                |
| <span data-ttu-id="0f947-135">Verdienst</span><span class="sxs-lookup"><span data-stu-id="0f947-135">Merit</span></span>                  | <span data-ttu-id="0f947-136">DIES IST \_ \_ NICHT ZU \_ VERWENDEN.</span><span class="sxs-lookup"><span data-stu-id="0f947-136">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                     |
| <span data-ttu-id="0f947-137">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="0f947-137">Filter Category</span></span>        | <span data-ttu-id="0f947-138">Nicht angegeben</span><span class="sxs-lookup"><span data-stu-id="0f947-138">Not specified</span></span>                                                                                                                                                                                                           |



 

## <a name="remarks"></a><span data-ttu-id="0f947-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0f947-139">Remarks</span></span>

<span data-ttu-id="0f947-140">Die Anzahl der Eingabepins für den Filter hängt vom Profil ab, das an den Filter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0f947-140">The number of input pins on the filter depends on the profile that is passed to the filter.</span></span> <span data-ttu-id="0f947-141">Für jeden im Profil definierten Stream wird ein Pin des entsprechenden Medientyps erstellt.</span><span class="sxs-lookup"><span data-stu-id="0f947-141">One pin of the appropriate media type is created for each stream defined in the profile.</span></span>

<span data-ttu-id="0f947-142">Die Eingabepins unterstützen eine Methode der **IAMStreamConfig-Schnittstelle:** **IAMStreamConfig::GetFormat**.</span><span class="sxs-lookup"><span data-stu-id="0f947-142">The input pins support one method from the **IAMStreamConfig** interface: **IAMStreamConfig::GetFormat**.</span></span> <span data-ttu-id="0f947-143">Alle anderen Methoden geben E \_ NOTIMPL zurück.</span><span class="sxs-lookup"><span data-stu-id="0f947-143">All other methods return E\_NOTIMPL.</span></span> <span data-ttu-id="0f947-144">Rufen Sie die **GetFormat-Methode** auf, um das Zielkomprimierungsformat des Pins abzufragen, das vom aktuellen Profil definiert wird.</span><span class="sxs-lookup"><span data-stu-id="0f947-144">Call the **GetFormat** method to query the pin's destination compression format, which is defined by the current profile.</span></span> <span data-ttu-id="0f947-145">Verwenden Sie die [**IConfigAsfWriter-Schnittstelle,**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) um das Profil festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0f947-145">Use the [**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) interface to set the profile.</span></span>

<span data-ttu-id="0f947-146">Mit der **IServiceProvider-Schnittstelle** des Filters können Anwendungen die [**IWMWriterAdvanced2-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) abrufen, die im Windows Media Format SDK definiert ist.</span><span class="sxs-lookup"><span data-stu-id="0f947-146">The filter's **IServiceProvider** interface enables applications to retrieve the [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) interface, which is defined in the Windows Media Format SDK.</span></span> <span data-ttu-id="0f947-147">Die **IWMWriterAdvanced2-Schnittstelle** steuert das Deinterlacing von Videos und ist nützlich, wenn es sich bei der Eingabe um eine Quelle mit [*Zeilensprung*](wmformat-glossary.md) handelt, z. B. DV (digitales Video).</span><span class="sxs-lookup"><span data-stu-id="0f947-147">The **IWMWriterAdvanced2** interface controls video deinterlacing, and is useful if the input is an [*interlaced*](wmformat-glossary.md) source, such as DV (digital video).</span></span> <span data-ttu-id="0f947-148">Verwenden Sie die **Methoden GetInputSetting** und **SetInputSetting,** um das Deinterlacing zu steuern.</span><span class="sxs-lookup"><span data-stu-id="0f947-148">Use the **GetInputSetting** and **SetInputSetting** methods to control deinterlacing.</span></span> <span data-ttu-id="0f947-149">Es wird nicht empfohlen, dass Clients eine der anderen Methoden auf dieser Schnittstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="0f947-149">It is not recommended that clients use any of the other methods on this interface.</span></span> <span data-ttu-id="0f947-150">Diese Schnittstelle kann erst abgerufen werden, nachdem der Filter dem Filterdiagramm hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="0f947-150">This interface can only be obtained after the filter has been added to the filter graph.</span></span> <span data-ttu-id="0f947-151">Das folgende Beispiel zeigt, wie Sie diese Schnittstelle abfragen:</span><span class="sxs-lookup"><span data-stu-id="0f947-151">The following example shows how to query for this interface:</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="0f947-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0f947-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f947-153">**DirectShow-QASF-Referenz**</span><span class="sxs-lookup"><span data-stu-id="0f947-153">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> </dl>

 

 
