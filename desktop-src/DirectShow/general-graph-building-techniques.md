---
description: Allgemeine Graph-Building Techniken
ms.assetid: 66d93305-175c-4549-b825-2f3d7fd6bf09
title: Allgemeine Graph-Building Techniken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c73a005f1fbf7af0a53f11d44d600852f88752
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213825"
---
# <a name="general-graph-building-techniques"></a><span data-ttu-id="40501-103">Allgemeine Graph-Building Techniken</span><span class="sxs-lookup"><span data-stu-id="40501-103">General Graph-Building Techniques</span></span>

<span data-ttu-id="40501-104">Alle DirectShow-Anwendungen beginnen mit dem Aufbau eines Filter Diagramms.</span><span class="sxs-lookup"><span data-stu-id="40501-104">Every DirectShow application starts by building a filter graph.</span></span> <span data-ttu-id="40501-105">Wenn Sie die Übersichts Themen in der DirectShow-Dokumentation lesen, werden Sie zunächst feststellen, welche Art von Filter Diagramm Sie benötigen.</span><span class="sxs-lookup"><span data-stu-id="40501-105">As you read the overview topics in the DirectShow documentation, you will find that most start by describing what kind of filter graph you need.</span></span> <span data-ttu-id="40501-106">In einigen Fällen gibt es eine Methode oder ein Hilfsobjekt, das speziell zum entwickeln dieses Diagramm Typs entworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="40501-106">In some cases, there is a method or a helper object specifically designed for building that type of graph.</span></span> <span data-ttu-id="40501-107">Beispielsweise erstellt das [DVD Graph Builder](dvd-graph-builder.md) -Objekt DVD-Wiedergabe Diagramme.</span><span class="sxs-lookup"><span data-stu-id="40501-107">For example, the [DVD Graph Builder](dvd-graph-builder.md) object builds DVD playback graphs.</span></span> <span data-ttu-id="40501-108">In anderen Fällen muss die Anwendung das Diagramm erstellen, indem Sie Filter hinzufügen und Sie miteinander verbinden.</span><span class="sxs-lookup"><span data-stu-id="40501-108">In other cases, the application must construct the graph by adding filters and connecting them.</span></span>

<span data-ttu-id="40501-109">In diesem Abschnitt werden einige Hilfsfunktionen vorgestellt, die grundlegende Graph-Building-Vorgänge implementieren.</span><span class="sxs-lookup"><span data-stu-id="40501-109">This section presents some helper functions that implement basic graph-building operations.</span></span> <span data-ttu-id="40501-110">Sie können von jeder DirectShow-Anwendung verwendet werden, die ein Filter Diagramm erstellen oder ändern muss.</span><span class="sxs-lookup"><span data-stu-id="40501-110">They can be used by any DirectShow application that needs to build or modify a filter graph.</span></span> <span data-ttu-id="40501-111">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="40501-111">This section contains the following topics:</span></span>

-   [<span data-ttu-id="40501-112">Filter nach CLSID hinzufügen</span><span class="sxs-lookup"><span data-stu-id="40501-112">Add a Filter by CLSID</span></span>](add-a-filter-by-clsid.md)
-   [<span data-ttu-id="40501-113">Suchen einer nicht verbundenen PIN für einen Filter</span><span class="sxs-lookup"><span data-stu-id="40501-113">Find an Unconnected Pin on a Filter</span></span>](find-an-unconnected-pin-on-a-filter.md)
-   [<span data-ttu-id="40501-114">Zwei Filter verbinden</span><span class="sxs-lookup"><span data-stu-id="40501-114">Connect Two Filters</span></span>](connect-two-filters.md)
-   [<span data-ttu-id="40501-115">Suchen einer Schnittstelle in einem Filter oder einer PIN</span><span class="sxs-lookup"><span data-stu-id="40501-115">Find an Interface on a Filter or Pin</span></span>](find-an-interface-on-a-filter-or-pin.md)
-   [<span data-ttu-id="40501-116">Suchen eines Filter-Peers</span><span class="sxs-lookup"><span data-stu-id="40501-116">Find a Filter's Peer</span></span>](find-a-filters-peer.md)
-   [<span data-ttu-id="40501-117">Alle Filter im Diagramm entfernen</span><span class="sxs-lookup"><span data-stu-id="40501-117">Remove All the Filters in the Graph</span></span>](remove-all-the-filters-in-the-graph.md)
-   [<span data-ttu-id="40501-118">Erstellen von Diagrammen mit dem Erfassungs Diagramm-Generator</span><span class="sxs-lookup"><span data-stu-id="40501-118">Building Graphs with the Capture Graph Builder</span></span>](building-graphs-with-the-capture-graph-builder.md)

## <a name="related-topics"></a><span data-ttu-id="40501-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="40501-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40501-120">Grundlegende DirectShow-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="40501-120">Basic DirectShow Tasks</span></span>](basic-directshow-tasks.md)
</dt> <dt>

[<span data-ttu-id="40501-121">Auflisten von Geräten und Filtern</span><span class="sxs-lookup"><span data-stu-id="40501-121">Enumerating Devices and Filters</span></span>](enumerating-devices-and-filters.md)
</dt> <dt>

[<span data-ttu-id="40501-122">Auflisten von Objekten in einem Filter Diagramm</span><span class="sxs-lookup"><span data-stu-id="40501-122">Enumerating Objects in a Filter Graph</span></span>](enumerating-objects-in-a-filter-graph.md)
</dt> <dt>

[<span data-ttu-id="40501-123">Intelligent Connect</span><span class="sxs-lookup"><span data-stu-id="40501-123">Intelligent Connect</span></span>](intelligent-connect.md)
</dt> </dl>

 

 



