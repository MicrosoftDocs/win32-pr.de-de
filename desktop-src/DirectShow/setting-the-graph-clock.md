---
description: Festlegen der Graph Uhr
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: Festlegen der Graph Uhr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ab93fcefe4ba88aa7724bf59b775c493313783b2f4ad3801925e16b9a1818c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904140"
---
# <a name="setting-the-graph-clock"></a>Festlegen der Graph Uhr

Wenn Sie ein Filterdiagramm erstellen, wählt der Filter-Graph-Manager automatisch eine Referenzuhr für das Diagramm aus. Alle Filter im Diagramm werden mit der Referenzuhr synchronisiert. Insbesondere verwenden Rendererfilter die Referenzuhr, um die Präsentationszeit der einzelnen Stichproben zu bestimmen.

Es gibt in der Regel keinen Grund dafür, dass eine Anwendung den Filter Graph die Auswahl der Verweisuhr durch den Manager außer Kraft setzt. Sie können dies jedoch tun, indem Sie die [**IMediaFilter::SetSyncSource-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) im Filter Graph Manager aufrufen. Diese Methode verwendet einen Zeiger auf die **IReferenceClock-Schnittstelle der** Uhr. Rufen Sie die -Methode auf, während das Diagramm beendet wird.

Wenn ein Filter eine Uhr enthält, können Sie den **IReferenceClock-Zeiger** durch Aufrufen **von QueryInterface für** den Filter erhalten. Alternativ können Sie eine externe Referenzuhr implementieren, die nicht von einem Filter bereitgestellt wird, solange Ihre externe Uhr **IReferenceClock implementiert.** Das folgende Beispiel zeigt, wie eine Uhr angegeben wird:


```C++
IGraphBuilder *pGraph = 0;
IReferenceClock *pClock = 0;

CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
    IID_IGraphBuilder, (void **)&pGraph);

// Build the graph.
pGraph->RenderFile(L"C:\\Example.avi", 0);

// Create your clock.
hr = CreateMyPrivateClock(&pClock);
if (SUCCEEDED(hr))
{
    // Set the graph clock.
    IMediaFilter *pMediaFilter = 0;
    pGraph->QueryInterface(IID_IMediaFilter, (void**)&pMediaFilter);
    pMediaFilter->SetSyncSource(pClock);
    pClock->Release();
    pMediaFilter->Release();
}
```



In diesem Beispiel wird davon ausgegangen, dass CreateMyPrivateClock eine anwendungsdefinierte Funktion ist, die eine Uhr erstellt und einen **IReferenceClock-Zeiger** zurückgibt.

Sie können auch festlegen, dass das Filterdiagramm ohne Uhr ausgeführt wird, indem **Sie SetSyncSource mit** dem Wert **NULL aufrufen.** Wenn keine Uhr verfügbar ist, wird das Diagramm so schnell wie möglich ausgeführt. Ohne Uhr warten Rendererfilter nicht auf die Präsentationszeit eines Beispiels. Stattdessen rendern sie jedes Beispiel, sobald es eintrifft. Das Festlegen der Ausführung des Graphen ohne Uhr ist nützlich, wenn Sie Daten schnell verarbeiten möchten, anstatt sie in Echtzeit in der Vorschau anzuzeigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende DirectShow-Aufgaben](basic-directshow-tasks.md)
</dt> <dt>

[**CBaseReferenceClock-Klasse**](cbasereferenceclock.md)
</dt> <dt>

[Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



