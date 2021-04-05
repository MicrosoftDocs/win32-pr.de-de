---
title: So suchen Sie nach Zeit mithilfe des asynchronen Readers
description: So suchen Sie nach Zeit mithilfe des asynchronen Readers
ms.assetid: 731b0a6e-1472-45a7-998c-e395be86036f
keywords:
- Advanced Systems Format (ASF), Suche nach Zeit
- ASF (Advanced Systems Format), Suche nach Zeit
- Advanced Systems Format (ASF), asynchrone Leser
- ASF (Advanced Systems Format), asynchrone Leser
- asynchrone Leser, suchen nach Zeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f3e24c04d75d762aef6bac498d4b4c8dfa9552
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723565"
---
# <a name="to-seek-by-time-using-the-asynchronous-reader"></a><span data-ttu-id="e7e21-108">So suchen Sie nach Zeit mithilfe des asynchronen Readers</span><span class="sxs-lookup"><span data-stu-id="e7e21-108">To Seek By Time Using the Asynchronous Reader</span></span>

<span data-ttu-id="e7e21-109">Wenn Sie eine bestimmte Präsentationszeit in einer ASF-Datei suchen möchten, muss die Datei ordnungsgemäß konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="e7e21-109">If you want to seek to a specific presentation time in an ASF file, the file must be properly configured.</span></span> <span data-ttu-id="e7e21-110">Standardmäßig können Sie in Audiodateien suchen, Videodateien müssen jedoch vor der Suche indiziert werden.</span><span class="sxs-lookup"><span data-stu-id="e7e21-110">You can seek in audio only files by default, but video files need to be indexed before seeking.</span></span> <span data-ttu-id="e7e21-111">Wenn Sie sich nicht sicher sind, wie eine Datei erstellt wurde, können Sie das Attribut "g \_ wszwmseekable" im Header der Datei durch Aufrufen von " [**iwmheaderinfo:: getattributebyname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname)" überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e7e21-111">If you are not sure about how a file has been created, you can check the g\_wszWMSeekable attribute in the header of the file by calling [**IWMHeaderInfo::GetAttributeByName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-getattributebyname).</span></span>

<span data-ttu-id="e7e21-112">Um mithilfe des asynchronen Readers mithilfe des asynchronen Readers mithilfe des asynchronen Readers nach Daten in einer ASF-Datei zu suchen, nennen Sie [**iwmreader:: Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), und übergeben Sie die gewünschte Zeit und Dauer des Teils der Datei, die Sie als *cnsstart* bzw. *cnsduration* lesen möchten.</span><span class="sxs-lookup"><span data-stu-id="e7e21-112">To seek to data in an ASF file by presentation time using the asynchronous reader, call [**IWMReader::Start**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-start), passing the desired time and duration of the part of the file you want to read as *cnsStart* and *cnsDuration* respectively.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7e21-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e7e21-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7e21-114">**Iwmreader-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e7e21-114">**IWMReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreader)
</dt> <dt>

[<span data-ttu-id="e7e21-115">**Lesen von Dateien mit dem asynchronen Reader**</span><span class="sxs-lookup"><span data-stu-id="e7e21-115">**Reading Files with the Asynchronous Reader**</span></span>](reading-files-with-the-asynchronous-reader.md)
</dt> <dt>

[<span data-ttu-id="e7e21-116">**Lesen von Metadaten bei der Wiedergabe**</span><span class="sxs-lookup"><span data-stu-id="e7e21-116">**Reading Metadata at Playback**</span></span>](reading-metadata-at-playback.md)
</dt> <dt>

[<span data-ttu-id="e7e21-117">**Arbeiten mit Indizes**</span><span class="sxs-lookup"><span data-stu-id="e7e21-117">**Working with Indexes**</span></span>](working-with-indexes.md)
</dt> </dl>

 

 




