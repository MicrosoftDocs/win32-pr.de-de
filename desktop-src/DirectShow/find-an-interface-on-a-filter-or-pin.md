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
# <a name="find-an-interface-on-a-filter-or-pin"></a>Suchen einer Schnittstelle in einem Filter oder einer PIN

Bei vielen Vorgängen in DirectShow Ruft die Anwendung Methoden für den Filter Graph-Manager auf. In einigen Situationen muss die Anwendung jedoch eine Methode direkt für einen Filter oder eine PIN aufruft. Viele Filter machen z. b. spezielle Schnittstellen verfügbar, die zum Konfigurieren des Filters verwendet werden.

Im Fall einer Filter Schnittstelle verfügen Sie möglicherweise bereits über einen Zeiger auf die [**ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) -Schnittstelle des Filters. Verwenden Sie in diesem Fall einfach **QueryInterface** , um die andere Schnittstelle zu erhalten. Einige Filter können dem Diagramm jedoch vom Filter Graph-Manager hinzugefügt werden. (Ausführliche Informationen finden Sie unter [Intelligent Connect](intelligent-connect.md).) Verwenden Sie in diesem Fall die Schnittstelle [**ienumfilters**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) , um alle Filter im Diagramm zu durchlaufen und nacheinander abzufragen. Dies wird in der folgenden Funktion veranschaulicht:


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



Um eine Schnittstelle in einer PIN zu finden, verwenden Sie die [**iumumpins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) -Schnittstelle, um die Pins eines Filters zu durchlaufen. Die folgende Funktion zeigt die Vorgehensweise:


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



Die Next-Funktion sucht nach einer Schnittstelle in einem Filter oder einer PIN:


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



Beachten Sie, dass alle hier gezeigten Funktionen bei der ersten erfolgreichen **QueryInterface** angehalten werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Auflisten von Filtern](enumerating-filters.md)
</dt> <dt>

[Auflisten von Pins](enumerating-pins.md)
</dt> <dt>

[**ICaptureGraphBuilder2:: findinterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



