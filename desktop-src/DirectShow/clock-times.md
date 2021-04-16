---
description: Uhrzeiten
ms.assetid: ff964f7f-a084-4de3-8b2b-8efb6c9f4a9f
title: Uhrzeiten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0639fd2b38e312f30f932fcf508427cd71c054
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392405"
---
# <a name="clock-times"></a><span data-ttu-id="d8da2-103">Uhrzeiten</span><span class="sxs-lookup"><span data-stu-id="d8da2-103">Clock Times</span></span>

<span data-ttu-id="d8da2-104">DirectShow definiert zwei zugehörige Uhrzeiten: Verweis Zeit und streamzeit.</span><span class="sxs-lookup"><span data-stu-id="d8da2-104">DirectShow defines two related clock times: reference time and stream time.</span></span>

-   <span data-ttu-id="d8da2-105">Die *Verweis Zeit* ist die absolute Zeit, die von der Referenzuhr zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="d8da2-105">*Reference time* is the absolute time returned by the reference clock.</span></span> <span data-ttu-id="d8da2-106">(Siehe [Referenzuhren](reference-clocks.md).)</span><span class="sxs-lookup"><span data-stu-id="d8da2-106">(See [Reference Clocks](reference-clocks.md).)</span></span>
-   <span data-ttu-id="d8da2-107">Die *streamzeit* wird relativ zum Zeitpunkt der letzten Ausführung des Diagramms definiert.</span><span class="sxs-lookup"><span data-stu-id="d8da2-107">*Stream time* is defined relative to when the graph last started running.</span></span>
    -   <span data-ttu-id="d8da2-108">Während der Ausführung des Diagramms ist die streamzeit gleich der Verweis Zeit abzüglich der Startzeit.</span><span class="sxs-lookup"><span data-stu-id="d8da2-108">While the graph is running, stream time equals reference time minus start time.</span></span>
    -   <span data-ttu-id="d8da2-109">Während das Diagramm angehalten wird, verbleibt die streamzeit zum Zeitpunkt des anhalten.</span><span class="sxs-lookup"><span data-stu-id="d8da2-109">While the graph is paused, stream time remains at the stream time when it was paused.</span></span>
    -   <span data-ttu-id="d8da2-110">Nach einem Suchvorgang wird die streamzeit auf 0 zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d8da2-110">After a seek operation, stream time resets to zero.</span></span>
    -   <span data-ttu-id="d8da2-111">Während das Diagramm angehalten wird, ist die streamzeit nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="d8da2-111">While the graph is stopped, stream time is undefined.</span></span>

<span data-ttu-id="d8da2-112">Wenn ein Medien Beispiel einen Zeitstempel *t* aufweist, bedeutet dies, dass das Beispiel in der streamzeit *t* gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8da2-112">When a media sample has a time stamp *t*, it means the sample should be rendered at stream time *t*.</span></span> <span data-ttu-id="d8da2-113">Aus diesem Grund wird die streamzeit auch als *Präsentationszeit* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d8da2-113">For this reason, stream time is also called *presentation time*.</span></span>

<span data-ttu-id="d8da2-114">Wenn eine Anwendung [**IMediaControl:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) aufruft, um das Filter Diagramm auszuführen, ruft der Filter Graph-Manager [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) für jeden Filter auf.</span><span class="sxs-lookup"><span data-stu-id="d8da2-114">When an application calls [**IMediaControl::Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) to run the filter graph, the Filter Graph Manager calls [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) on each filter.</span></span> <span data-ttu-id="d8da2-115">Um die Zeitspanne zu kompensieren, die für die Ausführung der Filter benötigt wird, gibt der Filter Graph-Manager eine Startzeit etwas in der Zukunft an.</span><span class="sxs-lookup"><span data-stu-id="d8da2-115">To compensate for the slight amount of time it takes for the filters to start running, the Filter Graph Manager specifies a start time slightly in the future.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d8da2-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8da2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8da2-117">Uhrzeit und Uhren in DirectShow</span><span class="sxs-lookup"><span data-stu-id="d8da2-117">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="d8da2-118">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="d8da2-118">Time Stamps</span></span>](time-stamps.md)
</dt> </dl>

 

 



