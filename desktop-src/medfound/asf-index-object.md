---
description: ASF-Indexer
ms.assetid: 3f95b0ac-d70f-4bc2-8524-c7de1df34afa
title: ASF-Indexer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c729b547339149ee578a90283c570ec8460b0c57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338945"
---
# <a name="asf-indexer"></a><span data-ttu-id="33440-103">ASF-Indexer</span><span class="sxs-lookup"><span data-stu-id="33440-103">ASF Indexer</span></span>

<span data-ttu-id="33440-104">Der ASF- *Indexer* ist eine wmcontainer-Ebenenkomponente, die verwendet wird, um Index Objekte in einer ASF-Datei (Advanced Systems Format) zu lesen oder zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="33440-104">The ASF *indexer* is a WMContainer layer component that is used to read or write Index Objects in an Advanced Systems Format (ASF) file.</span></span> <span data-ttu-id="33440-105">Weitere Informationen zur Struktur einer ASF-Datei finden Sie unter [Struktur der ASF-Datei](asf-file-structure.md).</span><span class="sxs-lookup"><span data-stu-id="33440-105">For information about the structure of an ASF file, see [ASF File Structure](asf-file-structure.md).</span></span>

<span data-ttu-id="33440-106">Eine Anwendung kann den Indexer verwenden, um Suchvorgänge auf der Grundlage der Präsentationszeit auszuführen oder um neue Indexeinträge für eine ASF-Datei zu generieren.</span><span class="sxs-lookup"><span data-stu-id="33440-106">An application can use the indexer to perform seeking based on presentation time or to generate new index entries for an ASF file.</span></span> <span data-ttu-id="33440-107">Der ASF-Indexer implementiert die [**imfasfindexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="33440-107">The ASF indexer implements the [**IMFASFIndexer**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) interface.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="33440-108">Indextyp</span><span class="sxs-lookup"><span data-stu-id="33440-108">Index type</span></span></th>
<th><span data-ttu-id="33440-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33440-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33440-110">Präsentationszeit basierter Index</span><span class="sxs-lookup"><span data-stu-id="33440-110">Presentation time-based Index</span></span></td>
<td><span data-ttu-id="33440-111">Stellt die Präsentationszeit basierte Indizierung für Audiodaten und Videostreams in Indexblöcken bereit, um die Indizierung zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="33440-111">Provides presentation time-based indexing for audio and video streams in index blocks to make indexing more space efficient.</span></span> <span data-ttu-id="33440-112">Jeder Indexblock verweist auf Indexeinträge, die einen Byte Offset enthalten.</span><span class="sxs-lookup"><span data-stu-id="33440-112">Each index block references index entries that contain a byte offset.</span></span> <br/> <span data-ttu-id="33440-113">Der Offset ist die Position des Datenpakets, das Seeding ist, relativ zum Anfang des ASF-Datenobjekts.</span><span class="sxs-lookup"><span data-stu-id="33440-113">The offset is the position of the data packet being seeked, relative to the start of the ASF Data Object.</span></span><br/> <span data-ttu-id="33440-114">GUID_NULL muss als GUID-Typ für den Index Bezeichner verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="33440-114">GUID_NULL must be used as the GUID type for the index identifier.</span></span> <span data-ttu-id="33440-115">Weitere Informationen finden Sie unter. Weitere Informationen finden <a href="using-the-indexer-to-write-a-new-index.md">Sie unter Verwenden des Indexers zum Schreiben eines neuen Indexes</a>.</span><span class="sxs-lookup"><span data-stu-id="33440-115">For more information; see <a href="using-the-indexer-to-write-a-new-index.md">Using the Indexer to Write a New Index</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33440-116">Timecode-Index</span><span class="sxs-lookup"><span data-stu-id="33440-116">Timecode Index</span></span></td>
<td><span data-ttu-id="33440-117">Ermöglicht das Suchen nach Zeitcode in Streams, die Zeitcode-Metadaten enthalten.</span><span class="sxs-lookup"><span data-stu-id="33440-117">Facilitates seeking by timecode in streams which contain timecode metadata.</span></span> <span data-ttu-id="33440-118">Die Timecodes entsprechen einem SMPTE-Format (<em>Stunden: Minuten: Sekunden: Frames</em>).</span><span class="sxs-lookup"><span data-stu-id="33440-118">The timecodes conform to a SMPTE format (<em>Hours:Minutes:Seconds:Frames</em>).</span></span> <span data-ttu-id="33440-119">Jeder Indexblock verweist auf Indexeinträge, die einen Byte Offset enthalten.</span><span class="sxs-lookup"><span data-stu-id="33440-119">Each index block references index entries that contain a byte offset.</span></span> <br/> <span data-ttu-id="33440-120">Der Offset ist die Position des Datenpakets, das Seeding ist, relativ zum Anfang des ASF-Datenobjekts.</span><span class="sxs-lookup"><span data-stu-id="33440-120">The offset is the position of the data packet being seeked, relative to the start of the ASF Data Object.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="33440-121">Timecode-Index Objekte werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="33440-121">Timecode index objects are not currently supported.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33440-122">Frame basierter Index</span><span class="sxs-lookup"><span data-stu-id="33440-122">Frame-based Index</span></span></td>
<td><span data-ttu-id="33440-123">Stellt eine Frame basierte Indizierung für Videostreams bereit.</span><span class="sxs-lookup"><span data-stu-id="33440-123">Provides frame-based indexing for video streams.</span></span> <span data-ttu-id="33440-124">Indizes in den Frame basierten Index entsprechen Frame Nummern, wobei der erste Frame für einen Datenstrom in der ASF-Datei dem Eintrag 0 im Frame basierten Index Objekt entspricht.</span><span class="sxs-lookup"><span data-stu-id="33440-124">Indexes into the frame-based index are in terms of frame numbers, with the first frame for a stream in the ASF file corresponding to entry 0 in the frame-based index object.</span></span> <span data-ttu-id="33440-125">Jeder Indexblock verweist auf Indexeinträge, die einen Byte Offset enthalten.</span><span class="sxs-lookup"><span data-stu-id="33440-125">Each index block references index entries that contain a byte offset.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="33440-126">Frame basierte Index Objekte werden zurzeit nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="33440-126">Frame-based index objects are not currently supported.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="33440-127">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="33440-127">This section contains the following topics.</span></span>



| <span data-ttu-id="33440-128">Thema</span><span class="sxs-lookup"><span data-stu-id="33440-128">Topic</span></span>                                                                                | <span data-ttu-id="33440-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="33440-129">Description</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="33440-130">Erstellung und Konfiguration von Indexern</span><span class="sxs-lookup"><span data-stu-id="33440-130">Indexer Creation and Configuration</span></span>](indexer-creation-and-configuration.md)         | <span data-ttu-id="33440-131">So erstellen Sie ein Indexer-Objekt und konfigurieren es für das Lesen eines vorhandenen Indexes oder das Schreiben eines neuen ASF-Index Objekts für eine Datei.</span><span class="sxs-lookup"><span data-stu-id="33440-131">How to create an indexer object and configure it for reading an existing index or for writing a new ASF Index Object for a file.</span></span> |
| [<span data-ttu-id="33440-132">Verwenden des Indexers zum Suchen in einer Datei</span><span class="sxs-lookup"><span data-stu-id="33440-132">Using the Indexer to Seek in a File</span></span>](using-the-indexer-to-seek.md)                 | <span data-ttu-id="33440-133">Verwenden des Indexers, um in einer ASF-Datei zu suchen.</span><span class="sxs-lookup"><span data-stu-id="33440-133">How to use the indexer to seek within an ASF file.</span></span>                                                                               |
| [<span data-ttu-id="33440-134">Verwenden des Indexers zum Schreiben eines neuen Indexes</span><span class="sxs-lookup"><span data-stu-id="33440-134">Using the Indexer to Write a New Index</span></span>](using-the-indexer-to-write-a-new-index.md) | <span data-ttu-id="33440-135">Verwenden des Indexers, um Indexeinträge zu generieren und ein neues Index Objekt für eine ASF-Datei zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="33440-135">How to use the indexer to generate index entries and write a new Index Object for an ASF file.</span></span>                                   |



 

## <a name="related-topics"></a><span data-ttu-id="33440-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="33440-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="33440-137">Wmcontainer-ASF-Komponenten</span><span class="sxs-lookup"><span data-stu-id="33440-137">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)
</dt> <dt>

[<span data-ttu-id="33440-138">Unterstützung von ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="33440-138">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 




