---
description: In diesem Thema werden einige Hilfsfunktionen zum Verbinden von DirectShow-Filtern erläutert.
ms.assetid: cfd85944-7ae7-49e6-948f-9e190cdeed12
title: Zwei Filter verbinden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7e70e607c510490e7ed841ea44303153a94e83f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124868"
---
# <a name="connect-two-filters"></a>Zwei Filter verbinden

In diesem Thema werden einige Hilfsfunktionen zum Verbinden von DirectShow-Filtern erläutert.

Um zwei Filter miteinander zu verbinden, müssen Sie für den upstreamfilter eine nicht verbundene Ausgabe-PIN und für den downstreamfilter eine nicht verbundene Eingabe-PIN finden.

Wenn Sie bereits über Zeiger auf beide Pins verfügen, müssen Sie die [**igraphbuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) -Methode zum Herstellen einer Verbindung abrufen. Wenn die Pins keine direkte Verbindung herstellen können, fügt die **igraphbuilder:: Connect** -Methode möglicherweise zusätzliche Filter ein, um die Verbindung abzuschließen. Weitere Informationen finden Sie unter [Intelligent Connect](intelligent-connect.md).

Wenn Sie über einen Zeiger auf die Filter, aber nicht über die Pins verfügen, müssen Sie die [**ibasefilter:: enumpins**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) -Methode verwenden, um die Pins zu suchen. (Weitere Informationen finden Sie unter Auflisten von [Pins](enumerating-pins.md).) Diese Technik wird in den Hilfsfunktionen in diesem Thema veranschaulicht.

### <a name="output-pin-to-filter"></a>Anzufilternde Ausgabe-PIN

Die folgende Funktion nimmt zwei Parameter an: einen Zeiger auf eine Ausgabe-PIN und einen Zeiger auf einen Filter. Die-Funktion verbindet die Ausgabe-PIN mit der ersten verfügbaren Eingabe-PIN für den Filter.


```C++
// Connect output pin to filter.

HRESULT ConnectFilters(
    IGraphBuilder *pGraph, // Filter Graph Manager.
    IPin *pOut,            // Output pin on the upstream filter.
    IBaseFilter *pDest)    // Downstream filter.
{
    IPin *pIn = NULL;
        
    // Find an input pin on the downstream filter.
    HRESULT hr = FindUnconnectedPin(pDest, PINDIR_INPUT, &pIn);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pIn->Release();
    }
    return hr;
}
```



Diese Funktion führt Folgendes aus:

1.  Ruft die- `FindUnconnectedPin` Funktion auf, um eine nicht verbundene Eingabe-PIN zu erhalten. Diese Funktion wird im Thema [Suchen einer nicht verbundenen PIN für einen Filter](find-an-unconnected-pin-on-a-filter.md)gezeigt.
2.  Ruft [**igraphbuilder:: Connect**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) auf, um die beiden Pins zu verbinden.

### <a name="filter-to-input-pin"></a>An Eingabe-PIN Filtern

Die Next-Funktion nimmt einen Zeiger auf einen Filter und einen Zeiger auf eine Eingabe-PIN. Er verbindet die Eingabe-PIN mit dem ersten verfügbaren Ausgabepin für den Filter.


```C++
// Connect filter to input pin.

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IPin *pIn)
{
    IPin *pOut = NULL;
        
    // Find an output pin on the upstream filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        // Try to connect them.
        hr = pGraph->Connect(pOut, pIn);
        pOut->Release();
    }
    return hr;
}
```



### <a name="filter-to-filter"></a>Filter zum Filtern

Die dritte Funktion nimmt einen Zeiger auf einen upstreamfilter und einen Zeiger auf einen downstreamfilter und versucht, beide Filter zu verbinden.


```C++
// Connect filter to filter

HRESULT ConnectFilters(IGraphBuilder *pGraph, IBaseFilter *pSrc, IBaseFilter *pDest)
{
    IPin *pOut = NULL;

    // Find an output pin on the first filter.
    HRESULT hr = FindUnconnectedPin(pSrc, PINDIR_OUTPUT, &pOut);
    if (SUCCEEDED(hr))
    {
        hr = ConnectFilters(pGraph, pOut, pDest);
        pOut->Release();
    }
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Allgemeine Graph-Building Techniken](general-graph-building-techniques.md)
</dt> <dt>

[**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



