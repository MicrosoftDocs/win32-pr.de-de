---
title: Erstellen von Filter Diagrammen zum Schreiben von ASF-Dateien (qasf)
description: Erstellen von Filter Diagrammen zum Schreiben von ASF-Dateien (qasf)
ms.assetid: 45583c97-4e59-4a6a-987b-5486e6f33990
keywords:
- Windows Media-Format-SDK, Bausteine von Filter Diagrammen (qasf)
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, Schreiben von ASF-Dateien (qasf)
- Advanced Systems Format (ASF), Bausteine von Filter Diagrammen (qasf)
- ASF (Advanced Systems Format), Bausteine von Filter Diagrammen (qasf)
- Advanced Systems Format (ASF), schreiben (qasf)
- ASF (Advanced Systems Format), schreiben (qasf)
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, Bausteine von Filter Diagrammen (qasf)
- DirectShow, Schreiben von ASF-Dateien (qasf)
- Windows Media-Format-SDK, qasf
- Advanced Systems Format (ASF), qasf
- ASF (Advanced Systems Format), qasf
- DirectShow, qasf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbf0a261d1502f76cebc0eb2141cd230c509029
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337962"
---
# <a name="building-filter-graphs-to-write-asf-files-qasf"></a><span data-ttu-id="c8571-118">Erstellen von Filter Diagrammen zum Schreiben von ASF-Dateien (qasf)</span><span class="sxs-lookup"><span data-stu-id="c8571-118">Building Filter Graphs to Write ASF Files (QASF)</span></span>

<span data-ttu-id="c8571-119">Anwendungen, die auf DirectShow basieren, verwenden in der Regel einen von drei grundlegenden Arten von Filter Diagrammen, wenn Sie Windows Media – basierten Inhalt erstellen:</span><span class="sxs-lookup"><span data-stu-id="c8571-119">Applications based on DirectShow typically use one of three basic types of filter graphs when creating Windows Media–based content:</span></span>

-   <span data-ttu-id="c8571-120">Filtern Sie Diagramme zum Umwandeln oder transcodieren von Inhalten aus einem anderen Format in das Windows Media-Format.</span><span class="sxs-lookup"><span data-stu-id="c8571-120">Filter graphs for converting or transcoding content from some other format into Windows Media Format.</span></span>
-   <span data-ttu-id="c8571-121">Filtern Sie Diagramme für das Einfügen von Inhalten, die nicht auf Windows-Medien basierende (Native Streamformate) sind, in ASF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="c8571-121">Filter graphs for inserting content that is not Windows Media-based (native stream formats) into ASF files.</span></span>
-   <span data-ttu-id="c8571-122">Filtern Sie Diagramme, um Livedaten zu erfassen und direkt in das Windows Media-Format zu codieren, bevor Sie Sie auf einem Datenträger</span><span class="sxs-lookup"><span data-stu-id="c8571-122">Filter graphs for capturing live data and encoding it immediately into Windows Media Format before saving it to disk.</span></span>

<span data-ttu-id="c8571-123">Jeder Filter Diagrammtyp wird in den folgenden Abschnitten ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c8571-123">Each type of filter graph is described in more detail in the following sections.</span></span>



| <span data-ttu-id="c8571-124">`Section`</span><span class="sxs-lookup"><span data-stu-id="c8571-124">Section</span></span>                                                                                                             | <span data-ttu-id="c8571-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c8571-125">Description</span></span>                                                                                           |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c8571-126">Transcoding-Dateien (qasf)</span><span class="sxs-lookup"><span data-stu-id="c8571-126">Transcoding Files (QASF)</span></span>](transcoding-files--qasf.md)                                                             | <span data-ttu-id="c8571-127">Beschreibt, wie Datei-transcodierungsfilterdiagramme erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="c8571-127">Describes how to create file-transcoding filter graphs.</span></span>                                               |
| [<span data-ttu-id="c8571-128">Einfügen von nativen streamformaten in ASF-Dateien (qasf)</span><span class="sxs-lookup"><span data-stu-id="c8571-128">Inserting Native Stream Formats Into ASF Files (QASF)</span></span>](inserting-native-stream-formats-into-asf-files--qasf.md)   | <span data-ttu-id="c8571-129">Beschreibt, wie jeder Typ von komprimierten oder nicht komprimierten Audiodaten oder Videodaten in eine ASF-Datei platziert wird.</span><span class="sxs-lookup"><span data-stu-id="c8571-129">Describes how to place any type of compressed or non-compressed audio or video data into an ASF file.</span></span> |
| [<span data-ttu-id="c8571-130">Direkte Erfassung von einem Gerät in eine ASF-Datei (qasf)</span><span class="sxs-lookup"><span data-stu-id="c8571-130">Capturing Directly from a Device to an ASF File (QASF)</span></span>](capturing-directly-from-a-device-to-an-asf-file--qasf.md) | <span data-ttu-id="c8571-131">Beschreibt das Erstellen von Erfassungs Filter Diagrammen, die an eine ASF-Datei ausgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c8571-131">Describes how to create capture filter graphs that output to an ASF file.</span></span>                             |



 

 

 




