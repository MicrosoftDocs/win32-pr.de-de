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
# <a name="remove-all-the-filters-in-the-graph"></a>Alle Filter im Diagramm entfernen

Die einfachste Möglichkeit, alle Filter in einem Filter Diagramm zu entfernen, besteht darin, den Filter Graph-Manager freizugeben und einen neuen zu erstellen. Stellen Sie sicher, dass Sie jeden Zeiger, den Ihre Anwendung besitzt, auf alle Schnittstellen der Filter-Diagramm-Manager und Zeiger auf Objekte im Diagramm, einschließlich Filter, Pins, der Referenzuhr usw., freigeben.

Alternativ können Sie die Filter einzeln entfernen, indem Sie die [**ifiltergraph:: RemoveFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) -Methode verwenden:


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



In diesem Beispiel wird die [**ifiltergraph:: enumfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) -Methode verwendet, um die Filter im Diagramm aufzulisten. Das Entfernen eines Filters bewirkt, dass das Enumeratorobjekt nicht mehr mit dem Diagramm synchronisiert wird. Verwenden Sie die [**ienumfilters:: Reset**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) -Methode, um den Enumerator zurückzusetzen. Andernfalls schlagen alle nachfolgenden Aufrufe von ' [**ienumfilters:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) ' fehl.

 

 



