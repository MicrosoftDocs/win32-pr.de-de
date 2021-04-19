---
description: Informationen zu Medien Beispielen und-Zuweisungen
ms.assetid: d6283bf0-0460-4519-9a56-fd4c78cfaabc
title: Informationen zu Medien Beispielen und-Zuweisungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9105228e70f82aaa7c36b7e7d28cf7e748e1e2f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106357146"
---
# <a name="about-media-samples-and-allocators"></a><span data-ttu-id="eb2d9-103">Informationen zu Medien Beispielen und-Zuweisungen</span><span class="sxs-lookup"><span data-stu-id="eb2d9-103">About Media Samples and Allocators</span></span>

<span data-ttu-id="eb2d9-104">Filter übermitteln Daten über PIN-Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-104">Filters deliver data across pin connections.</span></span> <span data-ttu-id="eb2d9-105">Daten werden von der Ausgabe-PIN eines Filters zur Eingabe-PIN eines anderen Filters verschoben.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-105">Data moves from the output pin of one filter to the input pin of another filter.</span></span> <span data-ttu-id="eb2d9-106">Die häufigste Methode für die Bereitstellung der Daten durch den Ausgabepin besteht darin, dass die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode für die Eingabe aufgerufen wird, obwohl auch einige andere Mechanismen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-106">The most common way for the output pin to deliver the data is by calling the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the input, although a few other mechanisms exist as well.</span></span>

<span data-ttu-id="eb2d9-107">Abhängig vom Filter kann der Arbeitsspeicher für die Mediendaten auf verschiedene Arten zugewiesen werden: auf dem Heap, in einer DirectDraw-Oberfläche, mithilfe von frei gegebenem GDI-Speicher oder mit einem anderen Zuordnungs Mechanismus.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-107">Depending on the filter, memory for the media data can be allocated in various ways: on the heap, in a DirectDraw surface, using shared GDI memory, or using some other allocation mechanism.</span></span> <span data-ttu-id="eb2d9-108">Das für die Zuordnung des Arbeitsspeichers verantwortliche Objekt wird *als Zuweisung bezeichnet*. Hierbei handelt es sich um ein COM-Objekt, das die [**imembelegcator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-108">The object responsible for allocating the memory is called an *allocator*, which is a COM object that exposes the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="eb2d9-109">Wenn zwei Pins eine Verbindung herstellen, muss einer der Pins eine Zuweisung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-109">When two pins connect, one of the pins must provide an allocator.</span></span> <span data-ttu-id="eb2d9-110">DirectShow definiert eine Sequenz von Methoden aufrufen, die verwendet wird, um festzulegen, welche PIN die Zuweisung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-110">DirectShow defines a sequence of method calls that is used to establish which pin provides the allocator.</span></span> <span data-ttu-id="eb2d9-111">Die Pins stimmen auch mit der Anzahl von Puffern, die von der Zuweisung erstellt werden, und der Puffergröße überein.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-111">The pins also agree on the number of buffers that the allocator will create, and the size of the buffers.</span></span>

<span data-ttu-id="eb2d9-112">Bevor das Streaming beginnt, erstellt die Zuweisung einen Pufferpool.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-112">Before streaming begins, the allocator creates a pool of buffers.</span></span> <span data-ttu-id="eb2d9-113">Beim Streaming füllt der Upstream-Filter Puffer mit Daten und übergibt sie an den downstreamfilter.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-113">During streaming, the upstream filter fills buffers with data and delivers them to the downstream filter.</span></span> <span data-ttu-id="eb2d9-114">Der upstreamfilter gibt den nachgeschalteten Filter jedoch keine Rohdaten Zeiger auf die Puffer aus.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-114">But the upstream filter does not give the downstream filter raw pointers to the buffers.</span></span> <span data-ttu-id="eb2d9-115">Stattdessen werden COM-Objekte mit dem Namen " *Media Samples*" verwendet, die von der Zuweisung zum Verwalten der Puffer erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-115">Instead, it uses COM objects called *media samples*, which the allocator creates to manage the buffers.</span></span> <span data-ttu-id="eb2d9-116">Mit Medien Beispielen wird die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-116">Media samples expose the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="eb2d9-117">Ein Medien Beispiel enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="eb2d9-117">A media sample contains:</span></span>

-   <span data-ttu-id="eb2d9-118">Ein Zeiger auf den zugrunde liegenden Puffer.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-118">a pointer to the underlying buffer</span></span>
-   <span data-ttu-id="eb2d9-119">ein Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="eb2d9-119">a time stamp</span></span>
-   <span data-ttu-id="eb2d9-120">verschiedene Flags</span><span class="sxs-lookup"><span data-stu-id="eb2d9-120">various flags</span></span>
-   <span data-ttu-id="eb2d9-121">optional ein Medientyp</span><span class="sxs-lookup"><span data-stu-id="eb2d9-121">optionally, a media type</span></span>

<span data-ttu-id="eb2d9-122">Der Zeitstempel definiert die Präsentationszeit, die der rendererfilter zum Planen des Rendering verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-122">The time stamp defines the presentation time, which the renderer filter uses to schedule rendering.</span></span> <span data-ttu-id="eb2d9-123">Die Flags geben an, ob seit dem vorherigen Beispiel eine Unterbrechung der Daten aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-123">The flags indicate things like whether there was a break in the data since the previous sample.</span></span> <span data-ttu-id="eb2d9-124">Der Medientyp stellt eine Möglichkeit für Filter zum Ändern von Formaten in der Mitte des Streams bereit.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-124">The media type provides a way for filters to change formats mid-stream.</span></span> <span data-ttu-id="eb2d9-125">In der Regel hat das Beispiel keinen Medientyp, was darauf hinweist, dass das Format seit dem vorherigen Beispiel nicht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-125">Usually, the sample has no media type, which indicates that the format has not changed since the previous sample.</span></span>

<span data-ttu-id="eb2d9-126">Während ein Filter einen Puffer verwendet, enthält er den Verweis Zähler für das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-126">While a filter is using a buffer, it holds reference count on the sample.</span></span> <span data-ttu-id="eb2d9-127">Die Zuweisung verwendet den Verweis Zähler, um zu bestimmen, wann der Puffer wieder verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-127">The allocator uses the reference count to determine when it can re-use the buffer.</span></span> <span data-ttu-id="eb2d9-128">Dadurch wird verhindert, dass ein Filter einen Puffer überschreibt, den ein anderer Filter weiterhin verwendet.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-128">This prevents a filter from overwriting a buffer that another filter is still using.</span></span> <span data-ttu-id="eb2d9-129">Ein Beispiel kehrt nicht zum Pool der verfügbaren Stichproben zurück, bis jeder Filter ihn freigegeben hat.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-129">A sample does not return to the allocator's pool of available samples until every filter has released it.</span></span>

<span data-ttu-id="eb2d9-130">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="eb2d9-130">For more information, see the following topics:</span></span>

-   <span data-ttu-id="eb2d9-131">Das Thema [Beispiele und Zuweisungen](samples-and-allocators.md) bietet eine ausführlichere Beschreibung der Funktionsweise von Zuweisungen.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-131">The topic [Samples and Allocators](samples-and-allocators.md) provides a more detailed description of how allocators work.</span></span>
-   <span data-ttu-id="eb2d9-132">Der Thema [Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md) bietet einen allgemeinen Überblick über den Datenfluss in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="eb2d9-132">The topic [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md) gives a general overview of data flow in DirectShow.</span></span>

<span data-ttu-id="eb2d9-133">Die folgenden Themen sind für Entwickler gedacht, die ihre eigenen benutzerdefinierten Filter schreiben:</span><span class="sxs-lookup"><span data-stu-id="eb2d9-133">The following topics are intended for developers who are writing their own custom filters:</span></span>

-   [<span data-ttu-id="eb2d9-134">Datenfluss für Filter Entwickler</span><span class="sxs-lookup"><span data-stu-id="eb2d9-134">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
-   [<span data-ttu-id="eb2d9-135">Threads und kritische Abschnitte</span><span class="sxs-lookup"><span data-stu-id="eb2d9-135">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)

## <a name="related-topics"></a><span data-ttu-id="eb2d9-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="eb2d9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eb2d9-137">Das Filter Diagramm und dessen Komponenten</span><span class="sxs-lookup"><span data-stu-id="eb2d9-137">The Filter Graph and Its Components</span></span>](the-filter-graph-and-its-components.md)
</dt> </dl>

 

 



