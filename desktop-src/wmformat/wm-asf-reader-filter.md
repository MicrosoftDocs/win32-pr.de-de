---
title: WM ASF-Readerfilter (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über den WM ASF Reader-Filter für das Windows Media Format 11 SDK. Überprüfen Sie die Filterinformationen, und sehen Sie sich verwandte Themen an.
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK, WM ASF Reader
- DirectShow,WM ASF Reader
- QASF-Filter, WM ASF-Reader
- WM ASF Reader
- Advanced Systems Format (ASF), WM ASF Reader
- ASF (Advanced Systems Format), WM ASF Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26bde36b1b2cfa7644d6e75d8d1ff96260b2e457
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119645"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a><span data-ttu-id="12f90-110">WM ASF-Readerfilter (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="12f90-110">WM ASF Reader Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="12f90-111">Wenn der Name einer ASF-Datei oder einer URL angegeben wird, liest der WM ASF-Reader den komprimierten Inhalt, analysiert die Streams und macht einen Ausgabepin für jeden verfügbar.</span><span class="sxs-lookup"><span data-stu-id="12f90-111">When given the name of an ASF file or a URL, the WM ASF Reader reads the compressed content, parses the streams, and exposes an output pin for each one.</span></span> <span data-ttu-id="12f90-112">Dieser Filter stellt eine Downstreamverbindung mit den Windows Media Audio oder Windows Media Video DMOs her, die die Dekomprimierung durchführen.</span><span class="sxs-lookup"><span data-stu-id="12f90-112">This filter connects downstream to the Windows Media Audio or Windows Media Video DMOs, which do the decompression.</span></span> <span data-ttu-id="12f90-113">Suchen wird unterstützt, wenn die ASF-Datei gesucht werden kann.</span><span class="sxs-lookup"><span data-stu-id="12f90-113">Seeking is supported if the ASF file is seekable.</span></span> <span data-ttu-id="12f90-114">Der WM ASF-Reader wendet Zeitstempel auf die Medienbeispiele basierend auf dem Zeitstempel in der ASF-Datei an, ändert die Zeitstempel jedoch in keiner Weise.</span><span class="sxs-lookup"><span data-stu-id="12f90-114">The WM ASF Reader applies time stamps to the media samples based on the time stamp in the ASF file, but it does not modify the time stamps in any way.</span></span> <span data-ttu-id="12f90-115">Intern verwendet der Filter das Windows Media Format-Readerobjekt, um den Windows Media-basierten Inhalt zu lesen.</span><span class="sxs-lookup"><span data-stu-id="12f90-115">Internally, the filter uses the Windows Media Format reader object to read the Windows Media–based content.</span></span>

> [!Note]  
> <span data-ttu-id="12f90-116">Im DirectX SDK ist dieser Filter nicht der Standardquellfilter für ASF-Dateien, sodass Sie mit diesem SDK diesen Filter nicht mit der **RenderFile-Methode** verwenden können. Sie müssen es dem Filterdiagramm explizit mithilfe seines Klassenbezeichners (CLSID) hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="12f90-116">In the DirectX SDK, this filter is not the default source filter for ASF files, so with that SDK you cannot use this filter with the **RenderFile** method; you must explicitly add it to the filter graph by using its class identifier (CLSID).</span></span> <span data-ttu-id="12f90-117">Dieses Verhalten unterscheidet sich vom Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="12f90-117">This behavior is different with the Windows Media Format SDK.</span></span> <span data-ttu-id="12f90-118">Wenn Sie die Runtimebibliotheken des Windows Media Format SDK installieren, wird der WM ASF Reader als Standardfilter für ASF-Dateien registriert.</span><span class="sxs-lookup"><span data-stu-id="12f90-118">When you install the Windows Media Format SDK runtime libraries, the WM ASF Reader is registered as the default filter for ASF files.</span></span>

 

<span data-ttu-id="12f90-119">Die folgende Tabelle enthält Informationen zum WM ASF-Readerfilter, z. B. die unterstützten Schnittstellen und Medientypen.</span><span class="sxs-lookup"><span data-stu-id="12f90-119">The following table contains information about the WM ASF Reader filter, such as the interfaces and media types it supports.</span></span>



|  <span data-ttu-id="12f90-120">Filterinformationen</span><span class="sxs-lookup"><span data-stu-id="12f90-120">Filter Information</span></span>                      |  <span data-ttu-id="12f90-121">Typen</span><span class="sxs-lookup"><span data-stu-id="12f90-121">Types</span></span>                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12f90-122">Filterschnittstellen</span><span class="sxs-lookup"><span data-stu-id="12f90-122">Filter interfaces</span></span>      | <span data-ttu-id="12f90-123">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (teilweise implementiert.</span><span class="sxs-lookup"><span data-stu-id="12f90-123">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (partially implemented.</span></span> <span data-ttu-id="12f90-124">Siehe Hinweise.), **IWMReaderAdvanced2** (teilweise implementiert), **IWMDRMReader** (über **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="12f90-124">See Remarks.), **IWMReaderAdvanced2** (partially implemented), **IWMDRMReader** (through **IServiceProvider**)</span></span> |
| <span data-ttu-id="12f90-125">Eingabepinmedientypen</span><span class="sxs-lookup"><span data-stu-id="12f90-125">Input pin media types</span></span>  | <span data-ttu-id="12f90-126">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="12f90-126">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="12f90-127">Eingabepinschnittstellen</span><span class="sxs-lookup"><span data-stu-id="12f90-127">Input pin interfaces</span></span>   | <span data-ttu-id="12f90-128">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="12f90-128">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="12f90-129">Medientypen des Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="12f90-129">Output pin media types</span></span> | <span data-ttu-id="12f90-130">MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer</span><span class="sxs-lookup"><span data-stu-id="12f90-130">MEDIATYPE\_Video, MEDIATYPE\_Audio, MEDIATYPE\_ScriptCommand, MEDIATYPE\_FileTransfer</span></span>                                                                                                                                                         |
| <span data-ttu-id="12f90-131">Formattyp</span><span class="sxs-lookup"><span data-stu-id="12f90-131">Format type</span></span>            | <span data-ttu-id="12f90-132">**VIDEOINFOHEADER2,** wenn inhalt [*mit einem Zeilensprung verknüpft*](wmformat-glossary.md)ist, **andernfalls VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="12f90-132">**VIDEOINFOHEADER2** if content is [*interlaced*](wmformat-glossary.md), otherwise **VIDEOINFOHEADER**</span></span>                                                                                                                    |
| <span data-ttu-id="12f90-133">Ausgabepinschnittstellen</span><span class="sxs-lookup"><span data-stu-id="12f90-133">Output pin interfaces</span></span>  | <span data-ttu-id="12f90-134">**IMediaSeeking,** **IAMWMBufferPass,** **IServiceProvider,** **IWMStreamConfig2** (über **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="12f90-134">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                                                                             |
| <span data-ttu-id="12f90-135">Filtern von CLSID</span><span class="sxs-lookup"><span data-stu-id="12f90-135">Filter CLSID</span></span>           | <span data-ttu-id="12f90-136">CLSID \_ WMAsfReader</span><span class="sxs-lookup"><span data-stu-id="12f90-136">CLSID\_WMAsfReader</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="12f90-137">CLSID der Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="12f90-137">Property Page CLSID</span></span>    | <span data-ttu-id="12f90-138">Keine Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="12f90-138">No property page</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="12f90-139">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="12f90-139">Executable</span></span>             | <span data-ttu-id="12f90-140">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="12f90-140">Qasf.dll</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="12f90-141">Verdienst</span><span class="sxs-lookup"><span data-stu-id="12f90-141">Merit</span></span>                  | <span data-ttu-id="12f90-142">\_UNWAHRSCHEINLICHE WAHRSCHEINLICHKEIT</span><span class="sxs-lookup"><span data-stu-id="12f90-142">MERIT\_UNLIKELY</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="12f90-143">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="12f90-143">Filter Category</span></span>        | <span data-ttu-id="12f90-144">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="12f90-144">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="12f90-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12f90-145">Remarks</span></span>

<span data-ttu-id="12f90-146">Der WM ASF-Reader implementiert teilweise die Schnittstellen **IWMReaderAdvanced** und **IWMReaderAdvanced2,** um Anwendungen Zugriff auf die Informationsmethoden für das Readerobjekt zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="12f90-146">The WM ASF Reader partially implements the **IWMReaderAdvanced** and **IWMReaderAdvanced2** interfaces in order to give applications access to the informational methods on the reader object.</span></span> <span data-ttu-id="12f90-147">Die Implementierung des Filters übergibt einfach die Aufrufe an die Schnittstelle des Readerobjekts.</span><span class="sxs-lookup"><span data-stu-id="12f90-147">The filter's implementation simply passes the calls through to the interface on the reader object.</span></span> <span data-ttu-id="12f90-148">Die Streamingmethoden werden nicht implementiert, da der Filter die vollständige Kontrolle über den Streamingprozess haben muss.</span><span class="sxs-lookup"><span data-stu-id="12f90-148">The streaming methods are not implemented because the filter must have complete control over the streaming process.</span></span> <span data-ttu-id="12f90-149">Die folgenden **IWMReaderAdvanced-** und **IWMReaderAdvanced2-Methoden** werden implementiert:</span><span class="sxs-lookup"><span data-stu-id="12f90-149">The following **IWMReaderAdvanced** and **IWMReaderAdvanced2** methods are implemented:</span></span>

-   [<span data-ttu-id="12f90-150">**IWMReaderAdvanced::GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="12f90-150">**IWMReaderAdvanced::GetStatistics**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [<span data-ttu-id="12f90-151">**IWMReaderAdvanced::SetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="12f90-151">**IWMReaderAdvanced::SetClientInfo**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [<span data-ttu-id="12f90-152">**IWMReaderAdvanced2::GetBufferProgress**</span><span class="sxs-lookup"><span data-stu-id="12f90-152">**IWMReaderAdvanced2::GetBufferProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [<span data-ttu-id="12f90-153">**IWMReaderAdvanced2::GetDownloadProgress**</span><span class="sxs-lookup"><span data-stu-id="12f90-153">**IWMReaderAdvanced2::GetDownloadProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [<span data-ttu-id="12f90-154">**IWMReaderAdvanced2::GetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="12f90-154">**IWMReaderAdvanced2::GetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [<span data-ttu-id="12f90-155">**IWMReaderAdvanced2::GetProtocolName**</span><span class="sxs-lookup"><span data-stu-id="12f90-155">**IWMReaderAdvanced2::GetProtocolName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [<span data-ttu-id="12f90-156">**IWMReaderAdvanced2::SetLogClientID**</span><span class="sxs-lookup"><span data-stu-id="12f90-156">**IWMReaderAdvanced2::SetLogClientID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [<span data-ttu-id="12f90-157">**IWMReaderAdvanced2::SetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="12f90-157">**IWMReaderAdvanced2::SetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a><span data-ttu-id="12f90-158">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="12f90-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12f90-159">**DirectShow-QASF-Referenz**</span><span class="sxs-lookup"><span data-stu-id="12f90-159">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="12f90-160">**Lesen von ASF-Dateien in DirectShow**</span><span class="sxs-lookup"><span data-stu-id="12f90-160">**Reading ASF Files in DirectShow**</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




