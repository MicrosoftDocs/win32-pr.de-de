---
description: Übertragen von Datei vom Typ "-1"
ms.assetid: 5be2248b-7917-4c1b-9ae7-29e06779eac6
title: Übertragen von Datei vom Typ "-1"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e38ed3e549b6cd671248ba1df9b24df8fbfe3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042410"
---
# <a name="transmit-from-type-1-file"></a>Übertragen von Datei vom Typ "-1"

Verwenden Sie das in der folgenden Abbildung gezeigte Filter Diagramm, um eine Datei vom Typ 1 zu übertragen, während Sie die Datei in der Vorschau anzeigen.

![Type-1-Übertragung mit Vorschau](images/dv1-transmit.png)

Die Filter in diesem Diagramm umfassen Folgendes:

-   Der [avi-Splitter](avi-splitter-filter.md) analysiert die AVI-Datei. Für eine DV-Datei vom Typ "1" liefert die Ausgabe-PIN verschachtelte DV-Beispiele.
-   Der [unendliche Pin-Tee](infinite-pin-tee-filter.md) -Filter teilt den verschachtelten DV in einen übertragungstream und einen Vorschau Datenstrom. Beide Streams enthalten die gleichen verschachtelten Daten. (Dieses Diagramm verwendet den unendlichen Pin-Tee anstelle des [intelligenten Ausstellers](smart-tee-filter.md), da es keine Gefahr gibt, Rahmen beim Lesen aus einer Datei zu löschen, wie es bei Live Capture der Fall ist.)
-   Der [DV-Splitter](dv-splitter-filter.md) teilt den verschachtelten Stream in einen DV-Videostream, der vom [DV-Video Decoder](dv-video-decoder-filter.md)und einem Audiostream decodiert wird. Beide Streams sind rendererd für die Vorschau.

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



1.  Aufrufen von [**igraphbuilder:: addsourcefilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) zum Hinzufügen des Quell Filters zum Filter Diagramm.
2.  Erstellen Sie den avi-Splitter und den unbegrenzten Pin-Tee, und fügen Sie Sie dem Diagramm hinzu.
3.  Ruft [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) auf, um den Quell Filter mit dem avi-Splitter zu verbinden. Angeben von MediaType \_ , um sicherzustellen, dass die Methode fehlschlägt, wenn die Quelldatei keine Type-1-DV-Datei ist. In diesem Fall können Sie den Typ-2-Übertragungs Graph stattdessen wiederherstellen und versuchen, ein Diagramm vom Typ 2 zu erstellen.
4.  **RenderStream** erneut aufgerufen, um den überlappenden Stream vom avi-Splitter an den unbegrenzten Pin-Empfänger weiterzuleiten
5.  RenderStream wird ein drittes Mal aufgerufen, um einen Stream vom unbegrenzten Pin-Empfänger an den msdv-Filter für die Übertragung an das Gerät weiterzuleiten.
6.  **RenderStream** ein letztes Mal aufgerufen, um den Vorschau Abschnitt des Diagramms zu erstellen.

Wenn Sie die Vorschau nicht wünschen, verbinden Sie einfach die Datei Quelle mit dem msdv-Filter:


```C++
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pFileSource, 0, pDV);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



