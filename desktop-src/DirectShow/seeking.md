---
description: Diejenigen
ms.assetid: ceccb657-f1e1-4d59-920a-477a95b8a1a4
title: Diejenigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef7e82009198a790d5c0f7818599aa13905ce82
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104569255"
---
# <a name="seeking"></a><span data-ttu-id="8e160-103">Diejenigen</span><span class="sxs-lookup"><span data-stu-id="8e160-103">Seeking</span></span>

<span data-ttu-id="8e160-104">Filter unterstützen das Suchen über die [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8e160-104">Filters support seeking through the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="8e160-105">Die Anwendung fragt den Filter Graph-Manager nach **imediaseeking** ab und verwendet Sie, um Such Befehle auszugeben.</span><span class="sxs-lookup"><span data-stu-id="8e160-105">The application queries the Filter Graph Manager for **IMediaSeeking** and uses it to issue seek commands.</span></span> <span data-ttu-id="8e160-106">Der Filter Graph-Manager verteilt jeden Seek-Befehl an alle rendererfilter im Diagramm.</span><span class="sxs-lookup"><span data-stu-id="8e160-106">The Filter Graph Manager distributes each seek command to all of the renderer filters in the graph.</span></span> <span data-ttu-id="8e160-107">Jeder Renderer übergibt den Befehls Upstream über die Ausgabe Pins der upstreamfilter, bis er einen Filter erreicht, der die Suche ausführen kann.</span><span class="sxs-lookup"><span data-stu-id="8e160-107">Each renderer passes the command upstream, through the output pins of the upstream filters, until it reaches a filter that can execute the seek.</span></span> <span data-ttu-id="8e160-108">In der Regel führt ein Quell Filter oder Parserfilter, z. b. der [avi-Splitter](avi-splitter-filter.md), den Suchvorgang aus.</span><span class="sxs-lookup"><span data-stu-id="8e160-108">Typically a source filter or parser filter, such as the [AVI Splitter](avi-splitter-filter.md), carries out the seek operation.</span></span>

<span data-ttu-id="8e160-109">Wenn ein Filter einen Suchvorgang ausführt, werden alle ausstehenden Daten geleert.</span><span class="sxs-lookup"><span data-stu-id="8e160-109">When a filter performs a seek operation, it flushes any pending data.</span></span> <span data-ttu-id="8e160-110">Das Ergebnis besteht darin, die Latenz von Seek-Befehlen zu minimieren, da vorhandene Daten aus dem Diagramm geleert werden.</span><span class="sxs-lookup"><span data-stu-id="8e160-110">The result is to minimize the latency of seek commands, because existing data is flushed from the graph.</span></span> <span data-ttu-id="8e160-111">Nach einem Seek-Befehl wird die streamzeit auf 0 zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="8e160-111">After a seek command, stream time resets to zero.</span></span>

<span data-ttu-id="8e160-112">Das folgende Diagramm veranschaulicht die Abfolge von Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="8e160-112">The following diagram illustrates the sequence of events.</span></span>

![Abfolge von Ereignissen](images/seeking.png)

<span data-ttu-id="8e160-114">Wenn ein Parserfilter über mehr als eine Ausgabe-PIN verfügt, weist er in der Regel einen von Ihnen auf, um Such Befehle zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="8e160-114">If a parser filter has more than one output pin, it typically designates one of them to accept seek commands.</span></span> <span data-ttu-id="8e160-115">Mit den anderen Pins werden alle empfangenen Such Befehle abgelehnt oder ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8e160-115">The other pins reject or ignore any seek commands they receive.</span></span> <span data-ttu-id="8e160-116">Auf diese Weise hält der Parser alle zugehörigen Datenströme synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="8e160-116">In this way, the parser keeps all of its streams synchronized.</span></span> <span data-ttu-id="8e160-117">Alle Ausgabe Pins sollten jedoch [**imediaseeking:: getfunktionalitäten**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) und [**imediaseeking:: Check-Funktionen**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) implementieren, um die Suchfunktionen des Filters zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="8e160-117">However, all output pins should implement [**IMediaSeeking::GetCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getcapabilities) and [**IMediaSeeking::CheckCapabilities**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-checkcapabilities) to return the filter's seeking capabilities.</span></span> <span data-ttu-id="8e160-118">Dadurch wird sichergestellt, dass der Filter Graph-Manager den korrekten Wert an die Anwendung zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8e160-118">This ensures that the Filter Graph Manager returns the correct value to the application.</span></span>

<span data-ttu-id="8e160-119">Die [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition) -Schnittstelle wurde für Filter als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="8e160-119">The [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface has been deprecated for filters.</span></span> <span data-ttu-id="8e160-120">Automatisierungs Clients müssen diese Schnittstelle weiterhin auf dem Filter Graph-Manager verwenden, da **imediaseeking** nicht Automatisierungs kompatibel ist, aber der Filter Graph-Manager übersetzt alle **imediaposition** -Aufrufe in **imediaseeking** -Aufrufe.</span><span class="sxs-lookup"><span data-stu-id="8e160-120">Automation clients still need to use this interface on the Filter Graph Manager, because **IMediaSeeking** is not Automation-compatible, but the Filter Graph Manager translates all **IMediaPosition** calls into **IMediaSeeking** calls.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e160-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8e160-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e160-122">Lak</span><span class="sxs-lookup"><span data-stu-id="8e160-122">Flushing</span></span>](flushing.md)
</dt> <dt>

[<span data-ttu-id="8e160-123">Uhrzeit und Uhren in DirectShow</span><span class="sxs-lookup"><span data-stu-id="8e160-123">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



