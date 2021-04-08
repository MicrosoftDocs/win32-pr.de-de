---
description: Übertragen von Typ-2-Datei
ms.assetid: c14c1798-aeff-44d8-a2e4-2fe4c146dfb9
title: Übertragen von Typ-2-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96e15cb0b3aae5b5119739f327a84204730c9d05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959940"
---
# <a name="transmit-from-type-2-file"></a>Übertragen von Typ-2-Datei

Verwenden Sie das in der folgenden Abbildung gezeigte Filter Diagramm, um eine Typ-2-Datei während der Vorschau zu übertragen.

![Type-2-Übertragung mit Vorschau](images/dv2-transmit.png)

Eine Type-2-Datei enthält zwei Streams, einen Audiostream und einen DV-codierten Videostream. Dieses Diagramm verwendet den [DV-Muxer](dv-muxer-filter.md) -Filter, um die Audiodaten und Videodaten Ströme zu kombinieren. Der überlappende Datenstrom wird an den msdv-Filter gesendet, der Stream wird jedoch für die Vorschau erneut unterteilt.

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



Dieser Code führt mehrere Aufrufe von **RenderStream** aus:

Die ersten beiden verbinden den Quell Filter mit dem avi-Splitter und dem avi-Splitter mit dem DV-MUX. Beim ersten Aufruf fügt der Erfassungs Diagramm-Generator automatisch den avi-Splitter zum Diagramm hinzu und verbindet einen der Ausgabe Pins des AVI-Splitters mit dem DV-MUX. Im zweiten Aufruf findet der Erfassungs Diagramm-Generator die zweite Ausgabe-PIN des AVI-Splitters und verbindet diese mit dem DV-MUX.

Der dritte Aufruf von **RenderStream** verbindet den DV-Muxer mit dem Filter für unendliche PIN. Beim nächsten-Rückruf wird ein Stream von der unbegrenzten PIN mit dem msdv-Erfassungs Filter verbunden. Dieser Stream wird an das Gerät übertragen. Der letzte Aufruf von **RenderStream** erstellt den Vorschau Abschnitt des Diagramms.

Wenn Sie die Vorschau während der Übertragung nicht anzeigen möchten, können Sie den unbegrenzten Pin-Empfänger weglassen und einfach die DV-MUX mit dem msdv-Filter verbinden:


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



