---
description: Hinzufügen eines Filters nach CLSID
ms.assetid: b15cf324-5b9b-41da-a8cf-87071aaf3b60
title: Hinzufügen eines Filters nach CLSID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed8306613e5a73ad863b3c16b04529e3e0def12b76fb4e27685db9cb442b6c80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873430"
---
# <a name="add-a-filter-by-clsid"></a>Hinzufügen eines Filters nach CLSID

Die folgende Funktion erstellt einen Filter mit einem angegebenen Klassenbezeichner (CLSID) und fügt ihn dem Filterdiagramm hinzu:


```C++
// Create a filter by CLSID and add it to the graph.

HRESULT AddFilterByCLSID(
    IGraphBuilder *pGraph,      // Pointer to the Filter Graph Manager.
    REFGUID clsid,              // CLSID of the filter to create.
    IBaseFilter **ppF,          // Receives a pointer to the filter.
    LPCWSTR wszName             // A name for the filter (can be NULL).
    )
{
    *ppF = 0;

    IBaseFilter *pFilter = NULL;
    
    HRESULT hr = CoCreateInstance(clsid, NULL, CLSCTX_INPROC_SERVER, 
        IID_PPV_ARGS(&pFilter));
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pGraph->AddFilter(pFilter, wszName);
    if (FAILED(hr))
    {
        goto done;
    }

    *ppF = pFilter;
    (*ppF)->AddRef();

done:
    SafeRelease(&pFilter);
    return hr;
}
```



> [!Note]  
> In diesem Beispiel wird die [SafeRelease-Funktion](/windows/desktop/medfound/saferelease) verwendet, um den [**IBaseFilter-Zeiger**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) frei zu geben.

 

Die Funktion ruft [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um den Filter zu erstellen, und ruft dann [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) auf, um den Filter zum Diagramm hinzuzufügen. Im folgenden Codebeispiel wird diese Funktion verwendet, um dem [Diagramm den FILTER AVI Mux](avi-mux-filter.md) hinzuzufügen:


```C++
IBaseFilter *pMux;
hr = AddFilterByCLSID(pGraph, CLSID_AviDest, L"AVI Mux", &pMux, NULL); 
if (SUCCEEDED(hr))
{
    /* ... */
   pMux->Release();
}
```



Beachten Sie, dass einige Filter nicht mit [**CoCreateInstance erstellt werden können.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Dies ist häufig bei Filtern der Fall, die andere Softwarekomponenten verwalten. Beispielsweise ist der [FILTER AVI-11](avi-compressor-filter.md) ein Wrapper für Videocodecs, und der [WDM-Videoerfassungsfilter](wdm-video-capture-filter.md) ist ein Wrapper für WDM-Erfassungstreiber. Diese Filter müssen entweder mit dem [Systemgeräte-Enumerator](system-device-enumerator.md) oder dem [Filter-Mapper erstellt werden.](filter-mapper.md) Weitere Informationen finden Sie unter [Aufzählen von Geräten und Filtern.](enumerating-devices-and-filters.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Graph-Building Techniken](general-graph-building-techniques.md)
</dt> </dl>

 

 
