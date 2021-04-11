---
description: Verhalten der Demux-Uhr
ms.assetid: c8a067f7-4e4c-4f25-b26c-f6bb048060b0
title: Verhalten der Demux-Uhr
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9065e6da51acb5387ca06bf921d5cdc91c567843
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041243"
---
# <a name="demux-clock-behavior"></a><span data-ttu-id="19d88-103">Verhalten der Demux-Uhr</span><span class="sxs-lookup"><span data-stu-id="19d88-103">Demux Clock Behavior</span></span>

<span data-ttu-id="19d88-104">Im Pushmodus macht der MPEG-2-Demultiplexer (Demux) die [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="19d88-104">In push mode, the MPEG-2 Demultiplexer (demux) exposes the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) interface.</span></span> <span data-ttu-id="19d88-105">Er fungiert als Live Quelle und wird daher standardmäßig als Graph-verweiszeit ausgewählt. Weitere Informationen finden Sie unter [Live Quellen](live-sources.md) .</span><span class="sxs-lookup"><span data-stu-id="19d88-105">It acts as a live source, so it will be chosen as the graph reference clock by default; see [Live Sources](live-sources.md) for more information.</span></span>

-   <span data-ttu-id="19d88-106">Bei Transportstreams synchronisiert die Demux die Uhr mit dem PCR-Stream, der dem Audiostream oder Videostream entspricht, der zuletzt von der Anwendung zugeordnet wurde.</span><span class="sxs-lookup"><span data-stu-id="19d88-106">For transport streams, the demux synchronizes its clock to the PCR stream that corresponds to the audio or video stream most recently mapped by the application.</span></span> <span data-ttu-id="19d88-107">Intern werden die Tabellen Pat und PMT von der "Debug"-Tabelle nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="19d88-107">Internally, the demux tracks the PAT and PMT tables.</span></span> <span data-ttu-id="19d88-108">Wenn die Anwendung einer Ausgabe-PIN eine elementare Datenstrom-PID zuordnet, sucht der Demux den PCR-Stream für diese PID und verwendet diesen PCR-Stream.</span><span class="sxs-lookup"><span data-stu-id="19d88-108">When the application maps an elementary stream PID to an output pin, the demux looks up the PCR stream for that PID and uses that PCR stream.</span></span> <span data-ttu-id="19d88-109">(Derzeit gibt es für die Anwendung keine Möglichkeit, die PCR-PID direkt anzugeben.)</span><span class="sxs-lookup"><span data-stu-id="19d88-109">(Currently, there is not way for the application to specify the PCR PID directly.)</span></span>
-   <span data-ttu-id="19d88-110">Bei Programmstreams synchronisiert die Demux die Uhr mit dem SCR-Stream.</span><span class="sxs-lookup"><span data-stu-id="19d88-110">For program streams, the demux synchronizes its clock to the SCR stream.</span></span>

<span data-ttu-id="19d88-111">Durch die Synchronisierung der filteruhr mit dem PCR-oder SCR-Stream wird ein Überlauf oder Unterlauf von Daten verhindert</span><span class="sxs-lookup"><span data-stu-id="19d88-111">Synchronizing the filter clock to the PCR or SCR stream prevents data overflow or underflow, which could result if the graph clock varied from the stream clock.</span></span> <span data-ttu-id="19d88-112">Der Wert von "Debug" übersetzt außerdem die Werte von "PES PTS" in "DirectShow Reference Times" und verwendet diese Werte zum Zeitstempel der Medien Beispiele.</span><span class="sxs-lookup"><span data-stu-id="19d88-112">The demux also translates PES PTS values into DirectShow reference times, and uses these values to time stamp the media samples.</span></span> <span data-ttu-id="19d88-113">Die Zeitstempel gelten für die nächste Frame Grenze. Es gibt keine Garantie, dass die Rahmen Grenze am Anfang des Medien Beispiels ausgerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="19d88-113">The time stamps apply to the next frame boundary; there is no guarantee that the frame boundary will align with the start of the media sample.</span></span>

<span data-ttu-id="19d88-114">Die "Debug" gewährleistet, dass die Zeitstempel monoton zunehmen.</span><span class="sxs-lookup"><span data-stu-id="19d88-114">The demux guarantees that the time stamps increase monotonically.</span></span> <span data-ttu-id="19d88-115">Dies bedeutet beispielsweise Folgendes: Wenn ein Transportstream ein Segment enthält, z. b. ein kommerzieller, das mit einer anderen Uhr als das Hauptprogramm erstellt wurde, passt die Demux die Präsentationszeit Stempel an, um die Zeit Diskontinuität von downstreamfiltern zu verbergen.</span><span class="sxs-lookup"><span data-stu-id="19d88-115">This means, for example, that if a transport stream includes a segment such as a commercial that was created with a different clock than the main program, the demux will adjust the presentation time stamps to hide the time discontinuity from downstream filters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19d88-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="19d88-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19d88-117">Verwenden von MPEG-2 Demultiplexer</span><span class="sxs-lookup"><span data-stu-id="19d88-117">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 



