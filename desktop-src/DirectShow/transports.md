---
description: Transportprotokolle
ms.assetid: 63c5ff5b-293d-4a80-92e8-3ece41321095
title: Transportprotokolle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3d87ffacc871fc45ef1e8e645849afc956fb1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351733"
---
# <a name="transports"></a><span data-ttu-id="8eb4c-103">Transportprotokolle</span><span class="sxs-lookup"><span data-stu-id="8eb4c-103">Transports</span></span>

<span data-ttu-id="8eb4c-104">Um Mediendaten über das Filter Diagramm zu verschieben, muss ein DirectShow-Filter eines von mehreren möglichen Protokollen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-104">In order to move media data through the filter graph, a DirectShow filter must support one of several possible protocols.</span></span> <span data-ttu-id="8eb4c-105">Diese Protokolle werden als Transporte bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-105">These protocols are called transports.</span></span> <span data-ttu-id="8eb4c-106">Wenn zwei Filter eine Verbindung herstellen, müssen Sie denselben Transport unterstützen. Andernfalls können Sie keine Mediendaten austauschen.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-106">When two filters connect, they must support the same transport; otherwise they cannot exchange media data.</span></span> <span data-ttu-id="8eb4c-107">In der Regel erfordert ein Transport, dass einer der Pins eine bestimmte Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-107">Typically, a transport requires that one of the pins support a particular interface.</span></span> <span data-ttu-id="8eb4c-108">Wenn die Filter eine Verbindung herstellen, fragt eine PIN die andere nach der Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-108">When the filters connect, one pin queries the other for the interface.</span></span>

<span data-ttu-id="8eb4c-109">Die meisten DirectShow-Filter enthalten Mediendaten im Hauptspeicher und übermitteln Sie an andere Filter über PIN-Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-109">Most DirectShow filters hold media data in main memory, and deliver it to other filters across pin connections.</span></span> <span data-ttu-id="8eb4c-110">Diese Art von Transport wird als lokaler Speicher Transport bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-110">This type of transport is called local memory transport.</span></span> <span data-ttu-id="8eb4c-111">Obwohl der lokale Speicher Transport der am häufigsten verwendete Transport in DirectShow ist, wird er nicht von allen Filtern verwendet.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-111">Although local memory transport is the most common transport in DirectShow, not all filters use it.</span></span> <span data-ttu-id="8eb4c-112">Beispielsweise werden von einigen Filtern Mediendaten an einem Hardware Pfad gesendet, und es werden nur Pins verwendet, um Steuerungsinformationen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-112">For example, some filters send media data along a hardware path, and use pins only to deliver control information.</span></span> <span data-ttu-id="8eb4c-113">Informationen hierzu finden Sie beispielsweise in der [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-113">For example, see the [**IOverlay**](/windows/desktop/api/Strmif/nn-strmif-ioverlay) interface.</span></span>

<span data-ttu-id="8eb4c-114">DirectShow definiert zwei Mechanismen für den lokalen Speicher Transport, das Push-Modell und das Pull-Modell.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-114">DirectShow defines two mechanisms for local memory transport, the push model and the pull model.</span></span> <span data-ttu-id="8eb4c-115">Im Push-Modell generiert ein Quell Filterdaten und übermittelt Sie an den nächsten Filter Downstream.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-115">In the push model, a source filter generates data and delivers it to the next filter downstream.</span></span> <span data-ttu-id="8eb4c-116">Dieser Filter empfängt die Daten passiv, verarbeitet sie und sendet Sie weiter nach unten.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-116">That filter passively receives the data, processes it, and sends it further downstream.</span></span> <span data-ttu-id="8eb4c-117">Im Pull-Modell ist der Quell Filter mit einem Parserfilter verbunden.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-117">In the pull model, the source filter is connected to a parser filter.</span></span> <span data-ttu-id="8eb4c-118">Der Parserfilter fordert Daten aus dem Quell Filter an.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-118">The parser filter requests data from the source filter.</span></span> <span data-ttu-id="8eb4c-119">Der Quell Filter antwortet auf die Anforderungen, indem er Daten bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-119">The source filter responds to the requests by delivering data.</span></span> <span data-ttu-id="8eb4c-120">Das Pushmodell verwendet die [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -Schnittstelle, und das Pull-Modell verwendet die [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-120">The push model uses the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, and the pull model uses the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span>

<span data-ttu-id="8eb4c-121">Das Push-Modell ist häufiger als das Pull-Modell.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-121">The push model is more common than the pull model.</span></span> <span data-ttu-id="8eb4c-122">Daher wird von den folgenden Artikeln ein Push-Modell angenommen.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-122">Therefore, the articles that follow assume a push model.</span></span> <span data-ttu-id="8eb4c-123">Im letzten Artikel in diesem Abschnitt, [Pull Model](pull-model.md), wird beschrieben, wie die **iasynkreader** -Schnittstelle von **IMemInputPin** abweicht.</span><span class="sxs-lookup"><span data-stu-id="8eb4c-123">The last article in this section, [Pull Model](pull-model.md), describes how the **IAsyncReader** interface differs from **IMemInputPin**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8eb4c-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8eb4c-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8eb4c-125">Datenfluss im Filter Diagramm</span><span class="sxs-lookup"><span data-stu-id="8eb4c-125">Data Flow in the Filter Graph</span></span>](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



