---
description: Erfassen von DV in unkomprimiertem RGB
ms.assetid: 02b54070-09c8-45ab-8a08-1493008a5e1f
title: Erfassen von DV in unkomprimiertem RGB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb721dba2912774dd7cad18871484a9d578458161d78ea402261858cac03aa65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966765"
---
# <a name="capture-dv-to-uncompressed-rgb"></a>Erfassen von DV in unkomprimiertem RGB

In diesem Beispiel wird gezeigt, wie Sie DV aus dem Dvd-Speicher erfassen und während der Vorschau als unkomprimiertes RGB in einer Datei speichern. Verwenden Sie das Im folgenden Diagramm dargestellte Filterdiagramm.

![Erfassen von unkomprimierten RGB-Daten in einer Datei](images/dv-rgb-cap.png)

Der DV-Splitterfilter teilt das verleerte Audio/Video in separate Video- und Audiostreams auf. Das DV-codierte Video wird an den [DV-Videodecoder-Filter](dv-video-decoder-filter.md) übertragen, der unkomprimierte RGB-Videos ausausgabet. Das RGB-Video wird über den Smart Tee-Filter an den AVI Mux-Filter (zur Erfassung) und den Videorenderer (vorschau) geroutet. In der Zwischenzeit durchläuft der Audiodatenstrom aus dem DV-Splitter den Filter Infinite Pin Tee an den AVI Mux und den Audiorenderer. Der Filter Graph-Manager hält alle diese Datenströme synchronisiert, indem die Zeitstempel in den Beispielen und die Graphreferenzuhr verwendet werden.

Dieses Diagramm mag unnötig kompliziert erscheinen, stellt aber sicher, dass der DV-codierte Videostream nur einmal decodiert wird, wodurch die CPU-Anforderungen minimiert werden. Beachten Sie außerdem, dass das Video den Smart Tee-Filter durchläuft, während das Audio den Filter Infinite Pin Tee durchläuft. Smart Tee kann Vorschauframes zur Verbesserung der Erfassungsleistung ablegen. Dies ist für Videos wünschenswert, aber nicht für Audioinhalte, bei denen verworfene Stichproben deutlich zu sehen sind. Da das Audio viel weniger Bandbreite als das Video erfordert, besteht außerdem relativ wenig Wahrscheinlichkeit, audio in der Datei zu löschen.

Sie müssen dieses Diagramm abschnittsweise erstellen, aber die RenderStream-Methode kann weiterhin helfen. Verwenden Sie den folgenden Code:


```C++
// Build the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example3.avi"), &pMux, 0);

// MSDV to DV splitter.
IBaseFilter *pDVSplit;  // Create the DV Splitter (CLSID_DVSplitter)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pDV, 0, pDVSplit);

// Splitter to DV Decoder to Smart Tee.
IBaseFilter *pDVDec; // Create the DV Decoder (CLSID_DVVideoCodec)
IBaseFilter *pSmartTee; // Create the Smart Tee (CLSID_SmartTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Video, pDVSplit, pDVDec,
    pSmartTee);

// Smart Tee (video) to Avi Mux.
IPin *pPin1;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 0, &pPin1);
hr = pBuilder->RenderStream(0, 0, pPin1, 0, pMux);

// Smart Tee to preview.
IPin *pPin2;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 1, &pPin2);
hr = pBuilder->RenderStream(0, 0, pPin2, 0, pMux);

// DV Splitter (audio) to Infinite Tee to Avi Mux.
IBaseFilter *pTee; // Create the Infinite Pin Tee (CLSID_InfTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Audio, pDVSplit, pTee, pMux);

// Infinite Pin Tee to preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



Sie müssen die Filter DV Splitter, DV Video Decoder, Smart Tee und Infinite Pin Tee erstellen und diese jeweils dem Filterdiagramm hinzufügen. (Aus Kürze werden diese Schritte im vorherigen Code weggelassen.) In diesem Beispiel wird die [**ICaptureGraphBuilder2::FindPin-Methode**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) verwendet, um die Aufnahme- und Vorschaupins im Smart Tee-Filter zu suchen. Capture ist immer Ausgabepin 0, und vorschau ist Ausgabepin 1.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



