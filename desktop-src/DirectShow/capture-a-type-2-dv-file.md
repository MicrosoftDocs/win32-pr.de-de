---
description: Erfassung einer Type-2-DV-Datei
ms.assetid: c7d49c86-1b5d-43bf-98a5-78b297682375
title: Erfassung einer Type-2-DV-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919928a4c02ce9e3f3f3e6fcf3d2cd376f880a8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860033"
---
# <a name="capture-a-type-2-dv-file"></a>Erfassung einer Type-2-DV-Datei

Eine Type-2-DV-AVI-Datei enthält zwei Streams, eine mit DV-Video und eine andere, die Audiodaten enthält. Verwenden Sie das in der folgenden Abbildung gezeigte Filter Diagramm, um eine Datei vom Typ 2 zu erfassen, während die Vorschau angezeigt wird.

![Typ-2-Erfassung mit Vorschau](images/dv2-cap.png)

Dieses Diagramm ist fast identisch mit dem Diagramm für die Erfassung von Type-1 (siehe [Capture a Type-1 DV File](capture-a-type-1-dv-file.md)). Der Erfassungsdaten Strom durchläuft jedoch den [DV-Splitter](dv-splitter-filter.md) Filter, bevor der [AVI MUX](avi-mux-filter.md) -Filter erreicht wird. Der AVI-MUX empfängt daher zwei Streams, einen Audiostream und einen DV-codierten Videostream.

Erstellen Sie dieses Diagramm wie folgt:


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.
IBaseFilter           *pDVSplit;  // DV Splitter

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the DV Splitter and add it to the filter graph.
hr = CoCreateInstance(CLSID_DVSplitter, 0, CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVSplit));
hr = pGraph->AddFilter(pDVSplit, L"DV Splitter");

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi,
    OLESTR("C:\\Example2.avi"), &pAviMux, 0);

// Connect the capture pin to the DV Splitter, and render one stream from
// the DV Splitter to the AVI Mux. 
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, pDVSplit, pAviMux);

// Render the other stream from the DV splitter to the AVI Mux.
hr = pBuilder->RenderStream(0, 0, pDVSplit, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved, 
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  Erstellen Sie den DV-Splitter, und fügen Sie ihn dem Filter Diagramm hinzu.
2.  Aufrufen von [**ICaptureGraphBuilder2:: setoutputfilename**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) , um den AVI MUX-Filter mit dem dateiwriter-Filter zu verbinden.
3.  [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) zum Verbinden des msdv-Erfassungs Filters mit dem DV-Splitter aufruft. Dieser Befehl verbindet auch einen der Ausgabe Pins des DV-Splitters mit dem AVI MUX.
4.  RenderStream erneut aufgerufen, um die andere PIN des DV-Splitters mit dem AVI-MUX zu verbinden.
5.  RenderStream wird ein drittes Mal aufgerufen, um den Vorschau Datenstrom zu rendern. Überspringen Sie diesen Schritt, wenn Sie das Video nicht in der Vorschau anzeigen möchten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



