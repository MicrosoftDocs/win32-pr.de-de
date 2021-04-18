---
description: Auflisten von Filtern
ms.assetid: 57bcaa4d-37bf-457d-937e-f9d24fb5784f
title: Auflisten von Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2de0f979973d339b790b04a8a5d4d98fc52c95c6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106340073"
---
# <a name="enumerating-filters"></a>Auflisten von Filtern

Der Filter Graph-Manager unterstützt die [**ifiltergraph:: enumfilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-enumfilters) -Methode, die alle Filter im Filter Diagramm auflistet. Er gibt einen Zeiger auf die [**ienumfilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) -Schnittstelle zurück. Die [**ienumfilters:: Next**](/windows/desktop/api/Strmif/nf-strmif-ienumfilters-next) -Methode ruft [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstellen Zeiger ab.

Das folgende Beispiel zeigt eine Funktion, die die Filter in einem Diagramm auflistet und ein Meldungs Feld mit den Namen der einzelnen Filter anzeigt. Er verwendet die [**ibasefilter:: queryfilterinfo**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-queryfilterinfo) -Methode, um den Namen des Filters abzurufen. Beachten Sie die stellen, an denen die Funktion **Release** für eine Schnittstelle aufruft, um den Verweis Zähler zu verringern.


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

[Auflisten von Objekten in einem Filter Diagramm](enumerating-objects-in-a-filter-graph.md)
</dt> </dl>

 

 



