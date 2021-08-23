---
description: Übertragen von Einer Datei vom Typ 1
ms.assetid: 5be2248b-7917-4c1b-9ae7-29e06779eac6
title: Übertragen von Einer Datei vom Typ 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e62ce67627c350c24de1bf1ee96ba7804ac3f164264e167498c597e8136ea138
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119015532"
---
# <a name="transmit-from-type-1-file"></a>Übertragen von Einer Datei vom Typ 1

Um eine Datei vom Typ 1 während der Vorschau der Datei zu übertragen, verwenden Sie das im folgenden Diagramm gezeigte Filterdiagramm.

![Type-1-Übertragung mit Vorschau](images/dv1-transmit.png)

Filter in diesem Diagramm umfassen Folgendes:

-   Der [AVI-Splitter](avi-splitter-filter.md) analysiert die AVI-Datei. Für eine DV-Datei vom Typ 1 stellt der Ausgabepin verschachtelte DV-Beispiele bereit.
-   Der [Filter Infinite Pin Tee](infinite-pin-tee-filter.md) teilt die überlappende DV in einen Übertragungsstream und einen Vorschaudatenstrom auf. Beide Streams enthalten dieselben überlappende Daten. (In diesem Diagramm wird die Unendliche Pin Tee anstelle von [Smart Tee](smart-tee-filter.md)verwendet, da beim Lesen aus einer Datei keine Gefahr besteht, Frames zu löschen, wie es bei live capture der Fall ist.)
-   Der [DV-Splitter](dv-splitter-filter.md) teilt den überlappenden Stream in einen DV-Videostream auf, der vom [DV-Videodecoder](dv-video-decoder-filter.md)decodiert wird, und einen Audiostream. Beide Streams werden für die Vorschau gerendert.

Erstellen Sie dieses Diagramm wie folgt:


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(
    L"C:\\YourFileNameHere.avi",
    L"Source", 
    &pFileSource);

// Add the AVI Splitter filter to the graph.
IBaseFilter *pAviSplit;
hr = CoCreateInstance(CLSID_AviSplitter, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pAviSplit));
hr = pGraph->AddFilter(pAviSplit, L"AVI Splitter");

// Connect the file source to the AVI Splitter.
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pAviSplit);
if (FAILED(hr))
{
    // This is not an AVI file. 
}

// Connect the file source to the Infinite Pin Tee.
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pAviSplit, 0, pTee);
if (FAILED(hr))
{
    // This is not a type-1 DV file.
}

// Render one stream from the Infinite Pin Tee to MSDV, for transmit.
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);

// Render another stream from the Infinite Pin Tee for preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



1.  Rufen Sie [**IGraphBuilder::AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) auf, um dem Filterdiagramm den Quellfilter hinzuzufügen.
2.  Erstellen Sie den AVI-Splitter und den Infinite Pin Tee, und fügen Sie sie dem Diagramm hinzu.
3.  Rufen Sie [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) auf, um den Quellfilter mit dem AVI-Splitter zu verbinden. Geben Sie MEDIATYPE \_ Interleaved an, um sicherzustellen, dass die Methode fehlschlägt, wenn es sich bei der Quelldatei nicht um eine DV-Datei vom Typ 1 handelt. In diesem Fall können Sie ein Back-Out ausführen und stattdessen versuchen, ein Typ-2-Übertragungsdiagramm zu erstellen.
4.  Rufen Sie **RenderStream** erneut auf, um den verschachtelten Stream vom AVI-Splitter an die Unendliche Pin Tee weiterzuleiten.
5.  Rufen Sie RenderStream ein drittes Mal auf, um einen Stream vom Infinite Pin Tee an den MSDV-Filter für die Übertragung an das Gerät weiterzuleiten.
6.  Rufen Sie **RenderStream** ein letztes Mal auf, um den Vorschauabschnitt des Diagramms zu erstellen.

Wenn Sie keine Vorschauversion wünschen, verbinden Sie einfach die Dateiquelle mit dem MSDV-Filter:


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



