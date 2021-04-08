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
# <a name="transmit-from-type-2-file"></a><span data-ttu-id="9b67a-103">Übertragen von Typ-2-Datei</span><span class="sxs-lookup"><span data-stu-id="9b67a-103">Transmit from Type-2 File</span></span>

<span data-ttu-id="9b67a-104">Verwenden Sie das in der folgenden Abbildung gezeigte Filter Diagramm, um eine Typ-2-Datei während der Vorschau zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="9b67a-104">To transmit a type-2 file while previewing, use the filter graph shown in the following diagram.</span></span>

![Type-2-Übertragung mit Vorschau](images/dv2-transmit.png)

<span data-ttu-id="9b67a-106">Eine Type-2-Datei enthält zwei Streams, einen Audiostream und einen DV-codierten Videostream.</span><span class="sxs-lookup"><span data-stu-id="9b67a-106">A type-2 file has two streams, one audio stream and one DV-encoded video stream.</span></span> <span data-ttu-id="9b67a-107">Dieses Diagramm verwendet den [DV-Muxer](dv-muxer-filter.md) -Filter, um die Audiodaten und Videodaten Ströme zu kombinieren.</span><span class="sxs-lookup"><span data-stu-id="9b67a-107">This graph uses the [DV Muxer](dv-muxer-filter.md) filter to combine the audio and video streams.</span></span> <span data-ttu-id="9b67a-108">Der überlappende Datenstrom wird an den msdv-Filter gesendet, der Stream wird jedoch für die Vorschau erneut unterteilt.</span><span class="sxs-lookup"><span data-stu-id="9b67a-108">It sends the interleaved stream to the MSDV filter, but splits the stream again for preview.</span></span>

<span data-ttu-id="9b67a-109">Erstellen Sie dieses Diagramm wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9b67a-109">Build this graph as follows:</span></span>


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



<span data-ttu-id="9b67a-110">Dieser Code führt mehrere Aufrufe von **RenderStream** aus:</span><span class="sxs-lookup"><span data-stu-id="9b67a-110">This code makes several calls to **RenderStream**:</span></span>

<span data-ttu-id="9b67a-111">Die ersten beiden verbinden den Quell Filter mit dem avi-Splitter und dem avi-Splitter mit dem DV-MUX.</span><span class="sxs-lookup"><span data-stu-id="9b67a-111">The first two connect the source filter to the AVI Splitter and the AVI Splitter to the DV Mux.</span></span> <span data-ttu-id="9b67a-112">Beim ersten Aufruf fügt der Erfassungs Diagramm-Generator automatisch den avi-Splitter zum Diagramm hinzu und verbindet einen der Ausgabe Pins des AVI-Splitters mit dem DV-MUX.</span><span class="sxs-lookup"><span data-stu-id="9b67a-112">In the first call, the Capture Graph Builder automatically adds the AVI Splitter to the graph and connects one of the AVI Splitter's output pins to the DV Mux.</span></span> <span data-ttu-id="9b67a-113">Im zweiten Aufruf findet der Erfassungs Diagramm-Generator die zweite Ausgabe-PIN des AVI-Splitters und verbindet diese mit dem DV-MUX.</span><span class="sxs-lookup"><span data-stu-id="9b67a-113">In the second call, the Capture Graph Builder finds the AVI Splitter's second output pin and connects that to the DV Mux.</span></span>

<span data-ttu-id="9b67a-114">Der dritte Aufruf von **RenderStream** verbindet den DV-Muxer mit dem Filter für unendliche PIN.</span><span class="sxs-lookup"><span data-stu-id="9b67a-114">The third call to **RenderStream** connects the DV Muxer to the Infinite Pin Tee filter.</span></span> <span data-ttu-id="9b67a-115">Beim nächsten-Rückruf wird ein Stream von der unbegrenzten PIN mit dem msdv-Erfassungs Filter verbunden.</span><span class="sxs-lookup"><span data-stu-id="9b67a-115">The next call connects one stream from the Infinite Pin Tee to the MSDV capture filter.</span></span> <span data-ttu-id="9b67a-116">Dieser Stream wird an das Gerät übertragen.</span><span class="sxs-lookup"><span data-stu-id="9b67a-116">This stream is transmitted to the device.</span></span> <span data-ttu-id="9b67a-117">Der letzte Aufruf von **RenderStream** erstellt den Vorschau Abschnitt des Diagramms.</span><span class="sxs-lookup"><span data-stu-id="9b67a-117">The last call to **RenderStream** builds the preview section of the graph.</span></span>

<span data-ttu-id="9b67a-118">Wenn Sie die Vorschau während der Übertragung nicht anzeigen möchten, können Sie den unbegrenzten Pin-Empfänger weglassen und einfach die DV-MUX mit dem msdv-Filter verbinden:</span><span class="sxs-lookup"><span data-stu-id="9b67a-118">If you do not want to preview while transmitting, you can omit the Infinite Pin Tee, and simply connect the DV Mux to the MSDV filter:</span></span>


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a><span data-ttu-id="9b67a-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9b67a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9b67a-120">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="9b67a-120">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



