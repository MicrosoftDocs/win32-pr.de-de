---
description: Simulieren der Diagramm Erstellung mit GraphEdit
ms.assetid: 3f7d3079-3d3d-4b93-9ab7-4c03def7c4be
title: Simulieren der Diagramm Erstellung mit GraphEdit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f76878997c873c74d454979ccda689a9c241489d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481966"
---
# <a name="simulating-graph-building-with-graphedit"></a><span data-ttu-id="1e153-103">Simulieren der Diagramm Erstellung mit GraphEdit</span><span class="sxs-lookup"><span data-stu-id="1e153-103">Simulating Graph Building with GraphEdit</span></span>

<span data-ttu-id="1e153-104">DirectShow bietet ein debughilfsprogramm mit dem Namen GraphEdit, das Sie zum Erstellen und Testen von Filter Diagrammen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="1e153-104">DirectShow provides a debugging utility called GraphEdit, which you can use to create and test filter graphs.</span></span>

<span data-ttu-id="1e153-105">GraphEdit ist ein visuelles Tool zum Entwickeln von Filter Diagrammen.</span><span class="sxs-lookup"><span data-stu-id="1e153-105">GraphEdit is a visual tool for building filter graphs.</span></span> <span data-ttu-id="1e153-106">Mit GraphEdit können Sie mit einem Filter Diagramm experimentieren, bevor Sie Anwendungscode schreiben.</span><span class="sxs-lookup"><span data-stu-id="1e153-106">With GraphEdit, you can experiment with a filter graph before you write any application code.</span></span> <span data-ttu-id="1e153-107">Sie können auch ein Filter Diagramm laden, das von der Anwendung erstellt wird, um zu überprüfen, ob die Anwendung das richtige Diagramm erstellt.</span><span class="sxs-lookup"><span data-stu-id="1e153-107">You can also load a filter graph that your application creates, to verify that your application is building the correct graph.</span></span> <span data-ttu-id="1e153-108">Wenn Sie einen benutzerdefinierten Filter entwickeln, bietet GraphEdit eine schnelle Möglichkeit, Sie zu testen: Laden Sie einfach ein Diagramm mit Ihrem benutzerdefinierten Filter, und führen Sie das Diagramm aus.</span><span class="sxs-lookup"><span data-stu-id="1e153-108">If you develop a custom filter, GraphEdit provides a quick way to test it: Simply load a graph with your custom filter and try running the graph.</span></span> <span data-ttu-id="1e153-109">Wenn Sie mit DirectShow noch nicht vertraut sind, ist GraphEdit eine gute Möglichkeit, sich mit Filter Diagrammen und der DirectShow-Architektur vertraut zu machen.</span><span class="sxs-lookup"><span data-stu-id="1e153-109">If you are new to DirectShow, GraphEdit is a good way to become familiar with filter graphs and the DirectShow architecture.</span></span>

<span data-ttu-id="1e153-110">Die folgende Abbildung zeigt, wie GraphEdit ein einfaches Filter Diagramm darstellt.</span><span class="sxs-lookup"><span data-stu-id="1e153-110">The following illustration shows how GraphEdit represents a simple filter graph.</span></span>

![einfaches Filter Diagramm in GraphEdit](images/gedit09.png)

<span data-ttu-id="1e153-112">Jeder Filter wird als Rechteck dargestellt.</span><span class="sxs-lookup"><span data-stu-id="1e153-112">Each filter is represented as a rectangle.</span></span> <span data-ttu-id="1e153-113">Kleinere Quadrate entlang der Kanten der Filter stellen Pins dar.</span><span class="sxs-lookup"><span data-stu-id="1e153-113">Smaller squares along the edges of the filters represent pins.</span></span> <span data-ttu-id="1e153-114">Eingabe Pins befinden sich auf der linken Seite des Filters, und die Ausgabe Pins befinden sich auf der rechten Seite.</span><span class="sxs-lookup"><span data-stu-id="1e153-114">Input pins are on the left side of the filter, and output pins are on the right side.</span></span> <span data-ttu-id="1e153-115">Die Pfeile stellen die Verbindungen zwischen Pins dar.</span><span class="sxs-lookup"><span data-stu-id="1e153-115">The arrows represent the connections between pins.</span></span>

<span data-ttu-id="1e153-116">Mit GraphEdit können Sie folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="1e153-116">With GraphEdit, you can:</span></span>

-   <span data-ttu-id="1e153-117">Erstellen und Ändern von Filter Diagrammen mithilfe einer visuellen Drag & amp; Drop-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="1e153-117">Create and modify filter graphs using a visual, drag-and-drop interface.</span></span>
-   <span data-ttu-id="1e153-118">Simulieren Sie programmgesteuerte Aufrufe, um ein Diagramm zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1e153-118">Simulate programmatic calls to build a graph.</span></span>
-   <span data-ttu-id="1e153-119">Ausführen, anhalten, anhalten und Suchen eines Diagramms.</span><span class="sxs-lookup"><span data-stu-id="1e153-119">Run, pause, stop, and seek a graph.</span></span>
-   <span data-ttu-id="1e153-120">Sehen Sie sich an, welche Filter auf Ihrem Computer registriert sind, und zeigen Sie Registrierungsinformationen für die einzelnen Filter an.</span><span class="sxs-lookup"><span data-stu-id="1e153-120">See what filters are registered on your computer, and view registry information for each filter.</span></span>
-   <span data-ttu-id="1e153-121">Filtereigenschaften Seiten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="1e153-121">View filter property pages.</span></span>
-   <span data-ttu-id="1e153-122">Zeigen Sie die Medientypen der PIN-Verbindungen an.</span><span class="sxs-lookup"><span data-stu-id="1e153-122">View the media types of pin connections.</span></span>

<span data-ttu-id="1e153-123">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="1e153-123">This section contains the following topics:</span></span>

-   [<span data-ttu-id="1e153-124">Verwenden von GraphEdit</span><span class="sxs-lookup"><span data-stu-id="1e153-124">Using GraphEdit</span></span>](using-graphedit.md)
-   [<span data-ttu-id="1e153-125">Laden eines Diagramms aus einem externen Prozess</span><span class="sxs-lookup"><span data-stu-id="1e153-125">Loading a Graph From an External Process</span></span>](loading-a-graph-from-an-external-process.md)
-   [<span data-ttu-id="1e153-126">Speichern eines Filter Diagramms in einer GraphEdit-Datei</span><span class="sxs-lookup"><span data-stu-id="1e153-126">Saving a Filter Graph to a GraphEdit File</span></span>](saving-a-filter-graph-to-a-graphedit-file.md)
-   [<span data-ttu-id="1e153-127">Programm gesteuertes Laden einer GraphEdit-Datei</span><span class="sxs-lookup"><span data-stu-id="1e153-127">Loading a GraphEdit File Programmatically</span></span>](loading-a-graphedit-file-programmatically.md)
-   [<span data-ttu-id="1e153-128">GraphEdit-Datei Format</span><span class="sxs-lookup"><span data-stu-id="1e153-128">GraphEdit File Format</span></span>](graphedit-file-format.md)

## <a name="related-topics"></a><span data-ttu-id="1e153-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1e153-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e153-130">Verwenden von DirectShow</span><span class="sxs-lookup"><span data-stu-id="1e153-130">Using DirectShow</span></span>](using-directshow.md)
</dt> </dl>

 

 



