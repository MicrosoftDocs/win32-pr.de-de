---
description: Unterstützung von ASF in Media Foundation
ms.assetid: 4b0c4a83-623a-4378-9436-35ed120316af
title: Unterstützung von ASF in Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddb7774d0ddaee592cb583ffb771c900642ed216
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106366367"
---
# <a name="asf-support-in-media-foundation"></a><span data-ttu-id="0f952-103">Unterstützung von ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0f952-103">ASF Support in Media Foundation</span></span>

<span data-ttu-id="0f952-104">Media Foundation unterstützt Mediendateien im Advanced Systems-Format (ASF):</span><span class="sxs-lookup"><span data-stu-id="0f952-104">Media Foundation supports media files in the Advanced Systems Format (ASF):</span></span>

-   <span data-ttu-id="0f952-105">Windows Media Video (WMV-Dateien)</span><span class="sxs-lookup"><span data-stu-id="0f952-105">Windows Media Video (WMV files)</span></span>
-   <span data-ttu-id="0f952-106">Windows Media Audio (WMA-Dateien)</span><span class="sxs-lookup"><span data-stu-id="0f952-106">Windows Media Audio (WMA files)</span></span>

<span data-ttu-id="0f952-107">Media Foundation stellt mehrere Objekte zum Lesen und Schreiben von ASF-Dateien bereit.</span><span class="sxs-lookup"><span data-stu-id="0f952-107">Media Foundation provides several objects for reading and writing ASF files.</span></span> <span data-ttu-id="0f952-108">Diese Objekte werden in zwei verschiedenen Architektur Ebenen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="0f952-108">These objects are provided in two different architectural layers.</span></span>

<span data-ttu-id="0f952-109">Zunächst enthält die *Pipeline* Schicht Objekte, die innerhalb der [Media Foundation Pipeline](media-foundation-pipeline.md) funktionieren und den von der Pipeline definierten APIs entsprechen.</span><span class="sxs-lookup"><span data-stu-id="0f952-109">First, the *pipeline* layer contains objects that work inside the [Media Foundation pipeline](media-foundation-pipeline.md) and conform to the APIs defined by the pipeline.</span></span> <span data-ttu-id="0f952-110">Die ASF-Pipeline Ebene enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0f952-110">The ASF pipeline layer contains:</span></span>

-   <span data-ttu-id="0f952-111">[ASF-Medienquelle](asf-media-source.md): analysiert ASF-Dateien und übermittelt die Audiodaten-Datenpakete.</span><span class="sxs-lookup"><span data-stu-id="0f952-111">[ASF Media Source](asf-media-source.md): Parses ASF files and delivers the audio/video data packets.</span></span>
-   <span data-ttu-id="0f952-112">[Windows Media Codecs](windows-media-codecs.md): decodieren oder Codieren von Windows Media-Audiodaten und-Videostreams.</span><span class="sxs-lookup"><span data-stu-id="0f952-112">[Windows Media Codecs](windows-media-codecs.md): Decode or encode Windows Media audio or video streams.</span></span>
-   <span data-ttu-id="0f952-113">[ASF-Medien Senke](asf-media-sinks.md): empfängt Datenpakete und schreibt eine ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="0f952-113">[ASF Media Sink](asf-media-sinks.md): Receives data packets and writes an ASF file.</span></span>

<span data-ttu-id="0f952-114">Zweitens bietet die WM-Container Schicht eine Low-Level-Kontrolle über das Auswerten und Schreiben einer ASF-Datei.</span><span class="sxs-lookup"><span data-stu-id="0f952-114">Second, the WM Container layer provides low-level control over parsing and writing an ASF file.</span></span> <span data-ttu-id="0f952-115">Die Pipeline Schicht verwendet intern wmcontainer.</span><span class="sxs-lookup"><span data-stu-id="0f952-115">The pipeline layer uses WMContainer internally.</span></span> <span data-ttu-id="0f952-116">Anwendungen können auch wmcontainer für die Verwendung von ASF-und Schreib vornissen auf niedriger Ebene verwenden.</span><span class="sxs-lookup"><span data-stu-id="0f952-116">Applications can also use WMContainer for low-level ASF parsing and writing.</span></span>

![Diagramm, das Elemente der Pipeline Schicht und des WM-Containers anzeigt](images/asf-components.png)

## <a name="in-this-section"></a><span data-ttu-id="0f952-118">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0f952-118">In this section</span></span>



| <span data-ttu-id="0f952-119">Thema</span><span class="sxs-lookup"><span data-stu-id="0f952-119">Topic</span></span>                                                                         | <span data-ttu-id="0f952-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f952-120">Description</span></span>                                                                                                        |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f952-121">Struktur der ASF-Datei</span><span class="sxs-lookup"><span data-stu-id="0f952-121">ASF File Structure</span></span>](asf-file-structure.md)<br/>                       | <span data-ttu-id="0f952-122">Übersicht über die Struktur der ASF-Datei und die von Media Foundation bereitgestellten Objekte zum Arbeiten mit ASF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="0f952-122">Overview of the ASF file structure and the objects provided by Media Foundation to work with ASF files.</span></span><br/> |
| [<span data-ttu-id="0f952-123">Komponenten der Pipeline Schicht-ASF</span><span class="sxs-lookup"><span data-stu-id="0f952-123">Pipeline Layer ASF Components</span></span>](pipeline-layer-asf-components.md)<br/> | <span data-ttu-id="0f952-124">Beschreibt das analysieren und Erstellen von ASF-Dateien mithilfe der Pipeline Schicht.</span><span class="sxs-lookup"><span data-stu-id="0f952-124">Describes how to parse and author ASF files using the pipeline layer.</span></span><br/>                                   |
| [<span data-ttu-id="0f952-125">Wmcontainer-ASF-Komponenten</span><span class="sxs-lookup"><span data-stu-id="0f952-125">WMContainer ASF Components</span></span>](wmcontainer-asf-components.md)<br/>       | <span data-ttu-id="0f952-126">Beschreibt das analysieren und Erstellen von ASF-Dateien mithilfe der wmcontainer-Ebene.</span><span class="sxs-lookup"><span data-stu-id="0f952-126">Describes how to parse and author ASF files using the WMContainer layer.</span></span><br/>                                |



 

<span data-ttu-id="0f952-127">Ausführliche Informationen zur Struktur einer ASF-Datei finden Sie in der ASF-Spezifikation, die von dieser [Microsoft-Website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea)heruntergeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="0f952-127">For detailed information about the structure of an ASF file, see the ASF specification, which can be downloaded from this [Microsoft website](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=56de5ee4-51ca-46c6-903b-97390ad14fea).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0f952-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0f952-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f952-129">Media Foundation-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="0f952-129">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 




