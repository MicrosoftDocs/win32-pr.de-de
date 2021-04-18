---
description: Festlegen der diagrammuhr
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: Festlegen der diagrammuhr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe98c8dce1ab5f94664fbe1406c682e5d4e50b8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344312"
---
# <a name="setting-the-graph-clock"></a>Festlegen der diagrammuhr

Beim Erstellen eines Filter Diagramms wählt der Filter Diagramm-Manager automatisch eine Referenzuhr für das Diagramm aus. Alle Filter im Diagramm werden mit der Referenzuhr synchronisiert. Insbesondere rendererfilter verwenden die Referenzzeit, um die Präsentationszeit der einzelnen Stichproben zu bestimmen.

Es gibt in der Regel keinen Grund dafür, dass eine Anwendung die Auswahl der Referenzuhr des Filter-Graph-Managers außer Kraft setzt. Dies ist jedoch möglich, indem Sie die [**imediafilter:: setsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) -Methode für den Filter Graph-Manager aufrufen. Diese Methode nimmt einen Zeiger auf die **IReferenceClock** -Schnittstelle der Uhr. Ruft die-Methode auf, während das Diagramm angehalten wird.

Wenn ein Filter eine Uhr bereitstellt, können Sie den **IReferenceClock** -Zeiger abrufen, indem Sie **QueryInterface** für den Filter aufrufen. Alternativ können Sie eine externe verweisuhr implementieren, die nicht von einem Filter bereitgestellt wird, solange die externe Uhr **IReferenceClock** implementiert. Das folgende Beispiel zeigt, wie Sie eine Uhr angeben:


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



In diesem Beispiel wird davon ausgegangen, dass "conatemyprivateclock" eine Anwendungs definierte Funktion ist, die eine Uhr erstellt und einen **IReferenceClock** -Zeiger zurückgibt.

Sie können auch festlegen, dass das Filter Diagramm ohne Uhr ausgeführt wird, indem Sie **setsyncsource** mit dem Wert **null** aufrufen. Wenn keine Uhr vorhanden ist, wird das Diagramm so schnell wie möglich ausgeführt. Ohne Uhr warten rendererfilter nicht auf die Präsentationszeit eines Beispiels. Stattdessen wird jedes Beispiel so bald wie möglich dargestellt. Das Festlegen des Diagramms, das ohne eine Uhr ausgeführt wird, ist nützlich, wenn Sie Daten schnell verarbeiten möchten, anstatt Sie in Echtzeit anzuzeigen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grundlegende DirectShow-Aufgaben](basic-directshow-tasks.md)
</dt> <dt>

[**Cbasereferenceclock-Klasse**](cbasereferenceclock.md)
</dt> <dt>

[Uhrzeit und Uhren in DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



