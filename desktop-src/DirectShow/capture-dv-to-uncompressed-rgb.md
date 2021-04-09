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
# <a name="capture-dv-to-uncompressed-rgb"></a><span data-ttu-id="39581-103">DV in nicht komprimiertem RGB erfassen</span><span class="sxs-lookup"><span data-stu-id="39581-103">Capture DV to Uncompressed RGB</span></span>

<span data-ttu-id="39581-104">Dieses Beispiel zeigt, wie Sie DV vom Camcorder erfassen und in einer Datei als unkomprimiertes RGB speichern, während die Vorschau angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="39581-104">This example shows how to capture DV from the camcorder and save it to a file as uncompressed RGB while previewing.</span></span> <span data-ttu-id="39581-105">Verwenden Sie das in der folgenden Abbildung gezeigte Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="39581-105">Use the filter graph shown in the following diagram.</span></span>

![Erfassen von nicht komprimiertem RGB in Datei](images/dv-rgb-cap.png)

<span data-ttu-id="39581-107">Der DV-Splitter Filter teilt das überlappende Audioformat/Video in separate Video-und Audiostreams. das DV-codierte Video wird an den [DV-Video Decoder](dv-video-decoder-filter.md) -Filter weitergeleitet, der unkomprimierte RGB-Videos ausgibt.</span><span class="sxs-lookup"><span data-stu-id="39581-107">The DV Splitter filter splits the interleaved audio/video into separate video and audio streams The DV-encoded video goes to the [DV Video Decoder](dv-video-decoder-filter.md) filter, which outputs uncompressed RGB video.</span></span> <span data-ttu-id="39581-108">Das RGB-Video wird über den Smart Tee-Filter an den AVI MUX-Filter (für die Erfassung) und den Videorenderer (für die Vorschau) weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="39581-108">The RGB video is routed through the Smart Tee filter to the AVI Mux filter (for capture) and the video renderer (for preview).</span></span> <span data-ttu-id="39581-109">In der Zwischenzeit durchläuft der Audiostream aus dem DV-Splitter den unendlichen Pin-Tee-Filter an den AVI MUX und den audiorenderer.</span><span class="sxs-lookup"><span data-stu-id="39581-109">Meanwhile, the audio stream from the DV Splitter goes through the Infinite Pin Tee filter to the AVI Mux and the audio renderer.</span></span> <span data-ttu-id="39581-110">Der Filter Graph-Manager behält alle diese Datenströme mit den Zeitstempeln der Stichproben und der Diagramm Referenz Uhr bei.</span><span class="sxs-lookup"><span data-stu-id="39581-110">The Filter Graph Manager keeps all of these streams synchronized, using the time stamps on the samples and the graph reference clock.</span></span>

<span data-ttu-id="39581-111">Dieses Diagramm mag unnötig kompliziert erscheinen, stellt jedoch sicher, dass der DV-codierte Videostream nur einmal decodiert wird, wodurch die CPU-Anforderungen minimiert werden.</span><span class="sxs-lookup"><span data-stu-id="39581-111">This graph might seem unnecessarily complicated, but it ensures that the DV-encoded video stream is decoded only once, which minimizes the CPU requirements.</span></span> <span data-ttu-id="39581-112">Beachten Sie außerdem, dass das Video den intelligenten Tee-Filter durchläuft, während die Audiodaten den unendlichen Pin-Tee-Filter durchläuft.</span><span class="sxs-lookup"><span data-stu-id="39581-112">Also, note that the video goes through the Smart Tee filter while the audio goes through the Infinite Pin Tee filter.</span></span> <span data-ttu-id="39581-113">Der Smart Tee kann vorschauframes ablegen, um die Erfassungs Leistung zu verbessern, was für Video, aber nicht für Audiodaten wünschenswert ist, bei dem gelöschte Beispiele sehr bemerkbar sind</span><span class="sxs-lookup"><span data-stu-id="39581-113">The Smart Tee can drop preview frames to improve capture performance, which is desirable for video but not for audio, where dropped samples are highly noticeable.</span></span> <span data-ttu-id="39581-114">Da das Audiomaterial eine viel geringere Bandbreite als das Video erfordert, besteht die Möglichkeit, dass Audiodaten in der Datei nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="39581-114">Also, because the audio requires much lower bandwidth than the video, there is relatively little chance of dropping audio in the file.</span></span>

<span data-ttu-id="39581-115">Sie müssen dieses Diagramm jeweils einen Abschnitt erstellen, aber die RenderStream-Methode kann weiterhin helfen.</span><span class="sxs-lookup"><span data-stu-id="39581-115">You must build this graph one section at a time, but the RenderStream method can still help.</span></span> <span data-ttu-id="39581-116">Verwenden Sie den folgenden Code:</span><span class="sxs-lookup"><span data-stu-id="39581-116">Use the following code:</span></span>


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



<span data-ttu-id="39581-117">Sie müssen die Filter "DV Splitter", "DV Video Decoder", "Smart Tee" und "Infinite Pin Tee" erstellen und diese dem Filter Diagramm hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="39581-117">You must create the DV Splitter, DV Video Decoder, Smart Tee, and Infinite Pin Tee filters, and add each one to the filter graph.</span></span> <span data-ttu-id="39581-118">(Aus Gründen der Kürze werden diese Schritte im vorherigen Code ausgelassen.) In diesem Beispiel wird die [**ICaptureGraphBuilder2:: findpin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) -Methode verwendet, um die Erfassungs-und Vorschau Pins im intelligenten Tee-Filter zu suchen. Capture ist immer Ausgabe-PIN 0 und Vorschau ist Ausgabe-PIN 1.</span><span class="sxs-lookup"><span data-stu-id="39581-118">(For brevity, these steps are omitted from the previous code.) This example uses the [**ICaptureGraphBuilder2::FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) method to find the capture and preview pins on the Smart Tee filter; capture is always output pin 0, and preview is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="39581-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="39581-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="39581-120">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="39581-120">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



