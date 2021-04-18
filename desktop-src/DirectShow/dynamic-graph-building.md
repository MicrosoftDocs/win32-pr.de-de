---
description: Dynamische Diagramm Bildung
ms.assetid: 13fed430-979b-40f7-91ba-aff2d811bd92
title: Dynamische Diagramm Bildung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 710bf5f648fc91e8db6bf62d81b41327f874ddf7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344327"
---
# <a name="dynamic-graph-building"></a><span data-ttu-id="877c7-103">Dynamische Diagramm Bildung</span><span class="sxs-lookup"><span data-stu-id="877c7-103">Dynamic Graph Building</span></span>

<span data-ttu-id="877c7-104">Wenn Sie ein vorhandenes Filter Diagramm ändern müssen, können Sie das Diagramm beenden, die Änderungen vornehmen und das Diagramm neu starten.</span><span class="sxs-lookup"><span data-stu-id="877c7-104">If you need to modify an existing filter graph, you can stop the graph, make the changes, and restart the graph.</span></span> <span data-ttu-id="877c7-105">Dies ist normalerweise der beste Ansatz.</span><span class="sxs-lookup"><span data-stu-id="877c7-105">This is usually the best approach.</span></span> <span data-ttu-id="877c7-106">Unter bestimmten Umständen möchten Sie jedoch möglicherweise einen Graphen ändern, während er noch ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="877c7-106">However, under some circumstances, you might want to alter a graph while it is still running.</span></span> <span data-ttu-id="877c7-107">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="877c7-107">For example:</span></span>

-   <span data-ttu-id="877c7-108">Die Anwendung fügt während der Wiedergabe einen Videoeffekt Filter ein.</span><span class="sxs-lookup"><span data-stu-id="877c7-108">The application inserts a video effects filter during playback.</span></span>
-   <span data-ttu-id="877c7-109">Ein Quell Filter schaltet die Medientypen "Mittel Strom" ein und erfordert ggf. einen neuen Dekomprimierungs Filter.</span><span class="sxs-lookup"><span data-stu-id="877c7-109">A source filter switches media types midstream, possibly requiring a new decompression filter.</span></span>
-   <span data-ttu-id="877c7-110">Die Anwendung fügt dem Diagramm einen neuen Videostream hinzu.</span><span class="sxs-lookup"><span data-stu-id="877c7-110">The application adds a new video stream to the graph.</span></span>

<span data-ttu-id="877c7-111">Dabei handelt es sich um Beispiele für das *dynamische Graph-Gebäude*, einen Begriff, der alle Arten von Änderungen an einem Filter Diagramm abdeckt, während der Graph weiterhin ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="877c7-111">These are all examples of *dynamic graph building*, a term that covers any kind of change to a filter graph while the graph continues to run.</span></span> <span data-ttu-id="877c7-112">Die dynamische Diagramm Bildung kann von einer Anwendung oder einem Filter im Diagramm initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="877c7-112">Dynamic graph building can be initiated by an application or by a filter in the graph.</span></span> <span data-ttu-id="877c7-113">Drei verschiedene Szenarien sind möglich:</span><span class="sxs-lookup"><span data-stu-id="877c7-113">Three distinct scenarios are possible:</span></span>

-   <span data-ttu-id="877c7-114">[Dynamische Format Änderungen](dynamic-format-changes.md): ein Filter kann die Formatierungen von mittlerer Stream ändern, ohne dass Filter entfernt oder ersetzt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="877c7-114">[Dynamic Format Changes](dynamic-format-changes.md): A filter can change formats midstream, without the need to remove or replace any filters.</span></span>
-   <span data-ttu-id="877c7-115">[Dynamische erneute Verbindung](dynamic-reconnection.md): das Diagramm wird durch Hinzufügen oder Entfernen von Filtern geändert.</span><span class="sxs-lookup"><span data-stu-id="877c7-115">[Dynamic Reconnection](dynamic-reconnection.md): Changing the graph by adding or removing filters.</span></span>
-   <span data-ttu-id="877c7-116">[Filter Ketten](filter-chains.md): Hinzufügen, entfernen und Steuern von Filtern von Filtern.</span><span class="sxs-lookup"><span data-stu-id="877c7-116">[Filter Chains](filter-chains.md): Adding, removing, and controlling chains of filters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="877c7-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="877c7-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="877c7-118">Informationen zu DirectShow</span><span class="sxs-lookup"><span data-stu-id="877c7-118">About DirectShow</span></span>](about-directshow.md)
</dt> </dl>

 

 



