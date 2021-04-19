---
description: Neue Segmente
ms.assetid: 6c470b38-481f-4e52-93b8-eb6b343dcefc
title: Neue Segmente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5438cb3b457ed8ea0f77bd2ac1dcc5d6d2c72698
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345978"
---
# <a name="new-segments"></a><span data-ttu-id="1d87f-103">Neue Segmente</span><span class="sxs-lookup"><span data-stu-id="1d87f-103">New Segments</span></span>

<span data-ttu-id="1d87f-104">Bei einem *Segment* handelt es sich um eine Gruppe von Medien Beispielen, die eine gemeinsame Startzeit, Endzeit und Wiedergabe Rate gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="1d87f-104">A *segment* is a group of media samples that share a common start time, stop time, and playback rate.</span></span> <span data-ttu-id="1d87f-105">Die [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) -Methode signalisiert den Anfang eines neuen Segments.</span><span class="sxs-lookup"><span data-stu-id="1d87f-105">The [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method signals the start of a new segment.</span></span> <span data-ttu-id="1d87f-106">Er bietet eine Möglichkeit für einen Quell Filter, Downstream-Filter darüber zu informieren, dass sich die Zeit-und rateninformationen geändert haben.</span><span class="sxs-lookup"><span data-stu-id="1d87f-106">It provides a way for a source filter to inform downstream filters that the time and rate information has changed.</span></span> <span data-ttu-id="1d87f-107">Wenn der Quell Filter z. b. einen neuen Punkt im Stream sucht, wird **newsegment** mit der neuen Startzeit aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1d87f-107">For example, if the source filter seeks to a new point in the stream, it calls **NewSegment** with the new start time.</span></span>

<span data-ttu-id="1d87f-108">Bei einigen downstreamfiltern werden die Segmentinformationen beim Verarbeiten von Beispielen verwendet.</span><span class="sxs-lookup"><span data-stu-id="1d87f-108">Some downstream filters use the segment information when they process samples.</span></span> <span data-ttu-id="1d87f-109">Wenn z. b. in einem Format, das die Interframe-Komprimierung verwendet, die Endzeit auf einen Delta Rahmen fällt, muss der Quell Filter möglicherweise nach der Endzeit zusätzliche Proben senden.</span><span class="sxs-lookup"><span data-stu-id="1d87f-109">For example, in a format that uses interframe compression, if the stop time falls on a delta frame, the source filter may need to send additional samples after the stop time.</span></span> <span data-ttu-id="1d87f-110">Dadurch kann der Decoder den abschließenden Delta Frame decodieren.</span><span class="sxs-lookup"><span data-stu-id="1d87f-110">This enables the decoder to decode the final delta frame.</span></span> <span data-ttu-id="1d87f-111">Um den richtigen abschließenden Frame zu ermitteln, verweist der Decoder auf die Endzeit des Segments.</span><span class="sxs-lookup"><span data-stu-id="1d87f-111">To determine the correct final frame, the decoder refers to the segment stop time.</span></span> <span data-ttu-id="1d87f-112">Ein weiteres Beispiel ist, dass audiorenderer die Segment Rate zusammen mit der audiosamplingrate verwenden, um die korrekte Audioausgabe zu generieren.</span><span class="sxs-lookup"><span data-stu-id="1d87f-112">As another example, audio renderers use the segment rate along with the audio sampling rate to generate the correct audio output.</span></span>

<span data-ttu-id="1d87f-113">Im Push-Modell initiiert der Quell Filter den **newsegment** -Rückruf.</span><span class="sxs-lookup"><span data-stu-id="1d87f-113">In the push model, the source filter initiates the **NewSegment** call.</span></span> <span data-ttu-id="1d87f-114">Im Pull-Modell erfolgt dies durch den Parserfilter.</span><span class="sxs-lookup"><span data-stu-id="1d87f-114">In the pull model, this is done by the parser filter.</span></span> <span data-ttu-id="1d87f-115">In jedem Fall ruft der Filter **newsegment** für die downstreameingabepin auf, die den Aufruf an den nächsten Filter weitergibt, bis der Aufruf den Renderer erreicht.</span><span class="sxs-lookup"><span data-stu-id="1d87f-115">In either case, the filter calls **NewSegment** on the downstream input pin, which propagates the call to the next filter, until the call reaches the renderer.</span></span> <span data-ttu-id="1d87f-116">Filter müssen **newsegment** -Aufrufe mit anderen streamingaufrufen serialisieren, wie z. b. [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).</span><span class="sxs-lookup"><span data-stu-id="1d87f-116">Filters must serialize **NewSegment** calls with other streaming calls, such as [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive).</span></span>

<span data-ttu-id="1d87f-117">Die streamzeit wird nach jedem neuen Segment auf Null zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="1d87f-117">Stream time resets to zero after each new segment.</span></span> <span data-ttu-id="1d87f-118">Zeitstempel für Stichproben, die nach dem Segment zugestellt werden, beginnen bei Null.</span><span class="sxs-lookup"><span data-stu-id="1d87f-118">Time stamps on samples delivered after the segment start from zero.</span></span>

 

 



