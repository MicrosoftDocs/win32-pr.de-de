---
description: Entfernen Sie alle Filter im Graph
ms.assetid: a11af581-c331-4607-be8b-5f65961bd422
title: Entfernen Sie alle Filter im Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f10b76bb5f5bc3cff2bfb989c422f177ef0d2ee4d09acff3c2f895ef9984b7c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072734"
---
# <a name="remove-all-the-filters-in-the-graph"></a>Entfernen Sie alle Filter im Graph

Am einfachsten können Sie alle Filter in einem Filterdiagramm entfernen, indem Sie einfach den Filter Graph Manager veröffentlichen und einen neuen erstellen. Stellen Sie sicher, dass Sie jeden Zeiger, den Ihre Anwendung auf beliebige Schnittstellen in den Filter-Graph-Managern hat, sowie Zeiger auf Objekte im Diagramm, einschließlich Filtern, Stecknadeln, der Referenzuhr usw. frei geben.

Alternativ können Sie die Filter nach und nach mithilfe der [**IFilterGraph::RemoveFilter-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-removefilter) entfernen:


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



In diesem Beispiel wird die [**IFilterGraph::EnumFilters-Methode**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) verwendet, um die Filter im Diagramm zu aufzählen. Das Entfernen eines Filters führt dazu, dass das Enumeratorobjekt nicht mehr mit dem Diagramm synchron ist. Verwenden Sie [**die IEnumFilters::Reset-Methode,**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-reset) um den Enumerator zurückzusetzen. Andernfalls wird jeder nachfolgende Aufruf von [**IEnumFilters::Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) fehlschlagen.

 

 



