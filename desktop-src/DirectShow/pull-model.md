---
description: Pull-Modell
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: Pull-Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd4becd54bffb39acf30b6d29fca45e6a117989
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521344"
---
# <a name="pull-model"></a><span data-ttu-id="9d0c1-103">Pull-Modell</span><span class="sxs-lookup"><span data-stu-id="9d0c1-103">Pull Model</span></span>

<span data-ttu-id="9d0c1-104">In der [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle bestimmt der Upstream-Filter, welche Daten gesendet werden sollen, und überträgt die Daten an den downstreamfilter.</span><span class="sxs-lookup"><span data-stu-id="9d0c1-104">In the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, the upstream filter determines what data to send, and it pushes the data to the downstream filter.</span></span> <span data-ttu-id="9d0c1-105">Für einige Filter ist ein *Pull* -Modell besser geeignet.</span><span class="sxs-lookup"><span data-stu-id="9d0c1-105">For some filters, a *pull* model is more appropriate.</span></span> <span data-ttu-id="9d0c1-106">Hier fordert der Downstream-Filterdaten aus dem upstreamfilter an.</span><span class="sxs-lookup"><span data-stu-id="9d0c1-106">Here, the downstream filter requests data from the upstream filter.</span></span> <span data-ttu-id="9d0c1-107">Die Beispiele sind nach dem Wechsel nach unten, von der Ausgabe-Pin bis zur Eingabe-PIN, aber der Downstream-Filter initiiert den Datenfluss</span><span class="sxs-lookup"><span data-stu-id="9d0c1-107">Samples still travel downstream, from output pin to input pin, but the downstream filter initiates the data flow.</span></span> <span data-ttu-id="9d0c1-108">Dieser Verbindungstyp verwendet die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9d0c1-108">This type of connection uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

<span data-ttu-id="9d0c1-109">Die typische Verwendung für das Pull-Modell ist die Dateiwiedergabe.</span><span class="sxs-lookup"><span data-stu-id="9d0c1-109">The typical use for the pull model is in file playback.</span></span> <span data-ttu-id="9d0c1-110">Beispielsweise führt der asynchrone [Datei Quell](file-source--async--filter.md) Filter in einem AVI-Wiedergabe Diagramm generische Datei Lesevorgänge durch und übermittelt die Daten als Bytestream ohne Formatinformationen.</span><span class="sxs-lookup"><span data-stu-id="9d0c1-110">For example, in an AVI playback graph, the [Async File Source](file-source--async--filter.md) filter performs generic file reading operations and delivers the data as a byte stream, with no format information.</span></span> <span data-ttu-id="9d0c1-111">Der [avi-Splitter](avi-splitter-filter.md) Filter liest die AVI-Header und analysiert den Stream in Video-und Audiobeispiele.</span><span class="sxs-lookup"><span data-stu-id="9d0c1-111">The [AVI Splitter](avi-splitter-filter.md) filter reads the AVI headers and parses the stream into video and audio samples.</span></span> <span data-ttu-id="9d0c1-112">Der avi-Splitter kann ermitteln, welche Daten Sie besser benötigen als der asynchrone Quell Filter für Dateien, weshalb er anstelle von **IMemInputPin** **iasynkreader** verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d0c1-112">The AVI Splitter can determine what data it needs better than the Async File Source filter, and therefore it uses **IAsyncReader** instead of **IMemInputPin**.</span></span>

<span data-ttu-id="9d0c1-113">Um Daten aus dem Ausgabepin anzufordern, ruft die Eingabe-PIN eine der folgenden Methoden auf:</span><span class="sxs-lookup"><span data-stu-id="9d0c1-113">To request data from the output pin, the input pin calls one of the following methods:</span></span>

-   [<span data-ttu-id="9d0c1-114">**Iasynkreader:: Request**</span><span class="sxs-lookup"><span data-stu-id="9d0c1-114">**IAsyncReader::Request**</span></span>](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [<span data-ttu-id="9d0c1-115">**Iasynkreader:: synkread**</span><span class="sxs-lookup"><span data-stu-id="9d0c1-115">**IAsyncReader::SyncRead**</span></span>](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   <span data-ttu-id="9d0c1-116">[**Iasynkreader:: synkreadausgerichtete**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span><span class="sxs-lookup"><span data-stu-id="9d0c1-116">[**IAsyncReader::SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).</span></span>

<span data-ttu-id="9d0c1-117">Die erste Methode ist asynchron, um mehrere überlappende Lesevorgänge zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9d0c1-117">The first method is asynchronous, to support multiple overlapped reads.</span></span> <span data-ttu-id="9d0c1-118">Die anderen sind synchron.</span><span class="sxs-lookup"><span data-stu-id="9d0c1-118">The others are synchronous.</span></span>

<span data-ttu-id="9d0c1-119">Theoretisch kann ein beliebiger Filter **iasynkreader** unterstützen, in der Praxis ist er jedoch für Quell Filter konzipiert, die eine Verbindung mit Parserfiltern herstellen.</span><span class="sxs-lookup"><span data-stu-id="9d0c1-119">In theory, any filter can support **IAsyncReader**, but in practice it is designed for source filters that connect to parser filters.</span></span> <span data-ttu-id="9d0c1-120">Der Parser verhält sich sehr ähnlich wie der Quell Filter im Push-Modell.</span><span class="sxs-lookup"><span data-stu-id="9d0c1-120">The parser acts very much like a source filter in the push model.</span></span> <span data-ttu-id="9d0c1-121">Wenn er angehalten wird, erstellt er einen streamingindthread, der Daten aus der **iasynkreader** -Verbindung abruft und diese nach unten verschiebt.</span><span class="sxs-lookup"><span data-stu-id="9d0c1-121">When it pauses, it creates a streaming thread that pulls data from the **IAsyncReader** connection and pushes it downstream.</span></span> <span data-ttu-id="9d0c1-122">Die Ausgabe Pins verwenden **IMemInputPin**, und der Rest des Diagramms verwendet das Standard-Push-Modell.</span><span class="sxs-lookup"><span data-stu-id="9d0c1-122">The output pins use **IMemInputPin**, and the rest of the graph uses the standard push model.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d0c1-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9d0c1-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d0c1-124">Datenfluss im Filter Diagramm</span><span class="sxs-lookup"><span data-stu-id="9d0c1-124">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



