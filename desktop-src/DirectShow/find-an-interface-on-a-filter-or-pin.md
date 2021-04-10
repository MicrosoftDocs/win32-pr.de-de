---
description: Suchen einer Schnittstelle in einem Filter oder einer PIN
ms.assetid: 546f5b7d-3bcd-4e97-a012-daca6ae7bca1
title: Suchen einer Schnittstelle in einem Filter oder einer PIN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d264a35e0c33ba53f6a8df7f69113f3358a9737
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213817"
---
# <a name="find-an-interface-on-a-filter-or-pin"></a><span data-ttu-id="43067-103">Suchen einer Schnittstelle in einem Filter oder einer PIN</span><span class="sxs-lookup"><span data-stu-id="43067-103">Find an Interface on a Filter or Pin</span></span>

<span data-ttu-id="43067-104">Bei vielen Vorgängen in DirectShow Ruft die Anwendung Methoden für den Filter Graph-Manager auf.</span><span class="sxs-lookup"><span data-stu-id="43067-104">For many operations in DirectShow, the application calls methods on the Filter Graph Manager.</span></span> <span data-ttu-id="43067-105">In einigen Situationen muss die Anwendung jedoch eine Methode direkt für einen Filter oder eine PIN aufruft.</span><span class="sxs-lookup"><span data-stu-id="43067-105">In some situations, however, the application must call a method directly on a filter or pin.</span></span> <span data-ttu-id="43067-106">Viele Filter machen z. b. spezielle Schnittstellen verfügbar, die zum Konfigurieren des Filters verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43067-106">For example, many filters expose specialized interfaces that are used to configure the filter.</span></span>

<span data-ttu-id="43067-107">Im Fall einer Filter Schnittstelle verfügen Sie möglicherweise bereits über einen Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Filters.</span><span class="sxs-lookup"><span data-stu-id="43067-107">In the case of a filter interface, you might already have a pointer to the filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span> <span data-ttu-id="43067-108">Verwenden Sie in diesem Fall einfach **QueryInterface** , um die andere Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="43067-108">In that case, simply use **QueryInterface** to get the other interface.</span></span> <span data-ttu-id="43067-109">Einige Filter können dem Diagramm jedoch vom Filter Graph-Manager hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="43067-109">But some filters might be added to the graph by the Filter Graph Manager.</span></span> <span data-ttu-id="43067-110">(Ausführliche Informationen finden Sie unter [Intelligent Connect](intelligent-connect.md).) Verwenden Sie in diesem Fall die Schnittstelle [**ienumfilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) , um alle Filter im Diagramm zu durchlaufen und nacheinander abzufragen.</span><span class="sxs-lookup"><span data-stu-id="43067-110">(For details, see [Intelligent Connect](intelligent-connect.md).) In that case, use the [**IEnumFilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) interface to loop through all the filters in the graph, and query each one in turn.</span></span> <span data-ttu-id="43067-111">Dies wird in der folgenden Funktion veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="43067-111">The following function demonstrates this:</span></span>


```C++
HRESULT FindFilterInterface(
    IGraphBuilder *pGraph, // Pointer to the Filter Graph Manager.
    REFGUID iid,           // IID of the interface to retrieve.
    void **ppUnk)          // Receives the interface pointer.
{
    if (!pGraph || !ppUnk) return E_POINTER;

    HRESULT hr = E_FAIL;
    IEnumFilters *pEnum = NULL;
    IBaseFilter *pF = NULL;
    if (FAILED(pGraph->EnumFilters(&pEnum)))
    {
        return E_FAIL;
    }
    // Query every filter for the interface.
    while (S_OK == pEnum->Next(1, &pF, 0))
    {
        hr = pF->QueryInterface(iid, ppUnk);
        pF->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



<span data-ttu-id="43067-112">Um eine Schnittstelle in einer PIN zu finden, verwenden Sie die [**iumumpins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) -Schnittstelle, um die Pins eines Filters zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="43067-112">To find an interface on a pin, use the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface to loop through the pins on a filter.</span></span> <span data-ttu-id="43067-113">Die folgende Funktion zeigt die Vorgehensweise:</span><span class="sxs-lookup"><span data-stu-id="43067-113">The following function shows how to do this:</span></span>


```C++
HRESULT FindPinInterface(
    IBaseFilter *pFilter,  // Pointer to the filter to search.
    REFGUID iid,           // IID of the interface.
    void **ppUnk)          // Receives the interface pointer.
{
    if (!pFilter || !ppUnk) return E_POINTER;

    HRESULT hr = E_FAIL;
    IEnumPins *pEnum = 0;
    if (FAILED(pFilter->EnumPins(&pEnum)))
    {
        return E_FAIL;
    }
    // Query every pin for the interface.
    IPin *pPin = 0;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        hr = pPin->QueryInterface(iid, ppUnk);
        pPin->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



<span data-ttu-id="43067-114">Die Next-Funktion sucht nach einer Schnittstelle in einem Filter oder einer PIN:</span><span class="sxs-lookup"><span data-stu-id="43067-114">The next function searches for an interface on a filter or a pin:</span></span>


```C++
HRESULT FindInterfaceAnywhere(
    IGraphBuilder *pGraph, 
    REFGUID iid, 
    void **ppUnk)
{
    if (!pGraph || !ppUnk) return E_POINTER;
    HRESULT hr = E_FAIL;
    IEnumFilters *pEnum = 0;
    if (FAILED(pGraph->EnumFilters(&pEnum)))
    {
        return E_FAIL;
    }
    // Loop through every filter in the graph.
    IBaseFilter *pF = 0;
    while (S_OK == pEnum->Next(1, &pF, 0))
    {
        hr = pF->QueryInterface(iid, ppUnk);
        if (FAILED(hr))
        {
            // The filter does not expose the interface, but maybe
            // one of its pins does.
            hr = FindPinInterface(pF, iid, ppUnk);
        }
        pF->Release();
        if (SUCCEEDED(hr))
        {
            break;
        }
    }
    pEnum->Release();
    return hr;
}
```



<span data-ttu-id="43067-115">Beachten Sie, dass alle hier gezeigten Funktionen bei der ersten erfolgreichen **QueryInterface** angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="43067-115">Note that all of the functions shown here stop at the first successful **QueryInterface**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43067-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43067-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43067-117">Auflisten von Filtern</span><span class="sxs-lookup"><span data-stu-id="43067-117">Enumerating Filters</span></span>](enumerating-filters.md)
</dt> <dt>

[<span data-ttu-id="43067-118">Auflisten von Pins</span><span class="sxs-lookup"><span data-stu-id="43067-118">Enumerating Pins</span></span>](enumerating-pins.md)
</dt> <dt>

[<span data-ttu-id="43067-119">**ICaptureGraphBuilder2:: findinterface**</span><span class="sxs-lookup"><span data-stu-id="43067-119">**ICaptureGraphBuilder2::FindInterface**</span></span>](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



