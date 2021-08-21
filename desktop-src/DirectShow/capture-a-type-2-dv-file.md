---
description: Erfassen einer Typ-2-DV-Datei
ms.assetid: c7d49c86-1b5d-43bf-98a5-78b297682375
title: Erfassen einer Typ-2-DV-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c944c84ed6cf04ec46de99a209a7b3d2942ae5157bc3ff9d14104da6615d03d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118158741"
---
# <a name="capture-a-type-2-dv-file"></a>Erfassen einer Typ-2-DV-Datei

Eine DV AVI-Datei vom Typ 2 verfügt über zwei Streams: einen mit DV-Video und einen mit Audio. Um eine Datei vom Typ 2 während der Vorschau zu erfassen, verwenden Sie das im folgenden Diagramm gezeigte Filterdiagramm.

![Type-2-Erfassung mit Vorschau](images/dv2-cap.png)

Dieses Diagramm entspricht fast dem Diagramm für die Erfassung vom Typ 1 (siehe [Erfassen einer Typ-1-DV-Datei).](capture-a-type-1-dv-file.md) Der Erfassungsstream durchläuft jedoch den [DV-Splitterfilter,](dv-splitter-filter.md) bevor er den [AVI Mux-Filter](avi-mux-filter.md) erreicht. Der AVI Mux empfängt daher zwei Streams: einen Audiostream und einen DV-codierten Videostream.

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



1.  Erstellen Sie den DV-Splitter, und fügen Sie ihn dem Filterdiagramm hinzu.
2.  Rufen Sie [**ICaptureGraphBuilder2::SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) auf, um den AVI Mux-Filter mit dem File Writer-Filter zu verbinden.
3.  Rufen Sie [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) auf, um den MSDV-Erfassungsfilter mit dem DV-Splitter zu verbinden. Dieser Aufruf verbindet auch einen der Ausgabepins des DV-Splitters mit dem AVI Mux.
4.  Rufen Sie RenderStream erneut auf, um den anderen Pin des DV-Splitters mit dem AVI Mux zu verbinden.
5.  Rufen Sie RenderStream ein drittes Mal auf, um den Vorschaustream zu rendern. Überspringen Sie diesen Schritt, wenn Sie keine Vorschau des Videos anzeigen möchten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



