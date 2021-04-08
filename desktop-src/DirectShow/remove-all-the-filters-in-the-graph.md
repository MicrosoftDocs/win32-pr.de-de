---
description: Alle Filter im Diagramm entfernen
ms.assetid: a11af581-c331-4607-be8b-5f65961bd422
title: Alle Filter im Diagramm entfernen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d414ef7e532eaf5df9143a6b601a57e4a8bd45
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746304"
---
# <a name="remove-all-the-filters-in-the-graph"></a><span data-ttu-id="a8e30-103">Alle Filter im Diagramm entfernen</span><span class="sxs-lookup"><span data-stu-id="a8e30-103">Remove All the Filters in the Graph</span></span>

<span data-ttu-id="a8e30-104">Die einfachste Möglichkeit, alle Filter in einem Filter Diagramm zu entfernen, besteht darin, den Filter Graph-Manager freizugeben und einen neuen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a8e30-104">The easiest way to remove all of the filters in a filter graph is simply to release the Filter Graph Manager and create a new one.</span></span> <span data-ttu-id="a8e30-105">Stellen Sie sicher, dass Sie jeden Zeiger, den Ihre Anwendung besitzt, auf alle Schnittstellen der Filter-Diagramm-Manager und Zeiger auf Objekte im Diagramm, einschließlich Filter, Pins, der Referenzuhr usw., freigeben.</span><span class="sxs-lookup"><span data-stu-id="a8e30-105">Make sure to release every pointer that your application has to any interfaces on the Filter Graph Managers, as well as pointers to objects in the graph, including filters, pins, the reference clock, and so forth.</span></span>

<span data-ttu-id="a8e30-106">Alternativ können Sie die Filter einzeln entfernen, indem Sie die [**ifiltergraph:: RemoveFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) -Methode verwenden:</span><span class="sxs-lookup"><span data-stu-id="a8e30-106">Alternatively, you can remove the filters one at a time, using the [**IFilterGraph::RemoveFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) method:</span></span>


```C++
// Stop the graph.
pControl->Stop();

// Enumerate the filters in the graph.
IEnumFilters *pEnum = NULL;
HRESULT hr = pGraph->EnumFilters(&pEnum);
if (SUCCEEDED(hr))
{
    IBaseFilter *pFilter = NULL;
    while (S_OK == pEnum->Next(1, &pFilter, NULL))
     {
         // Remove the filter.
         pGraph->RemoveFilter(pFilter);
         // Reset the enumerator.
         pEnum->Reset();
         pFilter->Release();
    }
    pEnum->Release();
}
```



<span data-ttu-id="a8e30-107">In diesem Beispiel wird die [**ifiltergraph:: enumfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) -Methode verwendet, um die Filter im Diagramm aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="a8e30-107">This example uses the [**IFilterGraph::EnumFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) method to enumerate the filters in the graph.</span></span> <span data-ttu-id="a8e30-108">Das Entfernen eines Filters bewirkt, dass das Enumeratorobjekt nicht mehr mit dem Diagramm synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="a8e30-108">Removing a filter causes the enumerator object to become out of sync with the graph.</span></span> <span data-ttu-id="a8e30-109">Verwenden Sie die [**ienumfilters:: Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) -Methode, um den Enumerator zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="a8e30-109">Use the [**IEnumFilters::Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) method to reset the enumerator.</span></span> <span data-ttu-id="a8e30-110">Andernfalls schlagen alle nachfolgenden Aufrufe von ' [**ienumfilters:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) ' fehl.</span><span class="sxs-lookup"><span data-stu-id="a8e30-110">Otherwise, any subsequent call to [**IEnumFilters::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) will fail.</span></span>

 

 



