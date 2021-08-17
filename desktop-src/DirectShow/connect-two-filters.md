---
description: In diesem Thema werden einige Hilfsfunktionen zum Verbinden von DirectShow-Filtern gezeigt.
ms.assetid: cfd85944-7ae7-49e6-948f-9e190cdeed12
title: Verbinden Zwei Filter
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab83e8608c088fde6d06c0a44621f1c066f177ecf76cbc8ba3f55d31218b49ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118954209"
---
# <a name="connect-two-filters"></a>Verbinden Zwei Filter

In diesem Thema werden einige Hilfsfunktionen zum Verbinden von DirectShow-Filtern gezeigt.

Um zwei Filter zu verbinden, müssen Sie einen nicht verbundenen Ausgabepin im Upstreamfilter und einen nicht verbundenen Eingabepin für den Downstreamfilter finden.

Wenn Sie bereits Zeiger auf beide Stecknadeln haben, rufen Sie die [**IGraphBuilder::Verbinden-Methode**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) auf, um sie zu verbinden. Wenn die Pins nicht direkt miteinander verbunden werden können, fügt die **IGraphBuilder::Verbinden-Methode** möglicherweise zusätzliche Filter ein, um die Verbindung herzustellen. Weitere Informationen finden Sie unter [Intelligent Verbinden](intelligent-connect.md).

Wenn Sie einen Zeiger auf die Filter, aber nicht die Stecknadeln haben, müssen Sie die [**IBaseFilter::EnumPins-Methode**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-enumpins) verwenden, um die Stecknadeln zu finden. (Siehe [Enumerating Pins](enumerating-pins.md).) Die Hilfsfunktionen in diesem Thema veranschaulichen diese Technik.

### <a name="output-pin-to-filter"></a>An Filter anheften der Ausgabe

Die folgende Funktion verwendet zwei Parameter: einen Zeiger auf einen Ausgabepin und einen Zeiger auf einen Filter. Die Funktion verbindet den Ausgabepin mit dem ersten verfügbaren Eingabepin im Filter.


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

1.  Ruft die `FindUnconnectedPin` Funktion auf, um einen nicht verbundenen Eingabepin zu erhalten. Diese Funktion wird im Thema Suchen einer [nicht verbundenen Stecknadel in einem Filter gezeigt.](find-an-unconnected-pin-on-a-filter.md)
2.  Ruft [**IGraphBuilder::Verbinden**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-connect) auf, um die beiden Stecknadeln zu verbinden.

### <a name="filter-to-input-pin"></a>Filtern nach Eingabepin

Die nächste Funktion verwendet einen Zeiger auf einen Filter und einen Zeiger auf einen Eingabepin. Er verbindet den Eingabepin mit dem ersten verfügbaren Ausgabepin im Filter.


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



### <a name="filter-to-filter"></a>Filtern nach Filter

Die dritte Funktion verwendet einen Zeiger auf einen Upstreamfilter und einen Zeiger auf einen Downstreamfilter und versucht, beide Filter zu verbinden.


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

[**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream)
</dt> </dl>

 

 



