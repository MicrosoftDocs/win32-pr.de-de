---
description: Suchen eines Filter Peers
ms.assetid: 74d9fe65-f7f4-4971-9550-27884ac4146b
title: Suchen eines Filter Peers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1717f6ad61ad7310fdaa11ea5baaab4dcb7f8011
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041118"
---
# <a name="find-a-filters-peer"></a><span data-ttu-id="20c46-103">Suchen eines Filter Peers</span><span class="sxs-lookup"><span data-stu-id="20c46-103">Find a Filters Peer</span></span>

<span data-ttu-id="20c46-104">Bei einem Filter können Sie das Diagramm durchlaufen, indem Sie die Filter suchen, mit denen eine Verbindung besteht.</span><span class="sxs-lookup"><span data-stu-id="20c46-104">Given a filter, you can traverse the graph by finding the filters to which it is connected.</span></span> <span data-ttu-id="20c46-105">Beginnen Sie mit dem Auflisten der Pins des Filters.</span><span class="sxs-lookup"><span data-stu-id="20c46-105">Start by enumerating the filter's pins.</span></span> <span data-ttu-id="20c46-106">Überprüfen Sie für jede PIN, ob diese PIN mit einer anderen Pin verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="20c46-106">For each pin, check whether that pin is connected to another pin.</span></span> <span data-ttu-id="20c46-107">Wenn dies der Fall ist, Fragen Sie die andere PIN nach Ihrem besitzenden Filter ab.</span><span class="sxs-lookup"><span data-stu-id="20c46-107">If so, query the other pin for it's owning filter.</span></span> <span data-ttu-id="20c46-108">Sie können das Diagramm in der Upstream-Richtung durchlaufen, indem Sie die Eingabe Pins des Filters oder in der Downstream-Richtung auflisten, indem Sie die Ausgabe Pins aufzählen.</span><span class="sxs-lookup"><span data-stu-id="20c46-108">You can walk the graph in the upstream direction by enumerating the filter's input pins, or in the downstream direction by enumerating the output pins.</span></span>

<span data-ttu-id="20c46-109">Mit der folgenden Funktion wird Upstream oder Downstream nach einem verbundenen Filter durchsucht.</span><span class="sxs-lookup"><span data-stu-id="20c46-109">The following function searches upstream or downstream for a connected filter.</span></span> <span data-ttu-id="20c46-110">Er gibt den ersten übereinstimmenden Filter zurück, den er findet:</span><span class="sxs-lookup"><span data-stu-id="20c46-110">It returns the first matching filter that it finds:</span></span>


```C++
// Get the first upstream or downstream filter
HRESULT GetNextFilter(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    IBaseFilter **ppNext) // Receives a pointer to the next filter.
{
    if (!pFilter || !ppNext) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                pPin->Release();
                pEnum->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    return E_UNEXPECTED;
                }
                // This is the filter we're looking for.
                *ppNext = PinInfo.pFilter; // Client must release.
                return S_OK;
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    // Did not find a matching filter.
    return E_FAIL;
}
```



<span data-ttu-id="20c46-111">Die Funktion ruft [**ibasefilter:: enumpins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) auf, um die Pins des ersten Filters aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="20c46-111">The function calls [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) to enumerate the first filter's pins.</span></span> <span data-ttu-id="20c46-112">Für jede PIN wird [**IPin:: querydirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) aufgerufen, um zu überprüfen, ob die PIN der angegebenen Richtung entspricht (Eingabe oder Ausgabe).</span><span class="sxs-lookup"><span data-stu-id="20c46-112">For each pin, it calls [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) to check whether the pin matches the specified direction (input or output).</span></span> <span data-ttu-id="20c46-113">Wenn dies der Fall ist, bestimmt die Funktion, ob diese PIN mit einer anderen Pin verbunden ist, indem die [**IPin:: connectedto**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="20c46-113">If so, the function determines whether that pin is connected to another pin, by calling the [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) method.</span></span> <span data-ttu-id="20c46-114">Schließlich wird [**IPin:: querypininfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) für die verbundene Pin aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="20c46-114">Finally, it calls [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) on the connected pin.</span></span> <span data-ttu-id="20c46-115">Diese Methode gibt eine-Struktur zurück, die unter anderem einen Zeiger auf den besitzenden Filter der PIN enthält.</span><span class="sxs-lookup"><span data-stu-id="20c46-115">This method returns a structure that contains, among other things, a pointer to that pin's owning filter.</span></span> <span data-ttu-id="20c46-116">Dieser Zeiger wird an den Aufrufer im *ppnext* -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="20c46-116">This pointer is returned to the caller in the *ppNext* parameter.</span></span> <span data-ttu-id="20c46-117">Der Aufrufer muss den Zeiger freigeben.</span><span class="sxs-lookup"><span data-stu-id="20c46-117">The caller must release the pointer.</span></span>

<span data-ttu-id="20c46-118">Der folgende Code zeigt, wie diese Funktion aufgerufen wird:</span><span class="sxs-lookup"><span data-stu-id="20c46-118">The following code shows how to call this function:</span></span>


```C++
IBaseFilter *pF; // Pointer to some filter.
IBaseFilter *pUpstream = NULL;
if (SUCCEEDED(GetNextFilter(pF, PINDIR_INPUT, &pUpstream)))
{
    // Use pUpstream ...
    pUpstream->Release();
}
```



<span data-ttu-id="20c46-119">Ein Filter kann mit zwei oder mehr Filtern in beide Richtungen verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="20c46-119">A filter might be connected to two or more filters in either direction.</span></span> <span data-ttu-id="20c46-120">Beispielsweise kann es sich um einen Splitter Filter mit mehreren nachgelagerten Filtern handeln.</span><span class="sxs-lookup"><span data-stu-id="20c46-120">For example, it might be a splitter filter, with several filters downstream from it.</span></span> <span data-ttu-id="20c46-121">Möglicherweise handelt es sich um einen MUX-Filter mit mehreren vorgelagerten filtern.</span><span class="sxs-lookup"><span data-stu-id="20c46-121">Or it might be a mux filter, with several filters upstream from it.</span></span> <span data-ttu-id="20c46-122">Daher sollten Sie alle in einer Liste erfassen.</span><span class="sxs-lookup"><span data-stu-id="20c46-122">Therefore, you might want to collect all of them into a list.</span></span>

<span data-ttu-id="20c46-123">Der folgende Code zeigt eine Möglichkeit, eine solche Funktion zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="20c46-123">The following code shows one possible way to implement such a function.</span></span> <span data-ttu-id="20c46-124">Dabei wird die DirectShow [**cgenericlist**](cgenericlist.md) -Klasse verwendet. Sie können eine äquivalente Funktion mit einer anderen Datenstruktur schreiben.</span><span class="sxs-lookup"><span data-stu-id="20c46-124">It uses the DirectShow [**CGenericList**](cgenericlist.md) class; you could write an equivalent function using some other data structure.</span></span>


```C++
#include <streams.h>  // Link to the DirectShow base class library
// Define a typedef for a list of filters.
typedef CGenericList<IBaseFilter> CFilterList;

// Forward declaration. Adds a filter to the list unless it's a duplicate.
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew);

// Find all the immediate upstream or downstream peers of a filter.
HRESULT GetPeerFilters(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    CFilterList &FilterList)  // Collect the results in this list.
{
    if (!pFilter) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    pPin->Release();
                    pEnum->Release();
                    return E_UNEXPECTED;
                }
                // Insert the filter into the list.
                AddFilterUnique(FilterList, PinInfo.pFilter);
                PinInfo.pFilter->Release();
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    return S_OK;
}
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew)
{
    if (pNew == NULL) return;

    POSITION pos = FilterList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pF = FilterList.GetNext(pos);
        if (IsEqualObject(pF, pNew))
        {
            return;
        }
    }
    pNew->AddRef();  // The caller must release everything in the list.
    FilterList.AddTail(pNew);
}
```



<span data-ttu-id="20c46-125">Um die Dinge etwas komplizierter zu machen, kann ein Filter über mehrere Pin-Verbindungen mit dem gleichen Filter verfügen.</span><span class="sxs-lookup"><span data-stu-id="20c46-125">To complicate matters somewhat, a filter can have multiple pin connections to the same filter.</span></span> <span data-ttu-id="20c46-126">Um zu vermeiden, dass Duplikate in die Liste aufgenommen werden, Fragen Sie jeden **ibasefilter** -Zeiger auf **IUnknown** ab und vergleichen die **IUnknown** -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="20c46-126">To avoid putting duplicates into the list, query each **IBaseFilter** pointer for **IUnknown** and compare the **IUnknown** pointers.</span></span> <span data-ttu-id="20c46-127">Durch die com-Regeln verweisen zwei Schnittstellen Zeiger auf dasselbe Objekt, wenn Sie identische **IUnknown** -Zeiger zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="20c46-127">By the rules of COM, two interface pointers refer to the same object if and only if they return identical **IUnknown** pointers.</span></span> <span data-ttu-id="20c46-128">Im vorherigen Beispiel verarbeitet die addfilterunique-Funktion dieses Detail.</span><span class="sxs-lookup"><span data-stu-id="20c46-128">In the previous example, the AddFilterUnique function handles this detail.</span></span>

<span data-ttu-id="20c46-129">Im folgenden Beispiel wird gezeigt, wie die getPeer Filters-Funktion verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="20c46-129">The following example shows how to use the GetPeerFilters function:</span></span>


```C++
IBaseFilter *pF; // Pointer to some filter.
CFilterList FList(NAME("MyList"));  // List to hold the downstream peers.
hr = GetPeerFilters(pF, PINDIR_OUTPUT, FList);
if (SUCCEEDED(hr))
{
    POSITION pos = FList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pDownstream = FList.GetNext(pos);
        pDownstream->Release();
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="20c46-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="20c46-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20c46-131">Allgemeine Graph-Building Techniken</span><span class="sxs-lookup"><span data-stu-id="20c46-131">General Graph-Building Techniques</span></span>](general-graph-building-techniques.md)
</dt> </dl>

 

 



