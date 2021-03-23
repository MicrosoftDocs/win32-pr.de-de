---
title: Untergeordnete Zuordnung innerhalb von Puffern
description: Puffer verfügen über alle Features, die in D3D12 erforderlich sind, damit Anwendungen einen großen Bereich vorübergehender Daten von der CPU auf die GPU übertragen können. In diesem Abschnitt werden vier häufige Szenarien für die Verwendung und Verwaltung von Ressourcen und Puffern behandelt.
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64944cb11507b8dc437d075938fad419f333433
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104462"
---
# <a name="suballocation-within-buffers"></a><span data-ttu-id="9de0a-104">Untergeordnete Zuordnung innerhalb von Puffern</span><span class="sxs-lookup"><span data-stu-id="9de0a-104">Suballocation Within Buffers</span></span>

<span data-ttu-id="9de0a-105">Puffer verfügen über alle Features, die in D3D12 erforderlich sind, damit Anwendungen einen großen Bereich vorübergehender Daten von der CPU auf die GPU übertragen können.</span><span class="sxs-lookup"><span data-stu-id="9de0a-105">Buffers have all the features necessary in D3D12 for applications to transfer a large range of transient data from the CPU to the GPU.</span></span> <span data-ttu-id="9de0a-106">In diesem Abschnitt werden vier häufige Szenarien für die Verwendung und Verwaltung von Ressourcen und Puffern behandelt.</span><span class="sxs-lookup"><span data-stu-id="9de0a-106">This section covers four common scenarios for the use and management of resources and buffers.</span></span>

<span data-ttu-id="9de0a-107">Ähnlich wie bei D3D11 müssen Anwendungen in D3D12 weiterhin die Verwendung des Arbeitsspeichers deklarieren, wenn Puffer in D3D12 im Vergleich zu dynamischen/stagingressourcen in D3D11 zugeordnet werden, aber in D3D12 haben Entwickler mehr Flexibilität und eine strengere Kontrolle über die Speicherauslastung.</span><span class="sxs-lookup"><span data-stu-id="9de0a-107">Similar to D3D11, applications in D3D12 still need to declare the usage of memory when allocating buffers in D3D12 compared to Dynamic/Staging Resources in D3D11, but in D3D12, developers have more flexibility and tighter control over memory usage.</span></span> <span data-ttu-id="9de0a-108">Puffer über die unter Zuweisung verfügen über alle Features, die für die Speicherverwaltung auf niedriger Ebene erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9de0a-108">Buffers, through suballocation, have all the features necessary for low-level memory management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9de0a-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9de0a-109">In this section</span></span>



| <span data-ttu-id="9de0a-110">Thema</span><span class="sxs-lookup"><span data-stu-id="9de0a-110">Topic</span></span>                                                                                        | <span data-ttu-id="9de0a-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9de0a-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9de0a-112">Hochladen verschiedener Arten von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9de0a-112">Uploading Different Types of Resources</span></span>](uploading-resources.md)<br/>                 | <span data-ttu-id="9de0a-113">Zeigt, wie ein Puffer verwendet wird, um sowohl Konstante Puffer Daten als auch Vertex-Puffer Daten in die GPU hochzuladen und Daten in Puffern ordnungsgemäß zuzuordnen und zu platzieren.</span><span class="sxs-lookup"><span data-stu-id="9de0a-113">Shows how to use one buffer to upload both constant buffer data and vertex buffer data to the GPU, and how to properly sub-allocate and place data within buffers.</span></span> <span data-ttu-id="9de0a-114">Die Verwendung eines einzelnen Puffers steigert die Flexibilität der Speicherauslastung und bietet Anwendungen eine strengere Kontrolle der Speicherauslastung.</span><span class="sxs-lookup"><span data-stu-id="9de0a-114">The use of one single buffer increases memory usage flexibility and provides applications with tighter control of memory usage.</span></span> <span data-ttu-id="9de0a-115">Zeigt außerdem die Unterschiede zwischen den D3D11-und D3D12-Modellen zum Hochladen unterschiedlicher Ressourcentypen.</span><span class="sxs-lookup"><span data-stu-id="9de0a-115">Also shows the differences between the D3D11 and D3D12 models for uploading different types of resources.</span></span><br/> |
| [<span data-ttu-id="9de0a-116">Hochladen von Textur Daten über Puffer</span><span class="sxs-lookup"><span data-stu-id="9de0a-116">Uploading Texture Data Through Buffers</span></span>](upload-and-readback-of-texture-data.md)<br/> | <span data-ttu-id="9de0a-117">Das Hochladen von 2D-oder 3D-Textur Daten ähnelt dem Hochladen von 1D-Daten, mit dem Unterschied, dass Anwendungen die Daten Ausrichtung im Zusammenhang mit der Zeilen Tonhöhe genauer berücksichtigen müssen.</span><span class="sxs-lookup"><span data-stu-id="9de0a-117">Uploading 2D or 3D texture data is similar to uploading 1D data, except that applications need to pay closer attention to data alignment related to row pitch.</span></span> <span data-ttu-id="9de0a-118">Puffer können von mehreren Teilen der Grafik Pipeline orthogonell und gleichzeitig verwendet werden und sind sehr flexibel.</span><span class="sxs-lookup"><span data-stu-id="9de0a-118">Buffers can be used orthogonally and concurrently from multiple parts of the graphics pipeline, and are very flexible.</span></span> <br/>                                                                                                                       |
| [<span data-ttu-id="9de0a-119">Zurück Lesen von Daten über einen Puffer</span><span class="sxs-lookup"><span data-stu-id="9de0a-119">Read back data via a buffer</span></span>](readback-data-using-heaps.md)<br/>                    | <span data-ttu-id="9de0a-120">Beim Lesen von Daten aus der GPU, z. b. beim Aufzeichnen eines Screenshots, wird der readback-Heap verwendet.</span><span class="sxs-lookup"><span data-stu-id="9de0a-120">Reading back data from the GPU, such as capturing a screen shot, involves the use of the Readback heap.</span></span> <br/>                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="9de0a-121">Auf der Fence basierende Ressourcenverwaltung</span><span class="sxs-lookup"><span data-stu-id="9de0a-121">Fence-Based Resource Management</span></span>](fence-based-resource-management.md)<br/>            | <span data-ttu-id="9de0a-122">Zeigt, wie die Lebensdauer von Ressourcen Daten verwaltet wird, indem der GPU-Status über Zäune nachverfolgt wird.</span><span class="sxs-lookup"><span data-stu-id="9de0a-122">Shows how to manage resource data life-span by tracking GPU progress via fences.</span></span> <span data-ttu-id="9de0a-123">Der Arbeitsspeicher kann mit der Verwendung von Zäunen, die die Verfügbarkeit von freiem Speicherplatz im Arbeitsspeicher sorgfältig verwalten, wie z. b. in einer Ringpuffer Implementierung für einen uploadheap</span><span class="sxs-lookup"><span data-stu-id="9de0a-123">Memory can be effectively re-used with fences carefully managing the availability of free space in memory, such as in a ring buffer implementation for an Upload heap.</span></span> <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="9de0a-124">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="9de0a-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9de0a-125">Speicherverwaltung</span><span class="sxs-lookup"><span data-stu-id="9de0a-125">Memory Management</span></span>](memory-management.md)
</dt> </dl>

 

 





