---
description: Datenfluss für Filter Entwickler
ms.assetid: cc7378c8-e268-4caa-98eb-6dc9c3b5bcad
title: Datenfluss für Filter Entwickler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ccb4e4123e8617190a459ff500d1100c0dbbb8ca
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041298"
---
# <a name="data-flow-for-filter-developers"></a><span data-ttu-id="f2bbd-103">Datenfluss für Filter Entwickler</span><span class="sxs-lookup"><span data-stu-id="f2bbd-103">Data Flow for Filter Developers</span></span>

<span data-ttu-id="f2bbd-104">In diesem Abschnitt wird ausführlich beschrieben, wie Daten durch das Filter Diagramm verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-104">This section describes in detail how data moves through the filter graph.</span></span> <span data-ttu-id="f2bbd-105">Der Schwerpunkt liegt auf dem lokalen Speicher Transport mithilfe der [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) -oder [**iasynkreader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-105">It focuses on local memory transport using the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) or [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span> <span data-ttu-id="f2bbd-106">Es ist für Entwickler gedacht, die eigene benutzerdefinierte Filter schreiben.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-106">It is intended for developers who are writing their own custom filters.</span></span> <span data-ttu-id="f2bbd-107">Eine allgemeine Einführung in die Verarbeitung von Daten Flüssen durch Microsoft DirectShow finden Sie unter [Datenfluss im Filter Diagramm](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="f2bbd-107">For a general introduction to how Microsoft DirectShow handles data flow, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="f2bbd-108">Viele Daten durchlaufen ein Filter Diagramm.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-108">A lot of data moves through a filter graph.</span></span> <span data-ttu-id="f2bbd-109">Es fällt ungefähr in zwei Kategorien: Mediendaten und Steuerungsdaten.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-109">It falls roughly into two categories: media data and control data.</span></span> <span data-ttu-id="f2bbd-110">Im Allgemeinen werden Mediendaten nach unten durchlaufen, und Steuerungsdaten werden im Upstream übertragen.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-110">In general, media data travels downstream and control data travels upstream.</span></span> <span data-ttu-id="f2bbd-111">Zu den Mediendaten gehören Video Frames, Audiobeispiele, MPEG-Pakete usw., die einen Stream bilden, aber auch Leerungs Befehle, Dateiende-Benachrichtigungen und andere Daten, die mit dem Stream übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-111">Media data includes the video frames, audio samples, MPEG packets, and so forth that make up a stream, but also includes flush commands, end-of-stream notifications, and other data that travels with the stream.</span></span> <span data-ttu-id="f2bbd-112">Steuerungsdaten sind nicht Teil des Mediendaten Stroms.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-112">Control data is not part of the media stream.</span></span> <span data-ttu-id="f2bbd-113">Beispiele für Steuerungsdaten sind Qualitäts Steuerungsanforderungen und Such Befehle.</span><span class="sxs-lookup"><span data-stu-id="f2bbd-113">Examples of control data are quality-control requests and seek commands.</span></span>

<span data-ttu-id="f2bbd-114">Dieser Abschnitt enthält die folgenden Artikel:</span><span class="sxs-lookup"><span data-stu-id="f2bbd-114">This section contains the following articles.</span></span>

-   [<span data-ttu-id="f2bbd-115">Bereitstellung von Beispielen</span><span class="sxs-lookup"><span data-stu-id="f2bbd-115">Delivering Samples</span></span>](delivering-samples.md)
-   [<span data-ttu-id="f2bbd-116">Verarbeiten von Daten</span><span class="sxs-lookup"><span data-stu-id="f2bbd-116">Processing Data</span></span>](processing-data.md)
-   [<span data-ttu-id="f2bbd-117">Streamende-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="f2bbd-117">End-of-Stream Notifications</span></span>](end-of-stream-notifications.md)
-   [<span data-ttu-id="f2bbd-118">Neue Segmente</span><span class="sxs-lookup"><span data-stu-id="f2bbd-118">New Segments</span></span>](new-segments.md)
-   [<span data-ttu-id="f2bbd-119">Lak</span><span class="sxs-lookup"><span data-stu-id="f2bbd-119">Flushing</span></span>](flushing.md)
-   [<span data-ttu-id="f2bbd-120">Diejenigen</span><span class="sxs-lookup"><span data-stu-id="f2bbd-120">Seeking</span></span>](seeking.md)
-   [<span data-ttu-id="f2bbd-121">Dynamische Format Änderungen</span><span class="sxs-lookup"><span data-stu-id="f2bbd-121">Dynamic Format Changes</span></span>](dynamic-format-changes.md)

## <a name="related-topics"></a><span data-ttu-id="f2bbd-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2bbd-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2bbd-123">Qualitäts Steuerungs Verwaltung</span><span class="sxs-lookup"><span data-stu-id="f2bbd-123">Quality-Control Management</span></span>](quality-control-management.md)
</dt> <dt>

[<span data-ttu-id="f2bbd-124">Threads und kritische Abschnitte</span><span class="sxs-lookup"><span data-stu-id="f2bbd-124">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> <dt>

[<span data-ttu-id="f2bbd-125">Schreiben von DirectShow-Filtern</span><span class="sxs-lookup"><span data-stu-id="f2bbd-125">Writing DirectShow Filters</span></span>](writing-directshow-filters.md)
</dt> </dl>

 

 



