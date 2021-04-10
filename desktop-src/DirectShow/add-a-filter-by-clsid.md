---
description: Filter nach CLSID hinzufügen
ms.assetid: b15cf324-5b9b-41da-a8cf-87071aaf3b60
title: Filter nach CLSID hinzufügen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f880ab1cb3b88fbe6d889acdd192bba341ce2acf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125324"
---
# <a name="add-a-filter-by-clsid"></a>Filter nach CLSID hinzufügen

Mit der folgenden Funktion wird ein Filter mit einem angegebenen Klassen Bezeichner (CLSID) erstellt und dem Filter Diagramm hinzugefügt:


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
> In diesem Beispiel wird die [saferelease](/windows/desktop/medfound/saferelease) -Funktion verwendet, um den [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Zeiger freizugeben.

 

Die Funktion ruft [**cokreateinstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) auf, um den Filter zu erstellen, und ruft dann [**ifiltergraph:: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) auf, um den Filter dem Diagramm hinzuzufügen. Im folgenden Codebeispiel wird diese Funktion verwendet, um dem Diagramm den [AVI MUX](avi-mux-filter.md) -Filter hinzuzufügen:


```C++
IBaseFilter *pMux;
hr = AddFilterByCLSID(pGraph, CLSID_AviDest, L"AVI Mux", &pMux, NULL); 
if (SUCCEEDED(hr))
{
    /* ... */
   pMux->Release();
}
```



Beachten Sie, dass einige Filter nicht mit [**cokreatanstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)erstellt werden können. Dies ist häufig der Fall bei Filtern, die andere Softwarekomponenten verwalten. Beispielsweise ist der [AVI-Kompressor](avi-compressor-filter.md) -Filter ein Wrapper für Video Codecs, und der [WDM-Video Erfassungs](wdm-video-capture-filter.md) Filter ist ein Wrapper für WDM-Erfassungs Treiber. Diese Filter müssen entweder mit dem [System Geräte-Enumerator](system-device-enumerator.md) oder dem [Filter Mapper](filter-mapper.md)erstellt werden. Weitere Informationen finden Sie unter Auflisten von [Geräten und Filtern](enumerating-devices-and-filters.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Graph-Building Techniken](general-graph-building-techniques.md)
</dt> </dl>

 

 
