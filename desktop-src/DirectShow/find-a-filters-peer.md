---
description: Suchen eines Filter Peers
ms.assetid: 74d9fe65-f7f4-4971-9550-27884ac4146b
title: Suchen eines Filter Peers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1717f6ad61ad7310fdaa11ea5baaab4dcb7f8011
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041118"
---
# <a name="find-a-filters-peer"></a>Suchen eines Filter Peers

Bei einem Filter können Sie das Diagramm durchlaufen, indem Sie die Filter suchen, mit denen eine Verbindung besteht. Beginnen Sie mit dem Auflisten der Pins des Filters. Überprüfen Sie für jede PIN, ob diese PIN mit einer anderen Pin verbunden ist. Wenn dies der Fall ist, Fragen Sie die andere PIN nach Ihrem besitzenden Filter ab. Sie können das Diagramm in der Upstream-Richtung durchlaufen, indem Sie die Eingabe Pins des Filters oder in der Downstream-Richtung auflisten, indem Sie die Ausgabe Pins aufzählen.

Mit der folgenden Funktion wird Upstream oder Downstream nach einem verbundenen Filter durchsucht. Er gibt den ersten übereinstimmenden Filter zurück, den er findet:


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



Die Funktion ruft [**ibasefilter:: enumpins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) auf, um die Pins des ersten Filters aufzuzählen. Für jede PIN wird [**IPin:: querydirection**](/windows/desktop/api/Strmif/nf-strmif-ipin-querydirection) aufgerufen, um zu überprüfen, ob die PIN der angegebenen Richtung entspricht (Eingabe oder Ausgabe). Wenn dies der Fall ist, bestimmt die Funktion, ob diese PIN mit einer anderen Pin verbunden ist, indem die [**IPin:: connectedto**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto) -Methode aufgerufen wird. Schließlich wird [**IPin:: querypininfo**](/windows/desktop/api/Strmif/nf-strmif-ipin-querypininfo) für die verbundene Pin aufgerufen. Diese Methode gibt eine-Struktur zurück, die unter anderem einen Zeiger auf den besitzenden Filter der PIN enthält. Dieser Zeiger wird an den Aufrufer im *ppnext* -Parameter zurückgegeben. Der Aufrufer muss den Zeiger freigeben.

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



Ein Filter kann mit zwei oder mehr Filtern in beide Richtungen verbunden sein. Beispielsweise kann es sich um einen Splitter Filter mit mehreren nachgelagerten Filtern handeln. Möglicherweise handelt es sich um einen MUX-Filter mit mehreren vorgelagerten filtern. Daher sollten Sie alle in einer Liste erfassen.

Der folgende Code zeigt eine Möglichkeit, eine solche Funktion zu implementieren. Dabei wird die DirectShow [**cgenericlist**](cgenericlist.md) -Klasse verwendet. Sie können eine äquivalente Funktion mit einer anderen Datenstruktur schreiben.


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



Um die Dinge etwas komplizierter zu machen, kann ein Filter über mehrere Pin-Verbindungen mit dem gleichen Filter verfügen. Um zu vermeiden, dass Duplikate in die Liste aufgenommen werden, Fragen Sie jeden **ibasefilter** -Zeiger auf **IUnknown** ab und vergleichen die **IUnknown** -Zeiger. Durch die com-Regeln verweisen zwei Schnittstellen Zeiger auf dasselbe Objekt, wenn Sie identische **IUnknown** -Zeiger zurückgeben. Im vorherigen Beispiel verarbeitet die addfilterunique-Funktion dieses Detail.

Im folgenden Beispiel wird gezeigt, wie die getPeer Filters-Funktion verwendet wird:


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

 

 



