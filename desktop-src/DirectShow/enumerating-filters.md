---
description: Aufzählen von Filtern
ms.assetid: 57bcaa4d-37bf-457d-937e-f9d24fb5784f
title: Aufzählen von Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d584ddf74a13b06e99d9a7e0a34ac802c6da881d87cb163411100ea7772e1df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819663"
---
# <a name="enumerating-filters"></a>Aufzählen von Filtern

Der Filter Graph Manager unterstützt die [**IFilterGraph::EnumFilters-Methode,**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) die alle Filter im Filterdiagramm aufzählt. Sie gibt einen Zeiger auf die [**IEnumFilters-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) zurück. Die [**IEnumFilters::Next-Methode**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) ruft [**IBaseFilter-Schnittstellenzeiger**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) ab.

Das folgende Beispiel zeigt eine Funktion, die die Filter in einem Diagramm aufzählt und ein Meldungsfeld mit dem Namen jedes Filters anzeigt. Er verwendet die [**IBaseFilter::QueryFilterInfo-Methode,**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) um den Namen des Filters abzurufen. Beachten Sie die Stellen, an denen die Funktion **Release** für eine Schnittstelle aufruft, um den Verweiszähler zu dekrementieren.


```C++
HRESULT EnumFilters (IFilterGraph *pGraph) 
{
    IEnumFilters *pEnum = NULL;
    IBaseFilter *pFilter;
    ULONG cFetched;

    HRESULT hr = pGraph->EnumFilters(&pEnum);
    if (FAILED(hr)) return hr;

    while(pEnum->Next(1, &pFilter, &cFetched) == S_OK)
    {
        FILTER_INFO FilterInfo;
        hr = pFilter->QueryFilterInfo(&FilterInfo);
        if (FAILED(hr))
        {
            MessageBox(NULL, TEXT("Could not get the filter info"),
                TEXT("Error"), MB_OK | MB_ICONERROR);
            continue;  // Maybe the next one will work.
        }

#ifdef UNICODE
        MessageBox(NULL, FilterInfo.achName, TEXT("Filter Name"), MB_OK);
#else
        char szName[MAX_FILTER_NAME];
        int cch = WideCharToMultiByte(CP_ACP, 0, FilterInfo.achName,
            MAX_FILTER_NAME, szName, MAX_FILTER_NAME, 0, 0);
        if (cch > 0)
            MessageBox(NULL, szName, TEXT("Filter Name"), MB_OK);
#endif

        // The FILTER_INFO structure holds a pointer to the Filter Graph
        // Manager, with a reference count that must be released.
        if (FilterInfo.pGraph != NULL)
        {
            FilterInfo.pGraph->Release();
        }
        pFilter->Release();
    }

    pEnum->Release();
    return S_OK;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzählen von Objekten in einem Filter Graph](enumerating-objects-in-a-filter-graph.md)
</dt> </dl>

 

 



