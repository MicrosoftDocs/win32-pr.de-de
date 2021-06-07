---
title: WM ASF-Readerfilter (Windows Media Format 11 SDK)
description: Erfahren Sie mehr über den WM ASF-Readerfilter.
ms.assetid: 3d5ca88a-86bd-4d84-b4f4-782564ced58d
keywords:
- Windows Media Format SDK, WM ASF-Reader
- DirectShow, WM ASF Reader
- QASF-Filter, WM ASF-Reader
- WM ASF-Reader
- Advanced Systems Format (ASF), WM ASF Reader
- ASF (Advanced Systems Format), WM ASF Reader
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 421ab634a0d68837b22961b37005c5670d73e5fa
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444281"
---
# <a name="wm-asf-reader-filter-windows-media-format-11-sdk"></a><span data-ttu-id="f8921-109">WM ASF-Readerfilter (Windows Media Format 11 SDK)</span><span class="sxs-lookup"><span data-stu-id="f8921-109">WM ASF Reader Filter (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="f8921-110">Wenn der Name einer ASF-Datei oder einer URL angegeben wird, liest der WM ASF-Reader den komprimierten Inhalt, analysiert die Datenströme und macht für jeden einen Ausgabepin verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f8921-110">When given the name of an ASF file or a URL, the WM ASF Reader reads the compressed content, parses the streams, and exposes an output pin for each one.</span></span> <span data-ttu-id="f8921-111">Dieser Filter stellt eine Downstream-Verbindung mit Windows Media Audio- oder Windows Media Video-DMOs, die die Dekomprimierung anwenden.</span><span class="sxs-lookup"><span data-stu-id="f8921-111">This filter connects downstream to the Windows Media Audio or Windows Media Video DMOs, which do the decompression.</span></span> <span data-ttu-id="f8921-112">Die Suche wird unterstützt, wenn die ASF-Datei durchsuchbar ist.</span><span class="sxs-lookup"><span data-stu-id="f8921-112">Seeking is supported if the ASF file is seekable.</span></span> <span data-ttu-id="f8921-113">Der WM ASF-Reader wendet Zeitstempel auf die Medienbeispiele basierend auf dem Zeitstempel in der ASF-Datei an, ändert die Zeitstempel jedoch in irgendeiner Weise.</span><span class="sxs-lookup"><span data-stu-id="f8921-113">The WM ASF Reader applies time stamps to the media samples based on the time stamp in the ASF file, but it does not modify the time stamps in any way.</span></span> <span data-ttu-id="f8921-114">Intern verwendet der Filter das Windows Media Format-Readerobjekt, um den Windows Media-basierten Inhalt zu lesen.</span><span class="sxs-lookup"><span data-stu-id="f8921-114">Internally, the filter uses the Windows Media Format reader object to read the Windows Media–based content.</span></span>

> [!Note]  
> <span data-ttu-id="f8921-115">Im DirectX SDK ist dieser Filter nicht der Standardquellenfilter für ASF-Dateien, sodass Sie diesen Filter mit diesem SDK nicht mit der **RenderFile-Methode verwenden** können. Sie müssen es dem Filterdiagramm explizit mithilfe seines Klassenbezeichners (CLSID) hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f8921-115">In the DirectX SDK, this filter is not the default source filter for ASF files, so with that SDK you cannot use this filter with the **RenderFile** method; you must explicitly add it to the filter graph by using its class identifier (CLSID).</span></span> <span data-ttu-id="f8921-116">Dieses Verhalten ist beim Windows Media Format SDK anders.</span><span class="sxs-lookup"><span data-stu-id="f8921-116">This behavior is different with the Windows Media Format SDK.</span></span> <span data-ttu-id="f8921-117">Wenn Sie die Runtimebibliotheken des Windows Media Format SDK installieren, wird der WM ASF-Reader als Standardfilter für ASF-Dateien registriert.</span><span class="sxs-lookup"><span data-stu-id="f8921-117">When you install the Windows Media Format SDK runtime libraries, the WM ASF Reader is registered as the default filter for ASF files.</span></span>

 

<span data-ttu-id="f8921-118">Die folgende Tabelle enthält Informationen zum WM ASF-Readerfilter, z. B. die unterstützten Schnittstellen und Medientypen.</span><span class="sxs-lookup"><span data-stu-id="f8921-118">The following table contains information about the WM ASF Reader filter, such as the interfaces and media types it supports.</span></span>



|  <span data-ttu-id="f8921-119">Filterinformationen</span><span class="sxs-lookup"><span data-stu-id="f8921-119">Filter Information</span></span>                      |  <span data-ttu-id="f8921-120">Typen</span><span class="sxs-lookup"><span data-stu-id="f8921-120">Types</span></span>                                                                                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8921-121">Filtern von Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f8921-121">Filter interfaces</span></span>      | <span data-ttu-id="f8921-122">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (teilweise implementiert.</span><span class="sxs-lookup"><span data-stu-id="f8921-122">**IBaseFilter**, **IFileSourceFilter**, **IServiceProvider**, **IWMHeaderInfo**, **IWMReaderAdvanced** (partially implemented.</span></span> <span data-ttu-id="f8921-123">Siehe Hinweise.), **IWMReaderAdvanced2** (teilweise implementiert), **IWMDRMReader** (über **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="f8921-123">See Remarks.), **IWMReaderAdvanced2** (partially implemented), **IWMDRMReader** (through **IServiceProvider**)</span></span> |
| <span data-ttu-id="f8921-124">Eingabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="f8921-124">Input pin media types</span></span>  | <span data-ttu-id="f8921-125">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f8921-125">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="f8921-126">Eingabepinschnittstellen</span><span class="sxs-lookup"><span data-stu-id="f8921-126">Input pin interfaces</span></span>   | <span data-ttu-id="f8921-127">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="f8921-127">Not applicable</span></span>                                                                                                                                                                                                                                |
| <span data-ttu-id="f8921-128">Ausgabepin-Medientypen</span><span class="sxs-lookup"><span data-stu-id="f8921-128">Output pin media types</span></span> | <span data-ttu-id="f8921-129">MEDIATYPE \_ Video, MEDIATYPE \_ Audio, MEDIATYPE \_ ScriptCommand, MEDIATYPE \_ FileTransfer</span><span class="sxs-lookup"><span data-stu-id="f8921-129">MEDIATYPE\_Video, MEDIATYPE\_Audio, MEDIATYPE\_ScriptCommand, MEDIATYPE\_FileTransfer</span></span>                                                                                                                                                         |
| <span data-ttu-id="f8921-130">Formattyp</span><span class="sxs-lookup"><span data-stu-id="f8921-130">Format type</span></span>            | <span data-ttu-id="f8921-131">**VIDEOINFOHEADER2,** wenn der Inhalt mit [*Einem Interlacing verkettet ist,*](wmformat-glossary.md) **andernfalls VIDEOINFOHEADER**</span><span class="sxs-lookup"><span data-stu-id="f8921-131">**VIDEOINFOHEADER2** if content is [*interlaced*](wmformat-glossary.md), otherwise **VIDEOINFOHEADER**</span></span>                                                                                                                    |
| <span data-ttu-id="f8921-132">Schnittstellen für Ausgabepins</span><span class="sxs-lookup"><span data-stu-id="f8921-132">Output pin interfaces</span></span>  | <span data-ttu-id="f8921-133">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (über **IServiceProvider**)</span><span class="sxs-lookup"><span data-stu-id="f8921-133">**IMediaSeeking**, **IAMWMBufferPass**, **IServiceProvider**, **IWMStreamConfig2** (through **IServiceProvider**)</span></span>                                                                                                                             |
| <span data-ttu-id="f8921-134">Filtern der CLSID</span><span class="sxs-lookup"><span data-stu-id="f8921-134">Filter CLSID</span></span>           | <span data-ttu-id="f8921-135">CLSID \_ WMAsfReader</span><span class="sxs-lookup"><span data-stu-id="f8921-135">CLSID\_WMAsfReader</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="f8921-136">Eigenschaftenseite CLSID</span><span class="sxs-lookup"><span data-stu-id="f8921-136">Property Page CLSID</span></span>    | <span data-ttu-id="f8921-137">Keine Eigenschaftenseite</span><span class="sxs-lookup"><span data-stu-id="f8921-137">No property page</span></span>                                                                                                                                                                                                                              |
| <span data-ttu-id="f8921-138">Ausführbare Datei</span><span class="sxs-lookup"><span data-stu-id="f8921-138">Executable</span></span>             | <span data-ttu-id="f8921-139">Qasf.dll</span><span class="sxs-lookup"><span data-stu-id="f8921-139">Qasf.dll</span></span>                                                                                                                                                                                                                                      |
| <span data-ttu-id="f8921-140">Verdienst</span><span class="sxs-lookup"><span data-stu-id="f8921-140">Merit</span></span>                  | <span data-ttu-id="f8921-141">WAHRSCHEINLICHKEIT \_ UNWAHRSCHEINLICH</span><span class="sxs-lookup"><span data-stu-id="f8921-141">MERIT\_UNLIKELY</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="f8921-142">Filterkategorie</span><span class="sxs-lookup"><span data-stu-id="f8921-142">Filter Category</span></span>        | <span data-ttu-id="f8921-143">CLSID \_ LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="f8921-143">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="f8921-144">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f8921-144">Remarks</span></span>

<span data-ttu-id="f8921-145">Der WM ASF-Reader implementiert teilweise die **Schnittstellen IWMReaderAdvanced** und **IWMReaderAdvanced2,** um Anwendungen Zugriff auf die Informationsmethoden auf dem Readerobjekt zu geben.</span><span class="sxs-lookup"><span data-stu-id="f8921-145">The WM ASF Reader partially implements the **IWMReaderAdvanced** and **IWMReaderAdvanced2** interfaces in order to give applications access to the informational methods on the reader object.</span></span> <span data-ttu-id="f8921-146">Die Implementierung des Filters übergibt die Aufrufe einfach an die -Schnittstelle des Readerobjekts.</span><span class="sxs-lookup"><span data-stu-id="f8921-146">The filter's implementation simply passes the calls through to the interface on the reader object.</span></span> <span data-ttu-id="f8921-147">Die Streamingmethoden werden nicht implementiert, da der Filter die vollständige Kontrolle über den Streamingprozess haben muss.</span><span class="sxs-lookup"><span data-stu-id="f8921-147">The streaming methods are not implemented because the filter must have complete control over the streaming process.</span></span> <span data-ttu-id="f8921-148">Die folgenden **IWMReaderAdvanced-** und **IWMReaderAdvanced2-Methoden** werden implementiert:</span><span class="sxs-lookup"><span data-stu-id="f8921-148">The following **IWMReaderAdvanced** and **IWMReaderAdvanced2** methods are implemented:</span></span>

-   [<span data-ttu-id="f8921-149">**IWMReaderAdvanced::GetStatistics**</span><span class="sxs-lookup"><span data-stu-id="f8921-149">**IWMReaderAdvanced::GetStatistics**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-getstatistics)
-   [<span data-ttu-id="f8921-150">**IWMReaderAdvanced::SetClientInfo**</span><span class="sxs-lookup"><span data-stu-id="f8921-150">**IWMReaderAdvanced::SetClientInfo**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced-setclientinfo)
-   [<span data-ttu-id="f8921-151">**IWMReaderAdvanced2::GetBufferProgress**</span><span class="sxs-lookup"><span data-stu-id="f8921-151">**IWMReaderAdvanced2::GetBufferProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getbufferprogress)
-   [<span data-ttu-id="f8921-152">**IWMReaderAdvanced2::GetDownloadProgress**</span><span class="sxs-lookup"><span data-stu-id="f8921-152">**IWMReaderAdvanced2::GetDownloadProgress**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getdownloadprogress)
-   [<span data-ttu-id="f8921-153">**IWMReaderAdvanced2::GetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="f8921-153">**IWMReaderAdvanced2::GetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getplaymode)
-   [<span data-ttu-id="f8921-154">**IWMReaderAdvanced2::GetProtocolName**</span><span class="sxs-lookup"><span data-stu-id="f8921-154">**IWMReaderAdvanced2::GetProtocolName**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-getprotocolname)
-   [<span data-ttu-id="f8921-155">**IWMReaderAdvanced2::SetLogClientID**</span><span class="sxs-lookup"><span data-stu-id="f8921-155">**IWMReaderAdvanced2::SetLogClientID**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setlogclientid)
-   [<span data-ttu-id="f8921-156">**IWMReaderAdvanced2::SetPlayMode**</span><span class="sxs-lookup"><span data-stu-id="f8921-156">**IWMReaderAdvanced2::SetPlayMode**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setplaymode)

## <a name="related-topics"></a><span data-ttu-id="f8921-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f8921-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8921-158">**DirectShow QASF-Referenz**</span><span class="sxs-lookup"><span data-stu-id="f8921-158">**DirectShow QASF Reference**</span></span>](directshow-qasf-reference.md)
</dt> <dt>

[<span data-ttu-id="f8921-159">**Lesen von ASF-Dateien in DirectShow**</span><span class="sxs-lookup"><span data-stu-id="f8921-159">**Reading ASF Files in DirectShow**</span></span>](reading-asf-files-in-directshow.md)
</dt> </dl>

 

 




