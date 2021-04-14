---
description: Erstellen von Topologien
ms.assetid: afd1e646-9bb6-4265-a225-6aaaf1a7bb2a
title: Erstellen von Topologien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a9ec738c82ea2b85bcae7d4c05627b81ad939db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393294"
---
# <a name="creating-topologies"></a><span data-ttu-id="646ce-103">Erstellen von Topologien</span><span class="sxs-lookup"><span data-stu-id="646ce-103">Creating Topologies</span></span>

<span data-ttu-id="646ce-104">In diesem Abschnitt werden einige der allgemeinen Verfahren zum Erstellen einer Topologie beschrieben.</span><span class="sxs-lookup"><span data-stu-id="646ce-104">This section describes some of the general procedures for creating a topology.</span></span>

<span data-ttu-id="646ce-105">Die allgemeinen Schritte zum Erstellen einer Topologie lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="646ce-105">The general steps for creating a topology are as follows:</span></span>

1.  <span data-ttu-id="646ce-106">Erstellen Sie ein neues Topologieobjekt durch Aufrufen von [**mfcreatetopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span><span class="sxs-lookup"><span data-stu-id="646ce-106">Create a new topology object by calling [**MFCreateTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopology).</span></span> <span data-ttu-id="646ce-107">Diese Funktion gibt einen Zeiger auf die [**imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) -Schnittstelle der Topologie zurück.</span><span class="sxs-lookup"><span data-stu-id="646ce-107">This function returns a pointer to the topology's [**IMFTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology) interface.</span></span>

2.  <span data-ttu-id="646ce-108">Anfänglich enthält die Topologie keine Knoten.</span><span class="sxs-lookup"><span data-stu-id="646ce-108">Initially, the topology does not contain any nodes.</span></span> <span data-ttu-id="646ce-109">Um Knoten für die Topologie zu erstellen, rufen Sie [**mfkreatetopologynode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode)auf.</span><span class="sxs-lookup"><span data-stu-id="646ce-109">To create nodes for the topology, call [**MFCreateTopologyNode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode).</span></span> <span data-ttu-id="646ce-110">Diese Funktion gibt einen Zeiger auf die [**imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) -Schnittstelle des Knotens zurück.</span><span class="sxs-lookup"><span data-stu-id="646ce-110">This function returns a pointer to the node's [**IMFTopologyNode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode) interface.</span></span> <span data-ttu-id="646ce-111">Beim Erstellen des Knotens müssen Sie den Knotentyp angeben:</span><span class="sxs-lookup"><span data-stu-id="646ce-111">You must specify the node type when you create the node:</span></span>

    -   <span data-ttu-id="646ce-112">Quellknoten.</span><span class="sxs-lookup"><span data-stu-id="646ce-112">Source node.</span></span>

    -   <span data-ttu-id="646ce-113">Knoten transformieren.</span><span class="sxs-lookup"><span data-stu-id="646ce-113">Transform node.</span></span>

    -   <span data-ttu-id="646ce-114">Ausgabe Knoten.</span><span class="sxs-lookup"><span data-stu-id="646ce-114">Output node.</span></span>

    -   <span data-ttu-id="646ce-115">Tee-Knoten.</span><span class="sxs-lookup"><span data-stu-id="646ce-115">Tee node.</span></span>

3.  <span data-ttu-id="646ce-116">Initialisieren Sie jeden Knoten.</span><span class="sxs-lookup"><span data-stu-id="646ce-116">Initialize each node.</span></span> <span data-ttu-id="646ce-117">Der Initialisierungs Prozess hängt vom Knotentyp ab, wie in den folgenden Themen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="646ce-117">The initialization process depends on the node type, as described in the topics that follow.</span></span>

4.  <span data-ttu-id="646ce-118">Fügen Sie jeden Knoten der Topologie hinzu, indem Sie [**imftopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="646ce-118">Add each node to the topology by calling [**IMFTopology::AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode).</span></span>

5.  <span data-ttu-id="646ce-119">Verbinden Sie die Knoten.</span><span class="sxs-lookup"><span data-stu-id="646ce-119">Connect the nodes.</span></span> <span data-ttu-id="646ce-120">Um einen Knoten zu verbinden, nennen Sie [**imftopologynode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) auf dem upstreamknoten, und übergeben Sie einen Zeiger auf den downstreamknoten.</span><span class="sxs-lookup"><span data-stu-id="646ce-120">To connect a node, call [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) on the upstream node, and pass in a pointer to the downstream node.</span></span>

<span data-ttu-id="646ce-121">In den folgenden Themen werden die spezifischen Schritte für die einzelnen Knoten Typen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="646ce-121">The following topics give the specific steps for each node type.</span></span>



| <span data-ttu-id="646ce-122">Thema</span><span class="sxs-lookup"><span data-stu-id="646ce-122">Topic</span></span>                                                    | <span data-ttu-id="646ce-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="646ce-123">Description</span></span>                     |
|----------------------------------------------------------|---------------------------------|
| [<span data-ttu-id="646ce-124">Erstellen von Quellknoten</span><span class="sxs-lookup"><span data-stu-id="646ce-124">Creating Source Nodes</span></span>](creating-source-nodes.md)       | <span data-ttu-id="646ce-125">Erstellen eines Quell Knotens</span><span class="sxs-lookup"><span data-stu-id="646ce-125">How to create a source node.</span></span>    |
| [<span data-ttu-id="646ce-126">Erstellen von Transformations Knoten</span><span class="sxs-lookup"><span data-stu-id="646ce-126">Creating Transform Nodes</span></span>](creating-transform-nodes.md) | <span data-ttu-id="646ce-127">So erstellen Sie einen Transformations Knoten.</span><span class="sxs-lookup"><span data-stu-id="646ce-127">How to create a transform node.</span></span> |
| [<span data-ttu-id="646ce-128">Erstellen von Ausgabe Knoten</span><span class="sxs-lookup"><span data-stu-id="646ce-128">Creating Output Nodes</span></span>](creating-output-nodes.md)       | <span data-ttu-id="646ce-129">So erstellen Sie einen Ausgabe Knoten.</span><span class="sxs-lookup"><span data-stu-id="646ce-129">How to create an output node.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="646ce-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="646ce-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="646ce-131">Topologien</span><span class="sxs-lookup"><span data-stu-id="646ce-131">Topologies</span></span>](topologies.md)
</dt> </dl>

 

 



