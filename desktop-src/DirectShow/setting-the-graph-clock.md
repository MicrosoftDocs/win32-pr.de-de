---
description: Festlegen der diagrammuhr
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: Festlegen der diagrammuhr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe98c8dce1ab5f94664fbe1406c682e5d4e50b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344312"
---
# <a name="setting-the-graph-clock"></a><span data-ttu-id="320e1-103">Festlegen der diagrammuhr</span><span class="sxs-lookup"><span data-stu-id="320e1-103">Setting the Graph Clock</span></span>

<span data-ttu-id="320e1-104">Beim Erstellen eines Filter Diagramms wählt der Filter Diagramm-Manager automatisch eine Referenzuhr für das Diagramm aus.</span><span class="sxs-lookup"><span data-stu-id="320e1-104">When you build a filter graph, the Filter Graph Manager automatically chooses a reference clock for the graph.</span></span> <span data-ttu-id="320e1-105">Alle Filter im Diagramm werden mit der Referenzuhr synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="320e1-105">All filters in the graph are synchronized to the reference clock.</span></span> <span data-ttu-id="320e1-106">Insbesondere rendererfilter verwenden die Referenzzeit, um die Präsentationszeit der einzelnen Stichproben zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="320e1-106">In particular, renderer filters use the reference clock to determine the presentation time of each sample.</span></span>

<span data-ttu-id="320e1-107">Es gibt in der Regel keinen Grund dafür, dass eine Anwendung die Auswahl der Referenzuhr des Filter-Graph-Managers außer Kraft setzt.</span><span class="sxs-lookup"><span data-stu-id="320e1-107">There is usually no reason for an application to override the Filter Graph Manager's choice of reference clock.</span></span> <span data-ttu-id="320e1-108">Dies ist jedoch möglich, indem Sie die [**imediafilter:: setsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) -Methode für den Filter Graph-Manager aufrufen.</span><span class="sxs-lookup"><span data-stu-id="320e1-108">However, you can do so by calling the [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method on the Filter Graph Manager.</span></span> <span data-ttu-id="320e1-109">Diese Methode nimmt einen Zeiger auf die **IReferenceClock** -Schnittstelle der Uhr.</span><span class="sxs-lookup"><span data-stu-id="320e1-109">This method takes a pointer to the clock's **IReferenceClock** interface.</span></span> <span data-ttu-id="320e1-110">Ruft die-Methode auf, während das Diagramm angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="320e1-110">Call the method while the graph is stopped.</span></span>

<span data-ttu-id="320e1-111">Wenn ein Filter eine Uhr bereitstellt, können Sie den **IReferenceClock** -Zeiger abrufen, indem Sie **QueryInterface** für den Filter aufrufen.</span><span class="sxs-lookup"><span data-stu-id="320e1-111">If a filter provides a clock, you can get the **IReferenceClock** pointer by calling **QueryInterface** on the filter.</span></span> <span data-ttu-id="320e1-112">Alternativ können Sie eine externe verweisuhr implementieren, die nicht von einem Filter bereitgestellt wird, solange die externe Uhr **IReferenceClock** implementiert.</span><span class="sxs-lookup"><span data-stu-id="320e1-112">Alternatively, you can implement an external reference clock that is not provided by a filter, as long as your external clock implements **IReferenceClock**.</span></span> <span data-ttu-id="320e1-113">Das folgende Beispiel zeigt, wie Sie eine Uhr angeben:</span><span class="sxs-lookup"><span data-stu-id="320e1-113">The following example shows how to specify a clock:</span></span>


```C++
IGraphBuilder *pGraph = 0;
IReferenceClock *pClock = 0;

CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
    IID_IGraphBuilder, (void **)&pGraph);

// Build the graph.
pGraph->RenderFile(L"C:\\Example.avi", 0);

// Create your clock.
hr = CreateMyPrivateClock(&pClock);
if (SUCCEEDED(hr))
{
    // Set the graph clock.
    IMediaFilter *pMediaFilter = 0;
    pGraph->QueryInterface(IID_IMediaFilter, (void**)&pMediaFilter);
    pMediaFilter->SetSyncSource(pClock);
    pClock->Release();
    pMediaFilter->Release();
}
```



<span data-ttu-id="320e1-114">In diesem Beispiel wird davon ausgegangen, dass "conatemyprivateclock" eine Anwendungs definierte Funktion ist, die eine Uhr erstellt und einen **IReferenceClock** -Zeiger zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="320e1-114">This example assumes that CreateMyPrivateClock is an application-defined function that creates a clock and returns an **IReferenceClock** pointer.</span></span>

<span data-ttu-id="320e1-115">Sie können auch festlegen, dass das Filter Diagramm ohne Uhr ausgeführt wird, indem Sie **setsyncsource** mit dem Wert **null** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="320e1-115">You can also set the filter graph to run with no clock, by calling **SetSyncSource** with the value **NULL**.</span></span> <span data-ttu-id="320e1-116">Wenn keine Uhr vorhanden ist, wird das Diagramm so schnell wie möglich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="320e1-116">If there is no clock, the graph runs as quickly as possible.</span></span> <span data-ttu-id="320e1-117">Ohne Uhr warten rendererfilter nicht auf die Präsentationszeit eines Beispiels.</span><span class="sxs-lookup"><span data-stu-id="320e1-117">With no clock, renderer filters do not wait for a sample's presentation time.</span></span> <span data-ttu-id="320e1-118">Stattdessen wird jedes Beispiel so bald wie möglich dargestellt.</span><span class="sxs-lookup"><span data-stu-id="320e1-118">Instead, they render each sample as soon as it arrives.</span></span> <span data-ttu-id="320e1-119">Das Festlegen des Diagramms, das ohne eine Uhr ausgeführt wird, ist nützlich, wenn Sie Daten schnell verarbeiten möchten, anstatt Sie in Echtzeit anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="320e1-119">Setting the graph to run without a clock is useful if you want to process data quickly, rather than previewing it in real time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="320e1-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="320e1-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="320e1-121">Grundlegende DirectShow-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="320e1-121">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="320e1-122">**Cbasereferenceclock-Klasse**</span><span class="sxs-lookup"><span data-stu-id="320e1-122">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> <dt>

[<span data-ttu-id="320e1-123">Uhrzeit und Uhren in DirectShow</span><span class="sxs-lookup"><span data-stu-id="320e1-123">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



