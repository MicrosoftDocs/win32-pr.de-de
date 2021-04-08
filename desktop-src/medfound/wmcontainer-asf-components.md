---
description: Die wmcontainer-Objekte bieten eine Low-Level-Kontrolle über das Auswerten und Schreiben einer ASF-Datei (Advanced Systems Format).
ms.assetid: 258ea139-581f-4b94-9655-43ecf1e77f10
title: Wmcontainer-ASF-Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d7d1c1b76683cfe01dc0970ab1c077580215d2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959885"
---
# <a name="wmcontainer-asf-components"></a><span data-ttu-id="2c17f-103">Wmcontainer-ASF-Komponenten</span><span class="sxs-lookup"><span data-stu-id="2c17f-103">WMContainer ASF Components</span></span>

<span data-ttu-id="2c17f-104">Die wmcontainer-Objekte bieten eine Low-Level-Kontrolle über das Auswerten und Schreiben einer ASF-Datei (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="2c17f-104">The WMContainer objects provide low-level control over parsing and writing an Advanced Systems Format (ASF) file.</span></span>

<span data-ttu-id="2c17f-105">In den [ASF-Komponenten der Pipeline Schicht](pipeline-layer-asf-components.md) werden intern die wmcontainer-Objekte verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c17f-105">The [Pipeline Layer ASF Components](pipeline-layer-asf-components.md) use the WMContainer objects internally.</span></span> <span data-ttu-id="2c17f-106">Die meisten Anwendungen sollten die Pipeline Komponenten anstelle von wmcontainer-Objekten verwenden.</span><span class="sxs-lookup"><span data-stu-id="2c17f-106">Most applications should use the pipeline components, rather than using WMContainer objects.</span></span> <span data-ttu-id="2c17f-107">Verwenden Sie wmcontainer nur dann, wenn Sie eine niedrige Kontrolle über das Auswerten und Schreiben einer ASF-Datei benötigen.</span><span class="sxs-lookup"><span data-stu-id="2c17f-107">Use WMContainer only if you require low-level control over parsing and writing an ASF file.</span></span>

<span data-ttu-id="2c17f-108">Die wmcontainer-Ebene enthält die folgenden Objekte:</span><span class="sxs-lookup"><span data-stu-id="2c17f-108">The WMContainer layer includes the following objects:</span></span>

-   [<span data-ttu-id="2c17f-109">ASF-Profil</span><span class="sxs-lookup"><span data-stu-id="2c17f-109">ASF Profile</span></span>](asf-profile.md)
-   [<span data-ttu-id="2c17f-110">ASF-ContentInfo-Objekt</span><span class="sxs-lookup"><span data-stu-id="2c17f-110">ASF ContentInfo Object</span></span>](asf-contentinfo-object.md)
-   [<span data-ttu-id="2c17f-111">ASF-Splitter</span><span class="sxs-lookup"><span data-stu-id="2c17f-111">ASF Splitter</span></span>](asf-splitter.md)
-   [<span data-ttu-id="2c17f-112">ASF Multiplexer</span><span class="sxs-lookup"><span data-stu-id="2c17f-112">ASF Multiplexer</span></span>](asf-multiplexer.md)
-   [<span data-ttu-id="2c17f-113">ASF-Indexer</span><span class="sxs-lookup"><span data-stu-id="2c17f-113">ASF Indexer</span></span>](asf-index-object.md)

<span data-ttu-id="2c17f-114">Die folgenden Themen enthalten Schritt-für-Schritt-Anleitungen zum Verwenden von wmcontainer zum Lesen oder Schreiben von ASF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="2c17f-114">The following topics contain step-by-step instructions about using WMContainer to read or write ASF files.</span></span>

-   [<span data-ttu-id="2c17f-115">Tutorial: Lesen einer ASF-Datei mithilfe von wmcontainer-Objekten</span><span class="sxs-lookup"><span data-stu-id="2c17f-115">Tutorial: Reading an ASF File by Using WMContainer Objects</span></span>](tutorial--reading-an-asf-file.md)
-   [<span data-ttu-id="2c17f-116">Tutorial: Kopieren von ASF-Streams mithilfe von wmcontainer-Objekten</span><span class="sxs-lookup"><span data-stu-id="2c17f-116">Tutorial: Copying ASF Streams by Using WMContainer Objects</span></span>](tutorial--copying-asf-streams-from-one-file-to-another.md)
-   [<span data-ttu-id="2c17f-117">Tutorial: Schreiben einer WMA-Datei mithilfe von wmcontainer-Objekten</span><span class="sxs-lookup"><span data-stu-id="2c17f-117">Tutorial: Writing a WMA File by Using WMContainer Objects</span></span>](tutorial--writing-a-wma-file-by-using-cbr-encoding.md)

## <a name="about-wm-container"></a><span data-ttu-id="2c17f-118">Informationen zum WM-Container</span><span class="sxs-lookup"><span data-stu-id="2c17f-118">About WM Container</span></span>

<span data-ttu-id="2c17f-119">Die wmcontainer-Objekte interagieren direkt mit den ASF-Datei Objekten.</span><span class="sxs-lookup"><span data-stu-id="2c17f-119">The WMContainer objects interact directly with ASF file objects.</span></span> <span data-ttu-id="2c17f-120">Das folgende Diagramm zeigt die Struktur der ASF-Datei und die entsprechenden wmcontainer-Objekte.</span><span class="sxs-lookup"><span data-stu-id="2c17f-120">The following diagram shows the ASF file structure and the corresponding WMContainer objects.</span></span>

![Diagramm mit der ASF-Dateistruktur und den zugehörigen Media Foundation-Objekten](images/asf-components01.png)

<span data-ttu-id="2c17f-122">Mit Ausnahme von Splitter und Multiplexer unterstützt jedes dieser Objekte sowohl das Auswerten (lesen) als auch das Schreiben von ASF-Dateien.</span><span class="sxs-lookup"><span data-stu-id="2c17f-122">Except for the splitter and multiplexer, each of these objects supports both parsing (reading) and writing ASF files.</span></span> <span data-ttu-id="2c17f-123">Der Splitter wird nur zum Lesen von ASF-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c17f-123">The splitter is used only for reading ASF files.</span></span> <span data-ttu-id="2c17f-124">Der Multiplexer wird nur zum Erstellen von neuen ASF-Dateien verwendet.</span><span class="sxs-lookup"><span data-stu-id="2c17f-124">The multiplexer is used only for authoring new ASF files.</span></span>

<span data-ttu-id="2c17f-125">Alle von wmcontainer-Objekten ausgeführten Vorgänge sind synchron, was bedeutet, dass der aufrufende Thread blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="2c17f-125">All operations performed by WMContainer objects are synchronous, meaning they block the calling thread.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c17f-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2c17f-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c17f-127">Unterstützung von ASF in Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2c17f-127">ASF Support in Media Foundation</span></span>](asf-support-in-media-foundation.md)
</dt> </dl>

 

 



