---
description: Auflösen einer Topologie mit topoedit
ms.assetid: da3e2bbc-7c9f-4a15-8842-c1bb00662cd2
title: Auflösen einer Topologie mit topoedit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8397e380b19a6f45736c06e859d2a80456aad079
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215013"
---
# <a name="resolving-a-topology-with-topoedit"></a><span data-ttu-id="647c8-103">Auflösen einer Topologie mit topoedit</span><span class="sxs-lookup"><span data-stu-id="647c8-103">Resolving a Topology with TopoEdit</span></span>

<span data-ttu-id="647c8-104">Es gibt zwei Arten von Topologien:</span><span class="sxs-lookup"><span data-stu-id="647c8-104">There are two types of topologies:</span></span>

-   <span data-ttu-id="647c8-105">Partielle Topologie.</span><span class="sxs-lookup"><span data-stu-id="647c8-105">Partial Topology.</span></span> <span data-ttu-id="647c8-106">Der Quellknoten ist direkt mit dem Ausgabe Knoten verbunden.</span><span class="sxs-lookup"><span data-stu-id="647c8-106">The source node is connected directly to the output node.</span></span> <span data-ttu-id="647c8-107">In einigen Fällen kann eine partielle Topologie über einige zwischen Transformations Knoten verfügen, z. b. Effekte, aber nicht alle.</span><span class="sxs-lookup"><span data-stu-id="647c8-107">In some cases, a partial topology can have some intermediate transform nodes, such as effects, but not all.</span></span> <span data-ttu-id="647c8-108">Die nicht ausgelassenen Transformations Knoten sind in der Regel Decoder oder Formatierungs-MFTs, wie z. b. Farb Konverter und audioresamplers.</span><span class="sxs-lookup"><span data-stu-id="647c8-108">The transform nodes that are omitted are typically decoders or format conversion MFTs, such as color converters and audio resamplers.</span></span>

-   <span data-ttu-id="647c8-109">Vollständige Topologie.</span><span class="sxs-lookup"><span data-stu-id="647c8-109">Full Topology.</span></span> <span data-ttu-id="647c8-110">Der Quellknoten ist über einen Transformations Knoten mit dem Ausgabe Knoten verbunden.</span><span class="sxs-lookup"><span data-stu-id="647c8-110">The source node is connected to the output node through a transform node.</span></span> <span data-ttu-id="647c8-111">Dieser Topologietyp muss über jeden Knoten verfügen, um Daten verarbeiten zu können.</span><span class="sxs-lookup"><span data-stu-id="647c8-111">This type of topology must have every node to process data.</span></span>

<span data-ttu-id="647c8-112">Topoedit kann nur vollständige Topologien wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="647c8-112">TopoEdit can only play full topologies.</span></span> <span data-ttu-id="647c8-113">Topoedit verwendet das von Media Foundation bereitgestellte topologieladeobjekt, um eine partielle Topologie in eine vollständige Topologie zu konvertieren, indem die erforderlichen Transformationen eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="647c8-113">TopoEdit uses the topology loader object, provided by Media Foundation, to convert a partial topology into a full topology by inserting the required transforms.</span></span> <span data-ttu-id="647c8-114">Der Prozess der Erstellung einer vollständigen Topologie wird als Auflösen einer Topologie bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="647c8-114">The process of creating a full topology is called resolving a topology.</span></span>

<span data-ttu-id="647c8-115">Informationen zu Topologietypen finden Sie im Abschnitt partielle Topologien in Informationen [zu Topologien](about-topologies.md).</span><span class="sxs-lookup"><span data-stu-id="647c8-115">For information about topology types, see the Partial Topologies section in [About Topologies](about-topologies.md).</span></span>

<span data-ttu-id="647c8-116">Bevor Sie eine Topologie auflösen, stellen Sie Folgendes sicher:</span><span class="sxs-lookup"><span data-stu-id="647c8-116">Before you resolve a topology ensure that:</span></span>

-   <span data-ttu-id="647c8-117">Die Topologie enthält einen Quellknoten und einen Ausgabe Knoten.</span><span class="sxs-lookup"><span data-stu-id="647c8-117">The topology contains a source node and an output node.</span></span>

-   <span data-ttu-id="647c8-118">Der Quell-und der Ausgabe Knoten sind über eine gültige Knoten Verbindung verbunden.</span><span class="sxs-lookup"><span data-stu-id="647c8-118">The source and the output nodes are connected by a valid node connection.</span></span> <span data-ttu-id="647c8-119">Während der topologieauflösung überprüft das topologielader den Medientyp der Knoten auf Kompatibilität.</span><span class="sxs-lookup"><span data-stu-id="647c8-119">During topology resolution, the topology loader checks the media type of the nodes for compatibility.</span></span> <span data-ttu-id="647c8-120">Wenn eine ungültige Knoten Verbindung vorhanden ist, schlägt der Prozess fehl, und es wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="647c8-120">If an invalid node connection exists, then the process fails and an error message is displayed.</span></span>

<span data-ttu-id="647c8-121">Klicken Sie zum Auflösen einer Topologie im Menü **Topologie** auf **Topologie auflösen**.</span><span class="sxs-lookup"><span data-stu-id="647c8-121">To resolve a topology, from the **Topology** menu, click **Resolve Topology**.</span></span>

<span data-ttu-id="647c8-122">Die Symbolleiste gibt den Status der Topologie an: **\[ aufgelöst \]** oder **\[ nicht aufgelöst \]**.</span><span class="sxs-lookup"><span data-stu-id="647c8-122">The toolbar indicates the topology status: **\[Resolved\]** or **\[Not Resolved\]**.</span></span>

<span data-ttu-id="647c8-123">Wenn topoedit eine Topologie erfolgreich auflöst, wird der **topologiestatus** auf **\[ aufgelöst \]** festgelegt, und die Wiedergabe Steuerelemente werden aktiviert.</span><span class="sxs-lookup"><span data-stu-id="647c8-123">If TopoEdit resolves a topology successfully, **Topology Status** is set to **\[Resolved\]** and the playback controls are enabled.</span></span>

<span data-ttu-id="647c8-124">Jedes Mal, wenn Sie Änderungen an der Topologie vornehmen, wird der **topologiestatus** auf **\[ nicht aufgelöst \]** festgelegt, was darauf hinweist, dass er erneut aufgelöst werden muss.</span><span class="sxs-lookup"><span data-stu-id="647c8-124">Each time you make changes to the topology, **Topology Status** is set to **\[Not Resolved\]** which indicates that it must be resolved again.</span></span>

## <a name="related-topics"></a><span data-ttu-id="647c8-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="647c8-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="647c8-126">Entwickeln von Topologien mithilfe von topoedit</span><span class="sxs-lookup"><span data-stu-id="647c8-126">Building Topologies by Using TopoEdit</span></span>](building-topologies-by-using-topoedit.md)
</dt> <dt>

[<span data-ttu-id="647c8-127">Topoedit</span><span class="sxs-lookup"><span data-stu-id="647c8-127">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 



