---
description: Suchen eines Filter-Peers
ms.assetid: 74d9fe65-f7f4-4971-9550-27884ac4146b
title: Suchen eines Filter-Peers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60d2f20a7145d2365e7ee1ec261ea861ddc5fa1eb01d0c3b2503f6f53fa25815
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118401764"
---
# <a name="find-a-filters-peer"></a>Suchen eines Filter-Peers

Bei einem Filter können Sie das Diagramm durchlaufen, indem Sie die Filter suchen, mit denen es verbunden ist. Beginnen Sie, indem Sie die Pins des Filters aufzählen. Überprüfen Sie für jeden Pin, ob dieser Stecknadel mit einem anderen Pin verbunden ist. Wenn ja, fragen Sie den anderen Pin nach seinem besitzenden Filter ab. Sie können das Diagramm in Upstreamrichtung durch aufzählen, indem Sie die Eingabepins des Filters aufzählen, oder in downstream-Richtung, indem Sie die Ausgabepins aufzählen.

Die folgende Funktion durchsucht upstream oder downstream nach einem verbundenen Filter. Sie gibt den ersten übereinstimmenden Filter zurück, der gefunden wird:


```C++
// Get the first upstream or downstream filter
HRESULT GetNextFilter(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    IBaseFilter **ppNext) // Receives a pointer to the next filter.
{
    if (!pFilter || !ppNext) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                pPin->Release();
                pEnum->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    return E_UNEXPECTED;
                }
                // This is the filter we're looking for.
                *ppNext = PinInfo.pFilter; // Client must release.
                return S_OK;
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    // Did not find a matching filter.
    return E_FAIL;
}
```



Die Funktion ruft [**IBaseFilter::EnumPins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) auf, um die Pins des ersten Filters aufzuzählen. Für jede Stecknadel ruft sie [**IPin::QueryDirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) auf, um zu überprüfen, ob der Stecknadel mit der angegebenen Richtung (Eingabe oder Ausgabe) übereinstimmt. Wenn ja, bestimmt die Funktion durch Aufrufen der [**IPin::ConnectedTo-Methode,**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) ob dieser Pin mit einem anderen Pin verbunden ist. Schließlich ruft sie [**IPin::QueryPinInfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) auf dem verbundenen Pin auf. Diese Methode gibt eine -Struktur zurück, die unter anderem einen Zeiger auf den besitzenden Filter dieses Pins enthält. Dieser Zeiger wird an den Aufrufer im *ppNext-Parameter* zurückgegeben. Der Aufrufer muss den Zeiger freigeben.

Der folgende Code zeigt, wie diese Funktion aufgerufen wird:


```C++
IBaseFilter *pF; // Pointer to some filter.
IBaseFilter *pUpstream = NULL;
if (SUCCEEDED(GetNextFilter(pF, PINDIR_INPUT, &pUpstream)))
{
    // Use pUpstream ...
    pUpstream->Release();
}
```



Ein Filter kann in beide Richtungen mit zwei oder mehr Filtern verbunden sein. Es kann sich z. B. um einen Splitterfilter mit mehreren Filtern nachgeschaltet haben. Oder es kann sich um einen mux-Filter mit mehreren Upstreamfiltern aus diesem filtert. Aus diesem Grund sollten Sie alle in einer Liste erfassen.

Der folgende Code zeigt eine mögliche Möglichkeit, eine solche Funktion zu implementieren. Es wird die [**DirectShow CGenericList-Klasse**](cgenericlist.md) verwendet. Sie könnten eine entsprechende Funktion mithilfe einer anderen Datenstruktur schreiben.


```C++
#include <streams.h>  // Link to the DirectShow base class library
// Define a typedef for a list of filters.
typedef CGenericList<IBaseFilter> CFilterList;

// Forward declaration. Adds a filter to the list unless it's a duplicate.
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew);

// Find all the immediate upstream or downstream peers of a filter.
HRESULT GetPeerFilters(
    IBaseFilter *pFilter, // Pointer to the starting filter
    PIN_DIRECTION Dir,    // Direction to search (upstream or downstream)
    CFilterList &FilterList)  // Collect the results in this list.
{
    if (!pFilter) return E_POINTER;

    IEnumPins *pEnum = 0;
    IPin *pPin = 0;
    HRESULT hr = pFilter->EnumPins(&pEnum);
    if (FAILED(hr)) return hr;
    while (S_OK == pEnum->Next(1, &pPin, 0))
    {
        // See if this pin matches the specified direction.
        PIN_DIRECTION ThisPinDir;
        hr = pPin->QueryDirection(&ThisPinDir);
        if (FAILED(hr))
        {
            // Something strange happened.
            hr = E_UNEXPECTED;
            pPin->Release();
            break;
        }
        if (ThisPinDir == Dir)
        {
            // Check if the pin is connected to another pin.
            IPin *pPinNext = 0;
            hr = pPin->ConnectedTo(&pPinNext);
            if (SUCCEEDED(hr))
            {
                // Get the filter that owns that pin.
                PIN_INFO PinInfo;
                hr = pPinNext->QueryPinInfo(&PinInfo);
                pPinNext->Release();
                if (FAILED(hr) || (PinInfo.pFilter == NULL))
                {
                    // Something strange happened.
                    pPin->Release();
                    pEnum->Release();
                    return E_UNEXPECTED;
                }
                // Insert the filter into the list.
                AddFilterUnique(FilterList, PinInfo.pFilter);
                PinInfo.pFilter->Release();
            }
        }
        pPin->Release();
    }
    pEnum->Release();
    return S_OK;
}
void AddFilterUnique(CFilterList &FilterList, IBaseFilter *pNew)
{
    if (pNew == NULL) return;

    POSITION pos = FilterList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pF = FilterList.GetNext(pos);
        if (IsEqualObject(pF, pNew))
        {
            return;
        }
    }
    pNew->AddRef();  // The caller must release everything in the list.
    FilterList.AddTail(pNew);
}
```



Um dies etwas zu erschweren, kann ein Filter mehrere Stecknadelverbindungen mit demselben Filter aufweisen. Um zu vermeiden, dass Duplikate in die Liste aufgenommen werden, fragen Sie jeden **IBaseFilter-Zeiger** nach **IUnknown** ab, und vergleichen Sie die **IUnknown-Zeiger.** Nach den Regeln von COM verweisen zwei Schnittstellenzeiger nur dann auf dasselbe Objekt, wenn sie identische **IUnknown-Zeiger** zurückgeben. Im vorherigen Beispiel behandelt die AddFilterUnique-Funktion dieses Detail.

Das folgende Beispiel zeigt die Verwendung der GetPeerFilters-Funktion:


```C++
IBaseFilter *pF; // Pointer to some filter.
CFilterList FList(NAME("MyList"));  // List to hold the downstream peers.
hr = GetPeerFilters(pF, PINDIR_OUTPUT, FList);
if (SUCCEEDED(hr))
{
    POSITION pos = FList.GetHeadPosition();
    while (pos)
    {
        IBaseFilter *pDownstream = FList.GetNext(pos);
        pDownstream->Release();
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Graph-Building Techniken](general-graph-building-techniques.md)
</dt> </dl>

 

 



