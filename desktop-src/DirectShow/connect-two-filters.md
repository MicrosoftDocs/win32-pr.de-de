---
description: In diesem Thema werden einige Hilfsfunktionen zum Verbinden von DirectShow-Filtern erläutert.
ms.assetid: cfd85944-7ae7-49e6-948f-9e190cdeed12
title: Zwei Filter verbinden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e70e607c510490e7ed841ea44303153a94e83f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124868"
---
# <a name="connect-two-filters"></a><span data-ttu-id="44b58-103">Zwei Filter verbinden</span><span class="sxs-lookup"><span data-stu-id="44b58-103">Connect Two Filters</span></span>

<span data-ttu-id="44b58-104">In diesem Thema werden einige Hilfsfunktionen zum Verbinden von DirectShow-Filtern erläutert.</span><span class="sxs-lookup"><span data-stu-id="44b58-104">This topic shows some helper functions for connecting DirectShow filters.</span></span>

<span data-ttu-id="44b58-105">Um zwei Filter miteinander zu verbinden, müssen Sie für den upstreamfilter eine nicht verbundene Ausgabe-PIN und für den downstreamfilter eine nicht verbundene Eingabe-PIN finden.</span><span class="sxs-lookup"><span data-stu-id="44b58-105">To connect two filters, you must find an unconnected output pin on the upstream filter, and an unconnected input pin on the downstream filter.</span></span>

<span data-ttu-id="44b58-106">Wenn Sie bereits über Zeiger auf beide Pins verfügen, müssen Sie die [**igraphbuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) -Methode zum Herstellen einer Verbindung abrufen.</span><span class="sxs-lookup"><span data-stu-id="44b58-106">If you already have pointers to both pins, call the [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) method to connect them.</span></span> <span data-ttu-id="44b58-107">Wenn die Pins keine direkte Verbindung herstellen können, fügt die **igraphbuilder:: Connect** -Methode möglicherweise zusätzliche Filter ein, um die Verbindung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="44b58-107">If the pins cannot connect directly to each other, the **IGraphBuilder::Connect** method might insert additional filters, to complete the connection.</span></span> <span data-ttu-id="44b58-108">Weitere Informationen finden Sie unter [Intelligent Connect](intelligent-connect.md).</span><span class="sxs-lookup"><span data-stu-id="44b58-108">For more information, see [Intelligent Connect](intelligent-connect.md).</span></span>

<span data-ttu-id="44b58-109">Wenn Sie über einen Zeiger auf die Filter, aber nicht über die Pins verfügen, müssen Sie die [**ibasefilter:: enumpins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) -Methode verwenden, um die Pins zu suchen.</span><span class="sxs-lookup"><span data-stu-id="44b58-109">If you have a pointer to the filters but not the pins, you must use the [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) method to find the pins.</span></span> <span data-ttu-id="44b58-110">(Weitere Informationen finden Sie unter Auflisten von [Pins](enumerating-pins.md).) Diese Technik wird in den Hilfsfunktionen in diesem Thema veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="44b58-110">(See [Enumerating Pins](enumerating-pins.md).) The helper functions in this topic demonstrate this technique.</span></span>

### <a name="output-pin-to-filter"></a><span data-ttu-id="44b58-111">Anzufilternde Ausgabe-PIN</span><span class="sxs-lookup"><span data-stu-id="44b58-111">Output Pin to Filter</span></span>

<span data-ttu-id="44b58-112">Die folgende Funktion nimmt zwei Parameter an: einen Zeiger auf eine Ausgabe-PIN und einen Zeiger auf einen Filter.</span><span class="sxs-lookup"><span data-stu-id="44b58-112">The following function takes two parameters: A pointer to an output pin, and a pointer to a filter.</span></span> <span data-ttu-id="44b58-113">Die-Funktion verbindet die Ausgabe-PIN mit der ersten verfügbaren Eingabe-PIN für den Filter.</span><span class="sxs-lookup"><span data-stu-id="44b58-113">The function connects the output pin to the first available input pin on the filter.</span></span>


```C++
// Connect output pin to filter.

HRESULT ConnectFilters(
    IGraphBuilder *pGraph, // Filter Graph Manager.
    IPin *pOut,            // Output pin on the upstream filter.
    IBaseFilter *pDest)    // Downstream filter.
{
    IPin *pIn = NULL;
        
    // Find an input pin on the downstream filter.
    HRESULT hr = FindUnconnectedPin(pDest, PINDIR_INPUT, &pIn);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pIn->Release();
    }
    return hr;
}
```



<span data-ttu-id="44b58-114">Diese Funktion führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="44b58-114">This function does the following:</span></span>

1.  <span data-ttu-id="44b58-115">Ruft die- `FindUnconnectedPin` Funktion auf, um eine nicht verbundene Eingabe-PIN zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="44b58-115">Calls the `FindUnconnectedPin` function to get an unconnected input pin.</span></span> <span data-ttu-id="44b58-116">Diese Funktion wird im Thema [Suchen einer nicht verbundenen PIN für einen Filter](find-an-unconnected-pin-on-a-filter.md)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="44b58-116">This function is shown in the topic [Find an Unconnected Pin on a Filter](find-an-unconnected-pin-on-a-filter.md).</span></span>
2.  <span data-ttu-id="44b58-117">Ruft [**igraphbuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) auf, um die beiden Pins zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="44b58-117">Calls [**IGraphBuilder::Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) to connect the two pins.</span></span>

### <a name="filter-to-input-pin"></a><span data-ttu-id="44b58-118">An Eingabe-PIN Filtern</span><span class="sxs-lookup"><span data-stu-id="44b58-118">Filter to Input Pin</span></span>

<span data-ttu-id="44b58-119">Die Next-Funktion nimmt einen Zeiger auf einen Filter und einen Zeiger auf eine Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="44b58-119">The next function takes a pointer to a filter and a pointer to an input pin.</span></span> <span data-ttu-id="44b58-120">Er verbindet die Eingabe-PIN mit dem ersten verfügbaren Ausgabepin für den Filter.</span><span class="sxs-lookup"><span data-stu-id="44b58-120">It connects the input pin to the first available output pin on the filter.</span></span>


```C++
// Connect filter to input pin.

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IPin *pIn)
{
    IPin *pOut = NULL;
        
    // Find an output pin on the upstream filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pOut->Release();
    }
    return hr;
}
```



### <a name="filter-to-filter"></a><span data-ttu-id="44b58-121">Filter zum Filtern</span><span class="sxs-lookup"><span data-stu-id="44b58-121">Filter to Filter</span></span>

<span data-ttu-id="44b58-122">Die dritte Funktion nimmt einen Zeiger auf einen upstreamfilter und einen Zeiger auf einen downstreamfilter und versucht, beide Filter zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="44b58-122">The third function takes a pointer to an upstream filter and a pointer to a downstream filter, and tries to connect both filters.</span></span>


```C++
// Connect filter to filter

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IBaseFilter *pDest)
{
    IPin *pOut = NULL;

    // Find an output pin on the first filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        hr = ConnectFilters(pGraph, pOut, pDest);
        pOut->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="44b58-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="44b58-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="44b58-124">Allgemeine Graph-Building Techniken</span><span class="sxs-lookup"><span data-stu-id="44b58-124">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> <dt>

[<span data-ttu-id="44b58-125">**ICaptureGraphBuilder2:: RenderStream**</span><span class="sxs-lookup"><span data-stu-id="44b58-125">**ICaptureGraphBuilder2::RenderStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



