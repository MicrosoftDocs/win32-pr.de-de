---
description: Übertragen von Einer Typ-2-Datei
ms.assetid: c14c1798-aeff-44d8-a2e4-2fe4c146dfb9
title: Übertragen von Einer Typ-2-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d1d6dec7c68cba177923dea04205d8dbc26faa8ff98cf5d6e79659fced46fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315715"
---
# <a name="transmit-from-type-2-file"></a>Übertragen von Einer Typ-2-Datei

Um eine Datei vom Typ 2 während der Vorschau zu übertragen, verwenden Sie das im folgenden Diagramm gezeigte Filterdiagramm.

![Type-2-Übertragung mit Vorschau](images/dv2-transmit.png)

Eine Typ-2-Datei verfügt über zwei Streams: einen Audiostream und einen DV-codierten Videodatenstrom. In diesem Diagramm wird der [DV Muxer-Filter](dv-muxer-filter.md) verwendet, um die Audio- und Videostreams zu kombinieren. Er sendet den überlappenden Stream an den MSDV-Filter, teilt den Stream jedoch erneut für die Vorschau auf.

Erstellen Sie dieses Diagramm wie folgt:


```C++
// Add the DV Mux filter to the graph.
IBaseFilter *pDVMux;
hr = CoCreateInstance(CLSID_DVMux, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVMux));
hr = pGraph->AddFilter(pDVMux, L"DV Mux");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(L"C:\\Example2.avi", L"Source", 
    &pFileSource);

hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pTee);
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pTee, 0, 0);
```



Dieser Code führt mehrere Aufrufe an **RenderStream** aus:

Die ersten beiden verbinden den Quellfilter mit dem AVI-Splitter und den AVI-Splitter mit dem DV Mux. Im ersten Aufruf fügt der Capture Graph Builder dem Graphen automatisch den AVI-Splitter hinzu und verbindet einen der Ausgabepins des AVI-Splitters mit dem DV Mux. Im zweiten Aufruf findet der Capture Graph Builder den zweiten Ausgabepin des AVI-Splitters und stellt eine Verbindung mit dem DV Mux her.

Der dritte Aufruf von **RenderStream** verbindet den DV Muxer mit dem Filter Infinite Pin Tee. Der nächste Aufruf verbindet einen Datenstrom vom Infinite Pin Tee mit dem MSDV-Erfassungsfilter. Dieser Stream wird an das Gerät übertragen. Der letzte Aufruf von **RenderStream** erstellt den Vorschauabschnitt des Diagramms.

Wenn Sie während der Übertragung keine Vorschau anzeigen möchten, können Sie die Unendliche Pin Tee weglassen und einfach den DV Mux mit dem MSDV-Filter verbinden:


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



