---
description: Threads und kritische Abschnitte
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: Threads und kritische Abschnitte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 576cb28e7e382db92328adf09980a825e71b5a3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104350338"
---
# <a name="threads-and-critical-sections"></a><span data-ttu-id="c2bcc-103">Threads und kritische Abschnitte</span><span class="sxs-lookup"><span data-stu-id="c2bcc-103">Threads and Critical Sections</span></span>

<span data-ttu-id="c2bcc-104">In diesem Abschnitt wird das Threading in DirectShow-Filtern und die Schritte beschrieben, die Sie durchführen sollten, um Abstürze oder Deadlocks in einem benutzerdefinierten Filter zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-104">This section describes threading in DirectShow filters, and the steps you should take to avoid crashes or deadlocks in a custom filter.</span></span>

<span data-ttu-id="c2bcc-105">In den Beispielen in diesem Abschnitt wird Pseudo Code verwendet, um den Code zu veranschaulichen, den Sie schreiben müssen.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-105">The examples in this section use pseudocode to illustrate the code you will need to write.</span></span> <span data-ttu-id="c2bcc-106">Sie gehen davon aus, dass ein benutzerdefinierter Filter von den DirectShow-Basisklassen abgeleitete Klassen wie folgt verwendet:</span><span class="sxs-lookup"><span data-stu-id="c2bcc-106">They assume that a custom filter is using classes derived from the DirectShow base classes, as follows:</span></span>

-   <span data-ttu-id="c2bcc-107">Cmyinputpin: abgeleitet von [**cbaseinputpin**](cbaseinputpin.md).</span><span class="sxs-lookup"><span data-stu-id="c2bcc-107">CMyInputPin: Derived from [**CBaseInputPin**](cbaseinputpin.md).</span></span>
-   <span data-ttu-id="c2bcc-108">Cmyoutputpin: abgeleitet von [**cbaseoutputpin**](cbaseoutputpin.md).</span><span class="sxs-lookup"><span data-stu-id="c2bcc-108">CMyOutputPin: Derived from [**CBaseOutputPin**](cbaseoutputpin.md).</span></span>
-   <span data-ttu-id="c2bcc-109">Cmyfilter: abgeleitet von [**cbasefilter**](cbasefilter.md).</span><span class="sxs-lookup"><span data-stu-id="c2bcc-109">CMyFilter: Derived from [**CBaseFilter**](cbasefilter.md).</span></span>
-   <span data-ttu-id="c2bcc-110">Cmyinputzucator: die Zuweisung der eingabepin, die von [**cmemzuzuordcator**](cmemallocator.md)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-110">CMyInputAllocator: The input pin's allocator, derived from [**CMemAllocator**](cmemallocator.md).</span></span> <span data-ttu-id="c2bcc-111">Nicht jeder Filter benötigt eine benutzerdefinierte Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-111">Not every filter needs a custom allocator.</span></span> <span data-ttu-id="c2bcc-112">Für viele Filter ist die Klasse **cmemzuordcator** ausreichend.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-112">For many filters, the **CMemAllocator** class is sufficient.</span></span>

<span data-ttu-id="c2bcc-113">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="c2bcc-113">This section contains the following topics.</span></span>

-   [<span data-ttu-id="c2bcc-114">Streaming-und Anwendungsthreads</span><span class="sxs-lookup"><span data-stu-id="c2bcc-114">The Streaming and Application Threads</span></span>](the-streaming-and-application-threads.md)
-   [<span data-ttu-id="c2bcc-115">Wird angehalten</span><span class="sxs-lookup"><span data-stu-id="c2bcc-115">Pausing</span></span>](pausing.md)
-   [<span data-ttu-id="c2bcc-116">Empfangen und Bereitstellung von Beispielen</span><span class="sxs-lookup"><span data-stu-id="c2bcc-116">Receiving and Delivering Samples</span></span>](receiving-and-delivering-samples.md)
-   [<span data-ttu-id="c2bcc-117">Über das Ende des Streams</span><span class="sxs-lookup"><span data-stu-id="c2bcc-117">Delivering the End of Stream</span></span>](delivering-the-end-of-stream.md)
-   [<span data-ttu-id="c2bcc-118">Leeren von Daten</span><span class="sxs-lookup"><span data-stu-id="c2bcc-118">Flushing Data</span></span>](flushing-data.md)
-   [<span data-ttu-id="c2bcc-119">Wird beendet</span><span class="sxs-lookup"><span data-stu-id="c2bcc-119">Stopping</span></span>](stopping.md)
-   [<span data-ttu-id="c2bcc-120">Puffer werden erhalten.</span><span class="sxs-lookup"><span data-stu-id="c2bcc-120">Getting Buffers</span></span>](getting-buffers.md)
-   [<span data-ttu-id="c2bcc-121">Streamingthreads und der Filter Graph-Manager</span><span class="sxs-lookup"><span data-stu-id="c2bcc-121">Streaming Threads and the Filter Graph Manager</span></span>](streaming-threads-and-the-filter-graph-manager.md)
-   [<span data-ttu-id="c2bcc-122">Zusammenfassung des filterthreading</span><span class="sxs-lookup"><span data-stu-id="c2bcc-122">Summary of Filter Threading</span></span>](summary-of-filter-threading.md)

## <a name="related-topics"></a><span data-ttu-id="c2bcc-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c2bcc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c2bcc-124">Datenfluss für Filter Entwickler</span><span class="sxs-lookup"><span data-stu-id="c2bcc-124">Data Flow for Filter Developers</span></span>](data-flow-for-filter-developers.md)
</dt> <dt>

[<span data-ttu-id="c2bcc-125">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="c2bcc-125">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



