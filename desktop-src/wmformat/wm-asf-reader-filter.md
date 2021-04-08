---
title: WM-ASF-Reader-Filter (Windows Media Format 11 SDK)
description: WM-ASF-Lesefilter
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media-Format-SDK, WM-ASF-Reader
- DirectShow, WM-ASF-Reader
- Qasf-Filter, WM-ASF-Reader
- WM-ASF-Reader
- Advanced Systems Format (ASF), WM-ASF-Reader
- ASF (Advanced Systems Format), WM-ASF-Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e13b7944f45b850a158c9832e174ae5ec7dce4d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739384"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a><span data-ttu-id="dcdf5-109">WM-ASF-Reader-Filter (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="dcdf5-109">WM ASF Reader Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="dcdf5-110">Wenn der Name einer ASF-Datei oder einer URL angegeben wird, liest der WM-ASF-Reader den komprimierten Inhalt, analysiert die Streams und macht für jeden eine Ausgabe-PIN verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dcdf5-110">When given the name of an ASF file or a URL, the WM ASF Reader reads the compressed content, parses the streams, and exposes an output pin for each one.</span></span> <span data-ttu-id="dcdf5-111">Mit diesem Filter wird eine Downstream-Verbindung mit dem Windows Media Audio oder Windows Media Video DMOS hergestellt, die die Komprimierung durchführen.</span><span class="sxs-lookup"><span data-stu-id="dcdf5-111">This filter connects downstream to the Windows Media Audio or Windows Media Video DMOs, which do the decompression.</span></span> <span data-ttu-id="dcdf5-112">Die Suche wird unterstützt, wenn die ASF-Datei suchbar ist.</span><span class="sxs-lookup"><span data-stu-id="dcdf5-112">Seeking is supported if the ASF file is seekable.</span></span> <span data-ttu-id="dcdf5-113">Der WM-ASF-Reader wendet Zeitstempel auf die Medien Beispiele basierend auf dem Zeitstempel in der ASF-Datei an, ändert jedoch nicht die Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="dcdf5-113">The WM ASF Reader applies time stamps to the media samples based on the time stamp in the ASF file, but it does not modify the time stamps in any way.</span></span> <span data-ttu-id="dcdf5-114">Intern verwendet der Filter das Windows Media-Format Reader-Objekt, um den Windows Media – basierten Inhalt zu lesen.</span><span class="sxs-lookup"><span data-stu-id="dcdf5-114">Internally, the filter uses the Windows Media Format reader object to read the Windows Media–based content.</span></span>

> [!Note]  
> <span data-ttu-id="dcdf5-115">Im DirectX SDK ist dieser Filter nicht der Standard Quell Filter für ASF-Dateien, sodass Sie mit diesem SDK diesen Filter nicht mit der **RenderFile** -Methode verwenden können. Sie müssen es explizit dem Filter Diagramm hinzufügen, indem Sie die zugehörige Klassen-ID (Class Identifier, CLSID) verwenden.</span><span class="sxs-lookup"><span data-stu-id="dcdf5-115">In the DirectX SDK, this filter is not the default source filter for ASF files, so with that SDK you cannot use this filter with the **RenderFile** method; you must explicitly add it to the filter graph by using its class identifier (CLSID).</span></span> <span data-ttu-id="dcdf5-116">Dieses Verhalten unterscheidet sich vom Windows Media-Format-SDK.</span><span class="sxs-lookup"><span data-stu-id="dcdf5-116">This behavior is different with the Windows Media Format SDK.</span></span> <span data-ttu-id="dcdf5-117">Wenn Sie die Windows Media Format SDK-Laufzeitbibliotheken installieren, wird der WM-ASF-Reader als Standardfilter für ASF-Dateien registriert.</span><span class="sxs-lookup"><span data-stu-id="dcdf5-117">When you install the Windows Media Format SDK runtime libraries, the WM ASF Reader is registered as the default filter for ASF files.</span></span>

 

<span data-ttu-id="dcdf5-118">Die folgende Tabelle enthält Informationen zum WM-ASF-Reader-Filter, z. b. die Schnittstellen und die unterstützten Medientypen.</span><span class="sxs-lookup"><span data-stu-id="dcdf5-118">The following table contains information about the WM ASF Reader filter, such as the interfaces and media types it supports.</span></span>



|                        |                                                                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcdf5-119">Filter Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="dcdf5-119">Filter interfaces</span></span>      | <span data-ttu-id="dcdf5-120">**Ibasefilter**, **IFileSourceFilter**, **IServiceProvider**, **iwmheaderinfo**, **iwmreaderadvanced** (teilweise implementiert.</span><span class="sxs-lookup"><span data-stu-id="dcdf5-120">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (partially implemented.</span></span> <span data-ttu-id="dcdf5-121">Weitere Informationen finden Sie unter "Hinweise".), **IWMReaderAdvanced2** (teilweise implementiert), **iwmdrmreader** (über **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="dcdf5-121">See Remarks.), **IWMReaderAdvanced2** (partially implemented), **IWMDRMReader** (through **IServiceProvider**)</span></span> |
| <span data-ttu-id="dcdf5-122">Eingabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="dcdf5-122">Input pin media types</span></span>  | <span data-ttu-id="dcdf5-123">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="dcdf5-123">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="dcdf5-124">PIN-Eingabeschnittstellen</span><span class="sxs-lookup"><span data-stu-id="dcdf5-124">Input pin interfaces</span></span>   | <span data-ttu-id="dcdf5-125">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="dcdf5-125">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="dcdf5-126">Ausgabe-PIN-Medientypen</span><span class="sxs-lookup"><span data-stu-id="dcdf5-126">Output pin media types</span></span> | <span data-ttu-id="dcdf5-127">MediaType \_ -Video, MediaType \_ -Audiodatei, MediaType \_ ScriptCommand, MediaType \_ Filetransfer</span><span class="sxs-lookup"><span data-stu-id="dcdf5-127">MEDIATYPE\_Video, MEDIATYPE\_Audio, MEDIATYPE\_ScriptCommand, MEDIATYPE\_FileTransfer</span></span>                                                                                                                                                         |
| <span data-ttu-id="dcdf5-128">Formattyp</span><span class="sxs-lookup"><span data-stu-id="dcdf5-128">Format type</span></span>            | <span data-ttu-id="dcdf5-129">**VIDEOINFOHEADER2** , wenn der Inhalt mit Zeilen Sprung [*verknüpft*](wmformat-glossary.md)ist, andernfalls **videoinfoheader** .</span><span class="sxs-lookup"><span data-stu-id="dcdf5-129">**VIDEOINFOHEADER2** if content is [*interlaced*](wmformat-glossary.md), otherwise **VIDEOINFOHEADER**</span></span>                                                                                                                    |
| <span data-ttu-id="dcdf5-130">PIN-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="dcdf5-130">Output pin interfaces</span></span>  | <span data-ttu-id="dcdf5-131">**Imediaseeking**, **iamwmbufferpass**, **IServiceProvider**, **IWMStreamConfig2** (über **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="dcdf5-131">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                                                                             |
| <span data-ttu-id="dcdf5-132">CLSID Filtern</span><span class="sxs-lookup"><span data-stu-id="dcdf5-132">Filter CLSID</span></span>           | <span data-ttu-id="dcdf5-133">CLSID- \_ wmasfreader</span><span class="sxs-lookup"><span data-stu-id="dcdf5-133">CLSID\_WMAsfReader</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="dcdf5-134">CLSID der Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="dcdf5-134">Property Page CLSID</span></span>    | <span data-ttu-id="dcdf5-135">Keine Eigenschaften Seite</span><span class="sxs-lookup"><span data-stu-id="dcdf5-135">No property page</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="dcdf5-136">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="dcdf5-136">Executable</span></span>             | <span data-ttu-id="dcdf5-137">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="dcdf5-137">Qasf.dll</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="dcdf5-138">Verdienst</span><span class="sxs-lookup"><span data-stu-id="dcdf5-138">Merit</span></span>                  | <span data-ttu-id="dcdf5-139">nicht \_ wahrscheinlich</span><span class="sxs-lookup"><span data-stu-id="dcdf5-139">MERIT\_UNLIKELY</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="dcdf5-140">Filter Kategorie</span><span class="sxs-lookup"><span data-stu-id="dcdf5-140">Filter Category</span></span>        | <span data-ttu-id="dcdf5-141">CLSID \_ legacyamfiltercategory</span><span class="sxs-lookup"><span data-stu-id="dcdf5-141">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="dcdf5-142">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dcdf5-142">Remarks</span></span>

<span data-ttu-id="dcdf5-143">Der WM-ASF-Reader implementiert teilweise die **iwmreaderadvanced** -und **IWMReaderAdvanced2** -Schnittstellen, um Anwendungen den Zugriff auf die Informationsmethoden für das Reader-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="dcdf5-143">The WM ASF Reader partially implements the **IWMReaderAdvanced** and **IWMReaderAdvanced2** interfaces in order to give applications access to the informational methods on the reader object.</span></span> <span data-ttu-id="dcdf5-144">Die Implementierung des Filters übergibt die Aufrufe einfach an die-Schnittstelle des Reader-Objekts.</span><span class="sxs-lookup"><span data-stu-id="dcdf5-144">The filter's implementation simply passes the calls through to the interface on the reader object.</span></span> <span data-ttu-id="dcdf5-145">Die Streamingmethoden werden nicht implementiert, da der Filter über eine umfassende Kontrolle über den streamingprozess verfügen muss.</span><span class="sxs-lookup"><span data-stu-id="dcdf5-145">The streaming methods are not implemented because the filter must have complete control over the streaming process.</span></span> <span data-ttu-id="dcdf5-146">Die folgenden **iwmreaderadvanced** -und **IWMReaderAdvanced2** -Methoden werden implementiert:</span><span class="sxs-lookup"><span data-stu-id="dcdf5-146">The following **IWMReaderAdvanced** and **IWMReaderAdvanced2** methods are implemented:</span></span>

-   [<span data-ttu-id="dcdf5-147">**Iwmreaderadvanced:: getstatistics**</span><span class="sxs-lookup"><span data-stu-id="dcdf5-147">**IWMReaderAdvanced::GetStatistics**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [<span data-ttu-id="dcdf5-148">**Iwmreaderadvanced:: setClientInfo**</span><span class="sxs-lookup"><span data-stu-id="dcdf5-148">**IWMReaderAdvanced::SetClientInfo**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [<span data-ttu-id="dcdf5-149">**IWMReaderAdvanced2:: getbufferprogress**</span><span class="sxs-lookup"><span data-stu-id="dcdf5-149">**IWMReaderAdvanced2::GetBufferProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [<span data-ttu-id="dcdf5-150">**IWMReaderAdvanced2:: getdownloadprogress**</span><span class="sxs-lookup"><span data-stu-id="dcdf5-150">**IWMReaderAdvanced2::GetDownloadProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [<span data-ttu-id="dcdf5-151">**IWMReaderAdvanced2:: getplaymode**</span><span class="sxs-lookup"><span data-stu-id="dcdf5-151">**IWMReaderAdvanced2::GetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [<span data-ttu-id="dcdf5-152">**IWMReaderAdvanced2:: getprotocolname**</span><span class="sxs-lookup"><span data-stu-id="dcdf5-152">**IWMReaderAdvanced2::GetProtocolName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [<span data-ttu-id="dcdf5-153">**IWMReaderAdvanced2:: setlogclientid**</span><span class="sxs-lookup"><span data-stu-id="dcdf5-153">**IWMReaderAdvanced2::SetLogClientID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [<span data-ttu-id="dcdf5-154">**IWMReaderAdvanced2:: setplaymode**</span><span class="sxs-lookup"><span data-stu-id="dcdf5-154">**IWMReaderAdvanced2::SetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a><span data-ttu-id="dcdf5-155">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dcdf5-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dcdf5-156">**DirectShow-qasf-Referenz**</span><span class="sxs-lookup"><span data-stu-id="dcdf5-156">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="dcdf5-157">**Lesen von ASF-Dateien in DirectShow**</span><span class="sxs-lookup"><span data-stu-id="dcdf5-157">**Reading ASF Files in DirectShow**</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




