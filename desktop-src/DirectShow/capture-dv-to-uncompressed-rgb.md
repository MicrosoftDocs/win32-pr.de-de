---
description: DV in nicht komprimiertem RGB erfassen
ms.assetid: 02b54070-09c8-45ab-8a08-1493008a5e1f
title: DV in nicht komprimiertem RGB erfassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b471bb8be6bc560fda6d3466cebaef8c490cfb8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123644"
---
# <a name="capture-dv-to-uncompressed-rgb"></a>DV in nicht komprimiertem RGB erfassen

Dieses Beispiel zeigt, wie Sie DV vom Camcorder erfassen und in einer Datei als unkomprimiertes RGB speichern, während die Vorschau angezeigt wird. Verwenden Sie das in der folgenden Abbildung gezeigte Filter Diagramm.

![Erfassen von nicht komprimiertem RGB in Datei](images/dv-rgb-cap.png)

Der DV-Splitter Filter teilt das überlappende Audioformat/Video in separate Video-und Audiostreams. das DV-codierte Video wird an den [DV-Video Decoder](dv-video-decoder-filter.md) -Filter weitergeleitet, der unkomprimierte RGB-Videos ausgibt. Das RGB-Video wird über den Smart Tee-Filter an den AVI MUX-Filter (für die Erfassung) und den Videorenderer (für die Vorschau) weitergeleitet. In der Zwischenzeit durchläuft der Audiostream aus dem DV-Splitter den unendlichen Pin-Tee-Filter an den AVI MUX und den audiorenderer. Der Filter Graph-Manager behält alle diese Datenströme mit den Zeitstempeln der Stichproben und der Diagramm Referenz Uhr bei.

Dieses Diagramm mag unnötig kompliziert erscheinen, stellt jedoch sicher, dass der DV-codierte Videostream nur einmal decodiert wird, wodurch die CPU-Anforderungen minimiert werden. Beachten Sie außerdem, dass das Video den intelligenten Tee-Filter durchläuft, während die Audiodaten den unendlichen Pin-Tee-Filter durchläuft. Der Smart Tee kann vorschauframes ablegen, um die Erfassungs Leistung zu verbessern, was für Video, aber nicht für Audiodaten wünschenswert ist, bei dem gelöschte Beispiele sehr bemerkbar sind Da das Audiomaterial eine viel geringere Bandbreite als das Video erfordert, besteht die Möglichkeit, dass Audiodaten in der Datei nicht gelöscht werden.

Sie müssen dieses Diagramm jeweils einen Abschnitt erstellen, aber die RenderStream-Methode kann weiterhin helfen. Verwenden Sie den folgenden Code:


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



Sie müssen die Filter "DV Splitter", "DV Video Decoder", "Smart Tee" und "Infinite Pin Tee" erstellen und diese dem Filter Diagramm hinzufügen. (Aus Gründen der Kürze werden diese Schritte im vorherigen Code ausgelassen.) In diesem Beispiel wird die [**ICaptureGraphBuilder2:: findpin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) -Methode verwendet, um die Erfassungs-und Vorschau Pins im intelligenten Tee-Filter zu suchen. Capture ist immer Ausgabe-PIN 0 und Vorschau ist Ausgabe-PIN 1.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



