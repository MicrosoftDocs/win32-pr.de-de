---
description: Erfassen einer DV-Datei vom Typ "1"
ms.assetid: fba11e9b-4900-4b29-a0c9-702272cd7387
title: Erfassen einer DV-Datei vom Typ "1"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8098669f124bdd4c0168e3549cd8eed8e1825c47
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104558947"
---
# <a name="capture-a-type-1-dv-file"></a>Erfassen einer DV-Datei vom Typ "1"

Eine "Type-1 DV AVI"-Datei enthält einen einzelnen überlappenden Datenstrom. Verwenden Sie das in der folgenden Abbildung gezeigte Filter Diagramm, um eine Datei vom Typ 1 zu erfassen, während die Vorschau angezeigt wird.

![Typ-1-Erfassung mit Vorschau](images/dv1-cap.png)

Die Filter in diesem Diagramm umfassen Folgendes:

-   Der [Smart Tee](smart-tee-filter.md) -Filter teilt den überlappenden DV in einen Aufzeichnungsdaten Strom und einen Vorschau Datenstrom. Beide Streams enthalten die gleichen verschachtelten Daten.
-   Der [AVI MUX](avi-mux-filter.md) und der [dateiwriter](file-writer-filter.md) schreiben den verschachtelten Stream auf den Datenträger.
-   Der [DV-Splitter](dv-splitter-filter.md) teilt den verschachtelten Stream in einen DV-Videostream und einen Audiodatenstrom. Beide Streams sind rendererd für die Vorschau.
-   Der [DV-Video-Decoder](dv-video-decoder-filter.md) decodiert den DV-Videodaten Strom für die Vorschau.

Erstellen Sie dieses Diagramm wie folgt:


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example1.avi"), &pAviMux, 0);

// Render the capture stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved,
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  Aufrufen von [**ICaptureGraphBuilder2:: setoutputfilename**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) , um den AVI MUX-Filter mit dem dateiwriter-Filter zu verbinden.
2.  Ruft [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) mit der PIN Category Pin \_ Category \_ Capture auf, um den Aufzeichnungsdaten Strom zu rendern. Der Erfassungs Diagramm-Generator fügt automatisch den intelligenten Tee-Filter ein.
3.  RenderStream erneut aufzurufen, aber mit der PIN Category Pin \_ Category \_ Preview, um den Vorschau Datenstrom zu rendern. Überspringen Sie diesen Befehl, wenn Sie das Video nicht in der Vorschau anzeigen möchten.

Bei beiden Aufrufen von RenderStream ist MediaType überlappende der Medientyp, d. h. überlappende \_ DV-Videos. In diesem Code fügt der Erfassungs Diagramm-Generator automatisch jeden benötigten Filter hinzu, mit Ausnahme des msdv-Erfassungs Filters.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



