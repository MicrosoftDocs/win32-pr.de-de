---
description: Suchen einer Schnittstelle für einen Filter oder eine Stecknadel
ms.assetid: 546f5b7d-3bcd-4e97-a012-daca6ae7bca1
title: Suchen einer Schnittstelle für einen Filter oder eine Stecknadel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17314f7e44e4b2c4f412dd0d152e038203268c29d585cd684ddde9eb34992a2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819562"
---
# <a name="find-an-interface-on-a-filter-or-pin"></a>Suchen einer Schnittstelle für einen Filter oder eine Stecknadel

Bei vielen Vorgängen in DirectShow ruft die Anwendung Methoden im Filter Graph Manager auf. In einigen Situationen muss die Anwendung jedoch eine Methode direkt auf einem Filter oder pin aufrufen. Viele Filter machen z. B. spezielle Schnittstellen verfügbar, die zum Konfigurieren des Filters verwendet werden.

Im Fall einer Filterschnittstelle verfügen Sie möglicherweise bereits über einen Zeiger auf die [**IBaseFilter-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) des Filters. Verwenden Sie in diesem Fall einfach **QueryInterface,** um die andere Schnittstelle abzurufen. Einige Filter werden dem Diagramm jedoch möglicherweise vom Filter Graph Manager hinzugefügt. (Weitere Informationen finden Sie unter [Intelligent Verbinden](intelligent-connect.md).) Verwenden Sie in diesem Fall die [**IEnumFilters-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-ienumfilters) um alle Filter im Diagramm zu durchlaufen und nacheinander abzufragen. Die folgende Funktion veranschaulicht dies:


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



Um eine Schnittstelle auf einem Pin zu finden, verwenden Sie die [**IEnumPins-Schnittstelle,**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) um die Stecknadeln eines Filters zu durchlaufen. Die folgende Funktion zeigt, wie Dies geschieht:


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



Die nächste Funktion sucht nach einer Schnittstelle für einen Filter oder einen Pin:


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



Beachten Sie, dass alle hier gezeigten Funktionen bei der ersten erfolgreichen **QueryInterface** beendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufzählen von Filtern](enumerating-filters.md)
</dt> <dt>

[Aufzählen von Pins](enumerating-pins.md)
</dt> <dt>

[**ICaptureGraphBuilder2::FindInterface**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findinterface)
</dt> </dl>

 

 



