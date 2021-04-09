---
description: Entwickeln von Topologien mithilfe von topoedit
ms.assetid: 04173f3d-3722-48ee-a6fb-9cdb2a897a33
title: Entwickeln von Topologien mithilfe von topoedit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92758911113c7500cb13fa814d07321435fafeb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128000"
---
# <a name="building-topologies-by-using-topoedit"></a><span data-ttu-id="dd1f8-103">Entwickeln von Topologien mithilfe von topoedit</span><span class="sxs-lookup"><span data-stu-id="dd1f8-103">Building Topologies by Using TopoEdit</span></span>

<span data-ttu-id="dd1f8-104">Eine Topologie muss über die folgenden drei Knoten verfügen:</span><span class="sxs-lookup"><span data-stu-id="dd1f8-104">A topology must have the following three nodes:</span></span>

-   <span data-ttu-id="dd1f8-105">Quellknoten: die Datenströme aus einer Mediendatei, die als Quelle für die Topologie verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-105">Source node: The streams from a media file, which are used as a source for the topology.</span></span>
-   <span data-ttu-id="dd1f8-106">Transformations Knoten: eine Media Foundation Transformation (MFT).</span><span class="sxs-lookup"><span data-stu-id="dd1f8-106">Transform node: A Media Foundation transform (MFT).</span></span> <span data-ttu-id="dd1f8-107">Diese Knoten sind in der Regel Encoder, Decoder und Effekte für die Topologie.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-107">These nodes are usually encoders, decoders, and effects for the topology.</span></span>
-   <span data-ttu-id="dd1f8-108">Ausgabe Knoten: die streamsenke, die die Mediendaten, Video Frames oder Audiostreams zur Wiedergabe an die Medien Sitzung übergibt.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-108">Output node: The stream sink that passes the media data, video frames, or audio streams to the Media Session for playback.</span></span>

<span data-ttu-id="dd1f8-109">Weitere Informationen zur topologiestruktur finden Sie unter Informationen [zu Topologien](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="dd1f8-109">For information about topology structure, see [About Topologies](about-topologies.md).</span></span>

<span data-ttu-id="dd1f8-110">Zum Erstellen einer Topologie müssen Sie die Knoten hinzufügen, die Knoten verbinden und die Topologie auflösen, damit Sie wiedergegeben werden kann.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-110">To build a topology, you must add the nodes, connect the nodes, and resolve the topology so that it can be played.</span></span>

<span data-ttu-id="dd1f8-111">Topologieknoten werden als Felder mit Text angezeigt, der den Namen des Knotens anzeigt.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-111">Topology nodes are displayed as boxes, with text showing the name of the node.</span></span> <span data-ttu-id="dd1f8-112">Grüne Felder stellen die Knoten dar, die vom Benutzer hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-112">Green boxes represent the nodes that are added by the user.</span></span> <span data-ttu-id="dd1f8-113">Wenn eine Topologie aufgelöst wird, kann topoedit der Topologie automatisch Transformations Knoten hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-113">When a topology is resolved, TopoEdit can add transform nodes to the topology automatically.</span></span> <span data-ttu-id="dd1f8-114">Diese werden im **Topologiebereich** als blaue Felder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-114">These appear as blue boxes on the **Topology Pane**.</span></span>

<span data-ttu-id="dd1f8-115">Topologieeingaben und-Ausgaben werden als schwarze Quadrate entlang der Kante des Knotens dargestellt.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-115">Topology inputs and outputs are represented by as black squares along the edge of the node.</span></span> <span data-ttu-id="dd1f8-116">Die *Knoten Eingabe* wird auf der linken Seite des Knotens angezeigt, und die *Knoten Ausgabe* befindet sich auf der rechten Seite des Knotens.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-116">The *node input* is shown on the left side of the node, and the *node output* is on the right side of the node.</span></span>

<span data-ttu-id="dd1f8-117">Die topologieknoten sind über eine *Knoten Verbindung* verbunden, die als schwarze Linie angezeigt wird, um die Knoten Eingabe eines Knotens mit der Knoten Ausgabe eines anderen Knotens zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-117">The topology nodes are connected through a *node connection* that appears as a black line connecting the node input of one node to the node output of another node.</span></span>

<span data-ttu-id="dd1f8-118">Die folgende Abbildung zeigt eine verbundene Topologie für eine Audioquelle.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-118">The following illustration shows a connected topology for an audio source.</span></span>

![Darstellung der Verbindungen vom Quellknoten zu zwei Transformations Knoten und dann zum Ausgabe Knoten](images/e94b4cce-aa8a-497f-94c2-cc9dace17291.gif)

<span data-ttu-id="dd1f8-120">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="dd1f8-120">This section contains the following topics:</span></span>



| <span data-ttu-id="dd1f8-121">Thema</span><span class="sxs-lookup"><span data-stu-id="dd1f8-121">Topic</span></span>                                                                                          | <span data-ttu-id="dd1f8-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dd1f8-122">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="dd1f8-123">Hinzufügen von Quellknoten mit topoedit</span><span class="sxs-lookup"><span data-stu-id="dd1f8-123">Adding Source Nodes with TopoEdit</span></span>](adding-source-nodes-with-topoedit.md)                     | <span data-ttu-id="dd1f8-124">Beschreibt den Prozess des Hinzufügens von Quellknoten zu einer Topologie.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-124">Describes the process of adding source nodes to a topology.</span></span>    |
| [<span data-ttu-id="dd1f8-125">Hinzufügen von Transformations Knoten mit topoedit</span><span class="sxs-lookup"><span data-stu-id="dd1f8-125">Adding Transform Nodes with TopoEdit</span></span>](adding-transform-nodes-with-topoedit.md)               | <span data-ttu-id="dd1f8-126">Beschreibt den Prozess des Hinzufügens von Transformations Knoten zu einer Topologie.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-126">Describes the process of adding transform nodes to a topology.</span></span> |
| [<span data-ttu-id="dd1f8-127">Hinzufügen von Ausgabe Knoten mit topoedit</span><span class="sxs-lookup"><span data-stu-id="dd1f8-127">Adding Output Nodes with TopoEdit</span></span>](adding-output-nodes-with-topoedit.md)                     | <span data-ttu-id="dd1f8-128">Beschreibt den Prozess des Hinzufügens von Ausgabe Knoten zu einer Topologie.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-128">Describes the process of adding output nodes to a topology.</span></span>    |
| [<span data-ttu-id="dd1f8-129">Verbinden von topologieknoten und Trennen der Verbindung</span><span class="sxs-lookup"><span data-stu-id="dd1f8-129">Connecting and Disconnecting Topology Nodes</span></span>](connecting-and-disconnecting-topology-nodes.md) | <span data-ttu-id="dd1f8-130">Beschreibt den Prozess zum Verbinden von zwei Knoten.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-130">Describes the process of connecting two nodes.</span></span>                 |
| [<span data-ttu-id="dd1f8-131">Auflösen einer Topologie mit topoedit</span><span class="sxs-lookup"><span data-stu-id="dd1f8-131">Resolving a Topology with TopoEdit</span></span>](resolving-a-topology-with-topoedit.md)                   | <span data-ttu-id="dd1f8-132">Beschreibt den Prozess der topologieauflösung.</span><span class="sxs-lookup"><span data-stu-id="dd1f8-132">Describes the process of topology resolution.</span></span>                  |



 

## <a name="related-topics"></a><span data-ttu-id="dd1f8-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="dd1f8-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dd1f8-134">Topoedit</span><span class="sxs-lookup"><span data-stu-id="dd1f8-134">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



