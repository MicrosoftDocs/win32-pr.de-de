---
description: MPEG-2-Demux-Run-Time Modi
ms.assetid: b0d0c725-9220-43a5-af1c-d3c5c72e1ef3
title: MPEG-2-Demux-Run-Time Modi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6e4e7a1dea0bfeccd60d8680a31b99cc10271ee
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125216"
---
# <a name="mpeg-2-demux-run-time-modes"></a><span data-ttu-id="43281-103">MPEG-2-Demux-Run-Time Modi</span><span class="sxs-lookup"><span data-stu-id="43281-103">MPEG-2 Demux Run-Time Modes</span></span>

<span data-ttu-id="43281-104">Der [MPEG-2-Demultiplexer](mpeg-2-demultiplexer.md) ("demux") kann im Pushmodus oder Pullmodus verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="43281-104">The [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) ("demux") can operate in push mode or pull mode.</span></span> <span data-ttu-id="43281-105">Im Pushmodus stammen die Daten aus einer Live Quelle, z. b. einem Netzwerk Broadcast.</span><span class="sxs-lookup"><span data-stu-id="43281-105">In push mode, the data comes from a live source, such as a network broadcast.</span></span> <span data-ttu-id="43281-106">Im Pullmodus stammen die Daten aus einer lokalen Datei.</span><span class="sxs-lookup"><span data-stu-id="43281-106">In pull mode, the data comes from a local file.</span></span>

-   <span data-ttu-id="43281-107">Der Pull-Modus ist in Windows XP und höher für Programm Datenströme verfügbar.</span><span class="sxs-lookup"><span data-stu-id="43281-107">Pull mode is available in Windows XP and later, for program streams only.</span></span> <span data-ttu-id="43281-108">Verwenden Sie auf untergeordneten Plattformen den [MPEG-2-Splitter](mpeg-2-splitter.md) Filter.</span><span class="sxs-lookup"><span data-stu-id="43281-108">On down-level platforms, use the [MPEG-2 Splitter](mpeg-2-splitter.md) filter.</span></span>
-   <span data-ttu-id="43281-109">Der Pushmodus ist auf allen Plattformen sowohl für Programmstreams als auch für Transport Datenströme verfügbar.</span><span class="sxs-lookup"><span data-stu-id="43281-109">Push mode is available on all platforms, for both program streams and transport streams.</span></span>

<span data-ttu-id="43281-110">Das Demux unterstützt daher drei mögliche Modi: Programmstreams im Pullmodus, Programmstreams im Pushmodus und Transportstreams im Pushmodus.</span><span class="sxs-lookup"><span data-stu-id="43281-110">The demux therefore supports three possible modes: Program streams in pull mode, program streams in push mode, and transport streams in push mode.</span></span> <span data-ttu-id="43281-111">Der Demux-Wert bestimmt, welcher Modus zur Laufzeit verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43281-111">The demux determines which mode to use at run time.</span></span> <span data-ttu-id="43281-112">Der Modus wird bestimmt, wenn die eingabepin eine Verbindung herstellt oder wenn die erste Ausgabepin konfiguriert ist, je nachdem, welcher Vorgang zuerst erfolgt</span><span class="sxs-lookup"><span data-stu-id="43281-112">The mode is determined when the input pin connects, or when the first output pin is configured, whichever happens first:</span></span>

-   <span data-ttu-id="43281-113">Wenn die eingabepin eine Verbindung herstellt: unter Windows XP und höher fragt Demux den upstreamfilter für die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle ab. Wenn der upstreamfilter diese Schnittstelle verfügbar macht, konfiguriert sich der Demux selbst für Programmstreams im Pullmodus.</span><span class="sxs-lookup"><span data-stu-id="43281-113">When the input pin connects: On Windows XP and later, the demux queries the upstream filter for the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface; if the upstream filter exposes that interface, the demux configures itself for program streams in pull mode.</span></span> <span data-ttu-id="43281-114">Andernfalls verwendet der Demux den Pushmodus, und der Medientyp bestimmt den Streamtyp (Programmstream oder Transportstream).</span><span class="sxs-lookup"><span data-stu-id="43281-114">Otherwise, the demux uses push mode, and the media type determines the stream type (program stream or transport stream).</span></span> <span data-ttu-id="43281-115">Eine Liste der Eingabetypen finden Sie unter [**MPEG-2 Demultiplexer-Medientypen**](mpeg-2-demultiplexer-media-types.md) .</span><span class="sxs-lookup"><span data-stu-id="43281-115">See [**MPEG-2 Demultiplexer Media Types**](mpeg-2-demultiplexer-media-types.md) for a list of input types.</span></span>
-   <span data-ttu-id="43281-116">Wenn die erste Ausgabepin konfiguriert ist: Wenn Sie eine Ausgabepin erstellen und Sie nach [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap)Abfragen, konfiguriert die Demux sich selbst für Transportstreams im Pushmodus.</span><span class="sxs-lookup"><span data-stu-id="43281-116">When the first output pin is configured: If you create an output pin and query it for [**IMPEG2PIDMap**](/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap), the demux configures itself for transport streams in push mode.</span></span> <span data-ttu-id="43281-117">Wenn Sie die PIN für [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap)Abfragen, konfiguriert die Demux sich selbst für Programmstreams, auch im Pushmodus.</span><span class="sxs-lookup"><span data-stu-id="43281-117">If you query the pin for [**IMPEG2StreamIdMap**](/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap), the demux configures itself for program streams, also in push mode.</span></span> <span data-ttu-id="43281-118">Alle nachfolgenden Abfragen für die andere Schnittstelle schlagen fehl, da die Demux nicht gleichzeitig in zwei Modi betrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="43281-118">Any subsequent queries for the other interface fail, because the demux cannot operate in two modes at once.</span></span>

<span data-ttu-id="43281-119">Sobald die Demux sich für einen bestimmten Modus konfiguriert hat, bleibt Sie in diesem Modus.</span><span class="sxs-lookup"><span data-stu-id="43281-119">Once the demux has configured itself for a particular mode, it remains in that mode.</span></span> <span data-ttu-id="43281-120">Um einen anderen Modus zu verwenden, müssen Sie eine neue Instanz der Demux-Instanz erstellen.</span><span class="sxs-lookup"><span data-stu-id="43281-120">To use a different mode, you must create a new instance of the demux.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43281-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43281-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43281-122">Verwenden von MPEG-2 Demultiplexer</span><span class="sxs-lookup"><span data-stu-id="43281-122">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



