---
description: Verbinden von topologieknoten und Trennen der Verbindung
ms.assetid: b2f70989-f0a8-4a11-baeb-18f026afaeab
title: Verbinden von topologieknoten und Trennen der Verbindung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08057eba74314ae6b87da418b743a089506a3b26
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344235"
---
# <a name="connecting-and-disconnecting-topology-nodes"></a><span data-ttu-id="42617-103">Verbinden von topologieknoten und Trennen der Verbindung</span><span class="sxs-lookup"><span data-stu-id="42617-103">Connecting and Disconnecting Topology Nodes</span></span>

<span data-ttu-id="42617-104">Damit eine Topologie funktionsfähig ist, müssen der Quellknoten und der Ausgabe Knoten verbunden sein.</span><span class="sxs-lookup"><span data-stu-id="42617-104">For a topology to be functional, the source node and the output node must be connected.</span></span> <span data-ttu-id="42617-105">Um zwei topologieknoten zu verbinden, ziehen Sie die Knoten Ausgabe eines Knotens auf die Knoten Eingabe des anderen Knotens.</span><span class="sxs-lookup"><span data-stu-id="42617-105">To connect two topology nodes, drag the node output of one node to the node input of the other node.</span></span> <span data-ttu-id="42617-106">In topoedit wird die Knoten Verbindung als schwarze Linie angezeigt.</span><span class="sxs-lookup"><span data-stu-id="42617-106">TopoEdit displays the node connection as a black line.</span></span> <span data-ttu-id="42617-107">Dies entspricht dem Verbinden von topologieknoten durch Aufrufen der [**imftopologynode:: ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) -Methode.</span><span class="sxs-lookup"><span data-stu-id="42617-107">This is equivalent to connecting topology nodes by calling the [**IMFTopologyNode::ConnectOutput**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-connectoutput) method.</span></span>

<span data-ttu-id="42617-108">Die Topologie kann nur aufgelöst werden, wenn die Knoten Verbindung gültig ist. Das heißt, wenn die Medientypen der beiden Knoten kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="42617-108">The topology can be resolved only if the node connection is valid; that is, if the media types of the two nodes are compatible.</span></span> <span data-ttu-id="42617-109">Informationen zum Auflösen von Topologien finden Sie unter [Auflösen einer Topologie mit topoedit](resolving-a-topology-with-topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="42617-109">For information about resolving topologies, see [Resolving a Topology with TopoEdit](resolving-a-topology-with-topoedit.md).</span></span>

<span data-ttu-id="42617-110">Wenn Sie versuchen, eine Verbindung von einem bereits verbundenen Knoten herzustellen, ersetzt die neue Knoten Verbindung die alte Knoten Verbindung.</span><span class="sxs-lookup"><span data-stu-id="42617-110">If you attempt to make a connection from a node that is already connected, the new node connection replaces the old node connection.</span></span>

<span data-ttu-id="42617-111">Um eine Verbindung zu löschen, wählen Sie die Knoten Verbindung aus, und drücken Sie die ENTF-Taste, oder wählen Sie **Löschen** aus dem Menü **Topologie** .</span><span class="sxs-lookup"><span data-stu-id="42617-111">To delete a connection, select the node connection and press the DELETE key or select **Delete** from the **Topology** menu.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42617-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="42617-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42617-113">Entwickeln von Topologien mithilfe von topoedit</span><span class="sxs-lookup"><span data-stu-id="42617-113">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="42617-114">Topoedit</span><span class="sxs-lookup"><span data-stu-id="42617-114">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



